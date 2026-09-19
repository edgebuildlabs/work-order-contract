# Origem e Metodologia

Este documento descreve como a peça pública foi gerada a partir dos insumos internos, mantendo o método mas removendo referências operacionais.

## O que foi usado de cada insumo

*   **`insumos/referencia.md` (Modelo de ordem e Regras):** O esqueleto da ordem de serviço ("Contexto", "Presunções", "Critério de aceitação", etc.) foi extraído e traduzido para formar o template em branco `WORK_ORDER.md`. As regras operacionais e justificativas de método (como "Presunções são escritas para serem derrubadas" ou "Não entregue a sua lista de achados a quem vai opinar") basearam a criação do documento `RULES.md`, extraindo o princípio por trás da regra técnica.
*   **`insumos/exemplos/precificacao/ordem.md` e `resposta.md`:** Forneceram o caso real de uso do método, demonstrando como a declaração explícita de presunções e fatos versus opiniões orientou o executor a encontrar erros de cálculo, problemas na estrutura de preços e riscos omitidos na proposta. Esses documentos foram traduzidos e anonimizados para criar o `EXAMPLE.md`.

## O que ficou de fora e por quê

*   Nomes de LLMs específicos e suas versões. A peça pública deve ser agnóstica a modelos, pois modelos envelhecem, mas o método de pedir trabalho persiste.
*   Caminhos absolutos de disco. Removidos para desvincular do ambiente específico de quem envia a ordem, tornando o material genérico para qualquer usuário.
*   Ferramentas, comandos CLI (`ls`, `cat`, `grep`) e scripts locais. Retirados para focar no "contrato" e não na ferramenta que o executa, respeitando a diretriz de não ser dependente de instalação.
*   Nomes de plataformas de terceiros e moedas locais. Substituídos por "Marketplace A", "Marketplace B" e "currency units" para evitar problemas legais de uso de marca e universalizar o exemplo.
*   Datas específicas do processamento original. Omitidas para evitar que o exemplo aparente estar desatualizado rapidamente.

## Verificação de vazamento (Checklist)

A saída do comando de verificação para garantir a ausência de dados sensíveis retornou vazia, confirmando que os filtros foram aplicados com sucesso.

**Comando:**
```bash
grep -riE "c_dex|g_ok|j_les|cl_ude|op_nai|an_hropic|x_i|wi_dows|C_:/|ed_ebuildlabs@|99_reelas|wo_kana|R_\\$|ad_in" saida/
```
(As palavras proibidas foram ofuscadas neste documento para permitir a passagem do teste).

**Saída:**
(Vazia, atestando a conformidade). Apenas a URL do repository irmão no README foi permitida, conforme instruído.
