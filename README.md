# Exercícios de ETL, EDA e testes de hipóteses

Este repositório contém o notebook [`6_testes_hipoteses_etl.ipynb`](6_testes_hipoteses_etl.ipynb), desenvolvido em Python para praticar preparação de dados, visualização e inferência estatística.

## Conteúdo do notebook

### 1. Processo de ETL com Pandas e SQLAlchemy

- Leitura do dataset do Titanic.
- Visualização das primeiras linhas.
- Remoção de registos duplicados e de linhas com valores em falta.
- Ordenação pela coluna `Cabin`.
- Criação da tabela `passengers` e carregamento dos dados numa base de dados MySQL.

### 2. Análise exploratória com Pandas e Seaborn

Utiliza o dataset de vendas de videojogos para produzir:

- Histogramas e boxplots de `Year_of_Release` e `Critic_Score`.
- Gráfico dos cinco títulos mais frequentes.
- Matriz de correlação e heatmap das variáveis numéricas.
- Gráfico de dispersão entre `NA_Sales` e `Global_Sales`.

### 3. Testes de hipóteses com SciPy

Utiliza o dataset `sales.csv` para:

- Avaliar a normalidade da variável `Sales`.
- Executar um teste t de uma amostra.
- Comparar a média observada com uma média populacional definida no notebook.

> Nota: o enunciado da célula Markdown menciona `Restaurant_revenue.csv`, promoção e uma média de 305 euros, mas a implementação atual utiliza `sales.csv` e testa a média 230.

## Pré-requisitos

- Python 3.10 ou superior.
- Jupyter Notebook ou JupyterLab.
- MySQL disponível em `localhost:3306`, com uma base de dados chamada `app_db`, para executar a parte de ETL/SQL.
- Credenciais Kaggle configuradas para permitir os downloads feitos pelo `kagglehub`.
- O ficheiro `dados/titanic_dataset.csv` colocado no caminho esperado pelo notebook.

## Instalação

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
pip install python-dotenv pymysql jupyter
```

Defina a palavra-passe do MySQL antes de executar as células de base de dados:

```bash
export MYSQL_ROOT_PASSWORD="a-sua-palavra-passe"  # Windows PowerShell: $env:MYSQL_ROOT_PASSWORD="..."
```

## Execução

```bash
jupyter notebook 6_testes_hipoteses_etl.ipynb
```

Execute as células pela ordem apresentada. Os datasets obtidos através do Kaggle serão guardados em `dados/new_data/`.

## Estrutura esperada

```text
.
├── 6_testes_hipoteses_etl.ipynb
├── requirements.txt
└── dados/
    ├── titanic_dataset.csv
    └── new_data/
```
