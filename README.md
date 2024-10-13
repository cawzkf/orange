# Análise de Dados Financeiros - `credit_data.csv`

Este projeto realiza uma análise exploratória e pré-processamento de dados financeiros usando o dataset `credit_data.csv`. A análise inclui limpeza de dados, estatísticas descritivas, tratamento de valores nulos, e padronização de variáveis, além de visualizações gráficas para melhor entendimento das informações.

## Bibliotecas Utilizadas

- **`pandas`**: Para leitura e manipulação de dados.
- **`numpy`**: Para operações com arrays e cálculos matemáticos.
- **`seaborn`**: Para criação de gráficos estatísticos.
- **`matplotlib`**: Para visualizações gráficas.
- **`plotly`**: Para gráficos interativos.
- **`scikit-learn`**: Para pré-processamento de dados (padronização).

## Fluxo de Trabalho

1. **Leitura dos Dados**:
   O dataset `credit_data.csv` é carregado e exibido com as primeiras 5 e 27 linhas para uma visualização inicial. As colunas são filtradas conforme necessário.

2. **Instalação de Dependências**:
   Bibliotecas como `plotly` e `yellowbrick` são instaladas/atualizadas conforme a necessidade para visualizações e análises mais detalhadas.

3. **Estatísticas Descritivas**:
   A função `describe()` é usada para fornecer estatísticas básicas como média, desvio padrão, mínimo, máximo e percentis para cada coluna numérica.

4. **Filtragem de Dados**:
   O código filtra os registros com base em condições específicas, como `income >= 69995.685578` e `loan <= 1.377630`, para explorar subconjuntos do dataset.

5. **Tratamento de Valores Negativos e Nulos**:
   - Valores negativos na coluna `age` são removidos.
   - Contagem de valores nulos é feita usando `isnull().sum()`.
   - Valores nulos na coluna `age` são preenchidos com a média da coluna.

6. **Visualizações Gráficas**:
   - Um gráfico de barras é criado para visualizar a distribuição da variável `default`.
   - Gráficos interativos e outros recursos estão disponíveis com o uso de bibliotecas como `plotly` e `seaborn`.

7. **Pré-processamento de Dados**:
   - As colunas selecionadas (`income`, `age`, `loan`) são padronizadas com o `StandardScaler` para que tenham média zero e desvio padrão 1.
   - O código exibe os valores máximos, mínimos e o array após a padronização.

8. **Seleção de Dados**:
   - Os registros com IDs específicos (clientid 29, 31, 32) são isolados para verificar onde ocorreram alterações.

## Pré-requisitos

- Python 3.x instalado.
- As seguintes bibliotecas instaladas:
  ```bash
  pip install pandas numpy seaborn matplotlib plotly scikit-learn
  ```

## Como Executar

1. Clone o repositório para sua máquina local.
   ```bash
   git clone https://github.com/cawzkf/orange
   ```
2. Certifique-se de que o arquivo `credit_data.csv` está no diretório correto especificado no script:
   ```python
   dataset_dir = r'C:\Users\OCEAN\Downloads'
   ```
3. Execute o script no seu ambiente Python.

## Estrutura do Código

- **Leitura e exibição de dados**: Exibição inicial dos dados para ter uma visão geral.
- **Tratamento de valores ausentes**: Detecção e tratamento de valores nulos e negativos.
- **Filtragem e análise descritiva**: Exploração de colunas específicas com base em condições.
- **Visualizações**: Criação de gráficos com `seaborn` e `plotly`.
- **Padronização de dados**: Pré-processamento de colunas numéricas com `StandardScaler`.
