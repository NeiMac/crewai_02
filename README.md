# Análise de Mercado com CrewAI

Um projeto de análise de mercado automatizado utilizando CrewAI, que emprega múltiplos agentes especializados para coletar, analisar e gerar relatórios sobre setores específicos.

## 📋 Descrição

Este projeto implementa um sistema multi-agente que trabalha de forma coordenada para:
1. **Coletar dados** sobre um setor de mercado específico
2. **Analisar tendências** e identificar padrões emergentes
3. **Gerar relatórios** estruturados e compreensíveis

## 🏗️ Arquitetura

### Agentes

#### 1. **Pesquisador de Mercado**
- **Função**: Coletar e organizar informações relevantes sobre o setor
- **Objetivo**: Garantir que todas as informações estejam atualizadas e bem documentadas
- **Saída**: Relatório estruturado contendo dados de mercado

#### 2. **Analista de Tendências**
- **Função**: Analisar os dados coletados e identificar padrões
- **Objetivo**: Identificar tendências emergentes, oportunidades e ameaças
- **Saída**: Relatório com insights e análise detalhada

#### 3. **Redator de Relatórios**
- **Função**: Transformar análises em um relatório final
- **Objetivo**: Elaborar um relatório consolidado e compreensível para tomadores de decisão
- **Saída**: Relatório estruturado em formato Markdown

### Tarefas

1. **Coleta de Dados**: Pesquisa e coleta de informações atualizadas
2. **Análise de Tendências**: Exame dos dados e identificação de padrões
3. **Redação do Relatório**: Criação de um relatório detalhado com resumo executivo

## 🚀 Como Usar

### Pré-requisitos

- Python 3.8+
- pip ou conda

### Instalação

1. Clone o repositório:
```bash
git clone https://github.com/NeiMac/crewai_02.git
cd crewai_02
```

2. Crie um ambiente virtual:
```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1  # Windows PowerShell
# ou
source .venv/bin/activate  # Linux/Mac
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

4. Configure as variáveis de ambiente:
Crie um arquivo `.env` com as suas chaves de API necessárias para os agentes (ex: LLM API keys).

### Execução

Execute o notebook Jupyter:
```bash
jupyter notebook analise_mercado.ipynb
```

Ou execute cada célula do notebook sequencialmente:
- A célula de importação carrega as dependências
- As células de agentes definem os três agentes especializados
- As células de tarefas definem as atividades a serem executadas
- A célula de crew coordena os agentes
- A célula de kickoff inicia a análise com o setor desejado

## 📁 Estrutura do Projeto

```
crewai_02/
├── README.md                 # Este arquivo
├── analise_mercado.ipynb     # Notebook principal com o projeto
├── requirements.txt          # Dependências do projeto
├── arquivo.md               # Relatório em Markdown (gerado)
├── arquivo.html             # Relatório em HTML (gerado)
└── .env                      # Variáveis de ambiente (não versionado)
```

## 📊 Saídas Geradas

O projeto gera automaticamente:
- **arquivo.md**: Relatório em formato Markdown
- **arquivo.html**: Relatório em formato HTML

## 🔧 Personalização

### Alterar o Setor Analisado

Para analisar um setor diferente, modifique a chamada:
```python
resultado = crew.kickoff(inputs={"sector": "Seu Setor Aqui"})
```

### Adicionar ou Modificar Agentes

Você pode criar novos agentes seguindo o padrão:
```python
novo_agente = Agent(
    role="Seu Role",
    goal="Seu Objetivo",
    backstory="Sua Descrição",
    allow_delegation=False,
    verbose=True
)
```

## 📦 Dependências

- `crewai`: Framework de multi-agentes
- `python-dotenv`: Gerenciamento de variáveis de ambiente
- `markdown`: Processamento de Markdown
- `pdfkit`: Conversão de conteúdo (opcional)
- `ipython`: Exibição de conteúdo em Jupyter

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para:
- Reportar bugs
- Sugerir novas funcionalidades
- Melhorar a documentação
- Adicionar novos agentes especializados

## 📝 Licença

Este projeto está sob licença MIT.

## 👨‍💻 Autor

**NeiMac**

---

**Última atualização**: Dezembro 2025
