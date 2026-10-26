# Base de Conhecimento

## Dados Utilizados
Os arquivos locais da pasta `data` fornecem todo o contexto necessário para o funcionamento do agente de metas financeiras:

| Arquivo | Formato | Utilização no Agente |
| :--- | :--- | :--- |
| **historico_atendimento.csv** | CSV | Contextualizar interações anteriores e o histórico de planejamento do usuário. |
| **perfil_investidor.json** | JSON | Personalizar recomendações de prazos e alocação conforme o perfil (conservador, moderado, arrojado). |
| **produtos_financeiros.json** | JSON | Sugerir ferramentas, contas ou investimentos adequados para cada tipo de meta (curto, médio ou longo prazo). |
| **transacoes.csv** | CSV | Analisar o padrão de gastos mensais, identificar excessos e calcular a capacidade real de poupança. |

## Adaptações nos Dados
Os arquivos padrão do repositório foram mantidos e adaptados conceitualmente para o contexto de **Metas Financeiras**:
* As transações servem de base para o monitoramento de gastos e alertas de desvio de rota.
* O perfil de investidor e o histórico ajudam a dimensionar metas realistas de curto, médio e longo prazo (como reserva de emergência, compra de bens ou quitação de dívidas).

---

## Estratégia de Integração

### Como os dados são carregados?
Os arquivos JSON e CSV são carregados no início da sessão em Python (via Pandas/JSON modules) e injetados de forma dinâmica no contexto do prompt do sistema (`system prompt`) para que a LLM tenha acesso imediato aos dados do cliente.

### Como os dados são usados no prompt?
Os dados estruturados são consultados dinamicamente a cada mensagem. Quando o usuário define ou atualiza uma meta, a IA cruza os dados de `transacoes.csv` com o saldo e o objetivo para calcular a quantia exata que precisa ser poupada mensalmente.

---

## Exemplo de Contexto Montado

Dados do Cliente (simulados a partir da base):
* **Nome:** João Silva
* **Perfil:** Moderado
* **Saldo disponível:** R$ 5.000
* **Meta Ativa:** Comprar uma casa (Longo Prazo) - Alvo: R$ 200.000

Últimas transações (`transacoes.csv`):
* 01/11: Supermercado - R$ 450
* 02/11: Streaming - R$ 55

Com base nesses dados injetados, o assistente calcula a viabilidade da meta, monitora o progresso mensal e emite alertas se os gastos superarem o planejado.
