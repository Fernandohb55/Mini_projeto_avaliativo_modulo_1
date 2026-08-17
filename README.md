
# Análise Exploratória de Dados - Varejo

Este repositório contém o projeto de Análise Exploratória de Dados (EDA) e higienização da base de dados de varejo composta por 830.000 registros. O estudo abrange desde o tratamento estrutural e limpeza de duplicadas até a geração de inteligência de negócios com regras de desconto e análise sazonal.

## Sobre o Projeto

O objetivo do projeto é transformar dados brutos de transações de varejo em insights estratégicos para a tomada de decisão. A análise identifica o comportamento de compra por perfil de cliente (estado civil, classe social e quantidade de filhos) e sazonalidade das vendas, propondo ações promocionais direcionadas para categorias de baixo desempenho.

## Principais Insights

* **Sazonalidade Crítica:** Novembro registrou o menor volume de vendas do ano (40.912 transações), enquanto Janeiro atingiu o ápice com 83.963 vendas.
* **Liderança por Categoria:** A categoria de **Alimentos** lidera com 434.767 vendas, ao passo que **Acessorios** apresentou o menor desempenho (14.557 itens), justificando uma campanha promocional com 10% de desconto.
* **Concentração de Segmento:** O **Segmento B** representa a maior fatia do volume de compras (530.163 transações), seguido pelo Segmento C (232.101) e Segmento A (67.736).
* **Perfil Familiar:** 52,47% dos clientes não possuem filhos. A média geral é de 1,15 filho por cliente, mantendo-se uniforme entre as classes sociais.
* **Viabilidade Promocional por Filhos:** A concessão de desconto de 5% por filho (com teto de 20% para 4 filhos) afeta a menor parcela da base, visto que clientes com 4 filhos correspondem a apenas 9,68% do total.
* **Qualidade dos Dados:** Identificou-se a presença de 96.553 linhas duplicadas e 4 colunas nulas (`Unnamed: 10` a `Unnamed: 13`), tratadas na fase de saneamento de dados.

## Sprints do Projeto

| **Sprint**   | **Etapa**               | **Descrição das Atividades**                                                                                               |
| ------------------ | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Sprint 1** | Importação dos Dados        | Leitura preliminar com`csv.DictReader`e carregamento do DataFrame via`pd.read_csv`com delimitador.                             |
| **Sprint 2** | Normalização                | Conversão da coluna`DATA`para`datetime`, remoção de espaços com`str.strip()`e padronização de maiúsculas/minúsculas. |
| **Sprint 3** | Limpeza de Nulos e Duplicatas | Mapeamento de valores nulos (`.isna()`)e remoção de 96.553 duplicatas com`df.drop_duplicates()`.                             |
| **Sprint 4** | Estatística Descritiva       | Agrupamento por segmento, categoria e número de filhos, além do cálculo das regras promocionais.                                |
| **Sprint 5** | Relatório & Documentação   | Consolidação dos indicadores finais de desempenho e elaboração da documentação técnica.                                     |
| **Sprint 6** | Versionamento                 | Publicação do código-fonte, dados limpos e documentação no repositório GitHub.                                               |

## Pré-requisitos e Configuração do VS Code

Para reproduzir ou contribuir com o projeto, siga o passo a passo para instalação e configuração do ambiente de desenvolvimento no  **Visual Studio Code** .

### 1. Instalação das Ferramentas Básicas

* **Python 3.11+** : Faça o download e instale a versão oficial do [Python](https://www.python.org/downloads/). Marque a opção **"Add Python to PATH"** durante a instalação.
* **VS Code** : Instale o editor de código oficial pelo site do [Visual Studio Code](https://code.visualstudio.com/).

### 2. Extensões Recomendadas no VS Code

Abra o VS Code, acesse o menu de extensões (`Ctrl + Shift + X` ou `Cmd + Shift + X` no macOS) e instale as seguintes extensões:

* **Python**  *(Microsoft)* : Adiciona suporte completo à linguagem Python, com suporte a autocompletar (IntelliSense) e depuração.
* **Jupyter**  *(Microsoft)* : Permite executar, editar e visualizar arquivos de Jupyter Notebook (`.ipynb`) diretamente no VS Code.
* **Data Wrangler**  *(Microsoft)* : Interface gráfica para exploração e limpeza rápida de dados integrada aos DataFrames do Pandas.
* **Office Viewer / Excel Viewer** : Permite visualizar e inspecionar planilhas `.csv` e `.xlsx` sem precisar sair do editor.

## Tecnologias e Bibliotecas Utilizadas

* **Python 3.11;**
* **Pandas** (Tratamento, agregação e manipulação de dados);
* **NumPy** (Apoio a cálculos estruturados);
* **Módulo CSV** (Leitura estruturada via dicionários);

## Como Executar

1. Clone o repositório para o seu ambiente local.
2. Posicione o arquivo `base_varejo.csv` no mesmo diretório do notebook `Mini_projeto.ipynb`.
3. Abra o VS Code na pasta do projeto e selecione o kernel Python configurado.
4. Execute as células do Jupyter Notebook sequencialmente da **Sprint 1** à **Sprint 6**.


## 📝 Licença

Este projeto está público.
