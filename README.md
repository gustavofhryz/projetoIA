# MetasBot - Agente Financeiro Inteligente com IA Generativa

# projetoIA

Agente financeiro com IA Generativa que vai além de responder perguntas: antecipa necessidades, personaliza objetivos, calcula valores e monitora o orçamento.

## 🎯 Contexto do Projeto

Os assistentes virtuais no setor financeiro estão evoluindo de simples chatbots reativos para agentes inteligentes e proativos. Este projeto concretiza a criação de um agente que utiliza IA Generativa para:

- **Antecipar necessidades** de poupança e planejamento em vez de apenas responder perguntas.
- **Personalizar objetivos** de curto, médio e longo prazo (como casa, reserva de emergência e quitação de dívidas) com base no perfil do utilizador.
- **Realizar cálculos matemáticos precisos** de quanto dinheiro é necessário poupar por mês.
- **Garantir monitoramento, alertas de progresso e ajustes de rota** quando os gastos excedem o planejado.
- **Garantir segurança e confiabilidade** (estratégias anti-alucinação e restrição de escopo).

## 📂 Estrutura do Repositório

```
projetoA/
├── assets/          # Imagens da aplicação e evidências dos testes executados
├── data/            # Dados simulados (histórico, perfil, produtos e transações)
├── docs/            # Documentação completa do projeto
│   ├── 01-documentacao-agente.md
│   ├── 02-base-conhecimento.md
│   ├── 03-prompts.md
│   ├── 04-metricas.md
│   └── 05-pitch.md
├── examples/        # Exemplos de referência da DIO
├── src/             # Código-fonte da aplicação (Streamlit / LLM)
│   ├── app.py       # Aplicação principal (interface Streamlit)
│   ├── agente.py    # Lógica do agente
│   ├── config.py    # Configurações (chaves de API, etc.)
│   └── requirements.txt  # Dependências
└── README.md        # Documentação principal do projeto
```

## ✅ Pré-requisitos

- **Python 3.10 ou superior** (verifique com `python --version`)
- **Git** (para clonar o repositório)
- **Chave de API** do provedor de LLM utilizado pelo projeto (por exemplo, OpenAI)

## 🚀 Como Executar

### 1. Clonar o repositório

```bash
git clone https://github.com/gustavofhryz/projetoIA.git
cd projetoIA
```

### 2. Criar e ativar um ambiente virtual

**Windows (PowerShell):**
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**Linux / macOS:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Instalar as dependências

```bash
pip install -r src/requirements.txt
```

As dependências principais são `streamlit`, `openai` e `python-dotenv`.

### 4. Configurar as variáveis de ambiente

Crie um arquivo `.env` na **raiz do projeto** (nunca o envie para o GitHub) com a sua chave de API:

```env
OPENAI_API_KEY=sua_chave_aqui
```

> Ajuste o nome da variável caso o `src/config.py` utilize outro nome.

Adicione `.env` e `.venv/` ao `.gitignore` para evitar que credenciais e o ambiente virtual sejam versionados.

### 5. Executar a aplicação

A partir da raiz do projeto:

```bash
streamlit run src/app.py
```

Alternativamente:

```bash
python -m streamlit run src/app.py
```

A aplicação abrirá automaticamente no navegador em `http://localhost:8501`. Se não abrir, acesse esse endereço manualmente.

## 🧪 Testes e Evidências

Os resultados dos testes executados e as capturas de tela ficam na pasta `assets/`. A documentação de métricas de qualidade está em `docs/04-metricas.md`.

## 📚 Documentação

| Arquivo | Conteúdo |
|---|---|
| `docs/01-documentacao-agente.md` | Descrição completa do agente |
| `docs/02-base-conhecimento.md` | Base de conhecimento utilizada pelo agente |
| `docs/03-prompts.md` | Prompts do sistema e exemplos de interação |
| `docs/04-metricas.md` | Métricas de avaliação |
| `docs/05-pitch.md` | Apresentação do projeto |

## 🛡️ Segurança e Limitações

- O agente é um **auxílio ao planejamento financeiro** e não substitui a orientação de um profissional certificado.
- Os dados em `data/` são **simulados**; não utilize informações financeiras reais sem antes revisar a privacidade.
- Respostas geradas por IA podem conter imprecisões. Os cálculos devem ser conferidos antes de decisões importantes.

## 🛠️ Solução de Problemas

- **`ModuleNotFoundError`**: confirme que o ambiente virtual está ativado e que `pip install -r src/requirements.txt` foi executado.
- **Erro de autenticação na API**: verifique se o arquivo `.env` está na raiz do projeto e se a chave está correta.
- **`streamlit: command not found`**: use `python -m streamlit run src/app.py`.
- **Porta 8501 em uso**: execute `streamlit run src/app.py --server.port 8502`.

## 📄 Licença

Projeto desenvolvido como parte de estudos em IA. Defina uma licença caso pretenda reutilizar ou distribuir o código.

MetasBot Em Funcionamento:

<img width="669" height="521" alt="Teste 2a" src="https://github.com/user-attachments/assets/9b9d5d8b-1b52-4d01-b021-fcf1efd7ccb1" />

<img width="620" height="491" alt="Teste 2b" src="https://github.com/user-attachments/assets/926a7efd-98c0-439c-ad9a-c28c15597ae6" />

<img width="614" height="598" alt="Teste 2c" src="https://github.com/user-attachments/assets/63d71a3b-6f7a-4aea-b283-0cd187741236" />

<img width="676" height="689" alt="Teste 1" src="https://github.com/user-attachments/assets/1ee59b8e-255a-4c02-9482-e8879a1adfee" />

<img width="672" height="596" alt="Teste 3" src="https://github.com/user-attachments/assets/ad1575c4-ed6c-4a11-82a8-c5e00a3c3366" />

<img width="674" height="681" alt="Teste 4" src="https://github.com/user-attachments/assets/60c2e49b-e12f-468c-8c25-69d50807ffc0" />


Desenvolvido por Gustavo como projeto prático para o bootcamp de Inteligência Artificial da DIO (Digital Innovation One).

