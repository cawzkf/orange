# Análise de Dados Financeiros - Credit Data

**Análise exploratória e pré-processamento** de dados financeiros usando o dataset `credit_data.csv`. Desenvolvido durante curso da **Ocean**, a análise inclui limpeza de dados, estatísticas descritivas, tratamento de valores nulos, padronização de variáveis e visualizações gráficas para melhor entendimento das informações.

---

## Funcionalidades

* **Análise exploratória** de dados financeiros
* **Limpeza e tratamento** de valores nulos e negativos
* **Estatísticas descritivas** completas
* **Visualizações gráficas** interativas e estáticas
* **Padronização de variáveis** para machine learning
* **Filtragem de dados** por condições específicas
* **Análise de distribuições** e correlações

---

## Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=matplotlib&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=seaborn&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Scikit Learn](https://img.shields.io/badge/Scikit_Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

### Bibliotecas Detalhadas

* **Pandas** — Leitura e manipulação de dados estruturados
* **NumPy** — Operações com arrays e cálculos matemáticos
* **Seaborn** — Criação de gráficos estatísticos elegantes
* **Matplotlib** — Visualizações gráficas fundamentais
* **Plotly** — Gráficos interativos e dashboards
* **Scikit-learn** — Pré-processamento e padronização de dados
* **Yellowbrick** — Visualizações para machine learning

---

## Estrutura do Projeto

```
projeto/
├── credit_data.csv           # Dataset principal
├── analise_financeira.py     # Script de análise
├── README.md                 # Documentação
└── outputs/                  # Gráficos e resultados gerados
```

---

## Fluxo de Trabalho

### 1. Carregamento e Exploração Inicial
```python
# Leitura do dataset
df = pd.read_csv('credit_data.csv')
df.head()  # Primeiras 5 linhas
df.describe()  # Estatísticas descritivas
```

### 2. Limpeza e Tratamento de Dados
* **Remoção de valores negativos** na coluna `age`
* **Tratamento de valores nulos** com preenchimento pela média
* **Contagem de missings** usando `isnull().sum()`
* **Filtragem por condições** específicas

### 3. Análise Exploratória
* **Estatísticas descritivas** (média, desvio padrão, percentis)
* **Distribuição de variáveis** categóricas e numéricas
* **Análise de correlações** entre variáveis
* **Identificação de outliers**

### 4. Visualizações
* **Gráficos de barras** para distribuição de `default`
* **Histogramas** para variáveis numéricas
* **Boxplots** para detecção de outliers
* **Gráficos interativos** com Plotly

### 5. Pré-processamento
```python
from sklearn.preprocessing import StandardScaler

# Padronização das variáveis
scaler = StandardScaler()
dados_padronizados = scaler.fit_transform(df[['income', 'age', 'loan']])
```

---

## Análises Realizadas

### Variáveis do Dataset
* **income** — Renda do cliente
* **age** — Idade do cliente
* **loan** — Valor do empréstimo
* **default** — Inadimplência (variável target)

### Filtragens Aplicadas
* Registros com `income >= 69995.685578`
* Registros com `loan <= 1.377630`
* Análise específica de clientes (IDs 29, 31, 32)

### Tratamentos Realizados
* **Valores negativos** em `age` removidos
* **Valores nulos** preenchidos com média
* **Padronização** para média 0 e desvio padrão 1

---

## Pré-requisitos

* **Python 3.x** instalado
* **Ambiente virtual** (recomendado)
* **Jupyter Notebook** ou IDE Python

### Instalação de Dependências

```bash
pip install pandas numpy seaborn matplotlib plotly scikit-learn yellowbrick
```

---

## Como Executar

### 1. Clone o Repositório
```bash
git clone https://github.com/cawzkf/analise-dados-financeiros.git
cd analise-dados-financeiros
```

### 2. Configure o Ambiente
```bash
# Criar ambiente virtual
python -m venv venv

# Ativar ambiente (Windows)
venv\Scripts\activate

# Ativar ambiente (Linux/Mac)
source venv/bin/activate

# Instalar dependências
pip install -r requirements.txt
```

### 3. Execute a Análise
```bash
python analise_financeira.py
```

### 4. Configuração do Dataset
Certifique-se de que o arquivo `credit_data.csv` está no diretório correto:
```python
dataset_dir = r'C:\Users\OCEAN\Downloads'
```

---

## Resultados e Insights

### Estatísticas Principais
* **Análise descritiva** completa das variáveis numéricas
* **Distribuição de inadimplência** no dataset
* **Correlações** entre idade, renda e valor do empréstimo

### Tratamento de Dados
* **Valores negativos** identificados e removidos
* **Missing values** tratados adequadamente
* **Padronização** aplicada para análises futuras

### Visualizações Geradas
* **Distribuições** das variáveis principais
* **Análise de outliers** com boxplots
* **Gráficos interativos** para exploração

---

## Curso Ocean

Este projeto foi desenvolvido como parte do programa educacional da **Ocean**, focando em:
* **Data Science** e análise de dados
* **Python** para análise estatística
* **Visualização** de dados
* **Pré-processamento** para machine learning

---

## Repositório

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/cawzkf/analise-dados-financeiros)

**Repositório:** [github.com/cawzkf/orange](https://github.com/cawzkf/orange)

---

<div align="center">

**Desenvolvido durante curso Ocean - Data Science**

![Python](https://img.shields.io/badge/Made_with-Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Ocean](https://img.shields.io/badge/Curso-Ocean-0066CC?style=flat-square&logo=education&logoColor=white)

</div>
