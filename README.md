# Gasoline Price Analysis and Prediction

Este repositório contém um projeto completo de análise e previsão de preços de gasolina no Brasil, utilizando dados de diversas fontes (ANP, produção de petróleo, cotações internacionais, etc.). O objetivo é entender os principais fatores que influenciam o preço da gasolina e construir um modelo preditivo que considere variáveis como cotação do dólar, preço do petróleo e produção interna.

## Objetivos

### Análise Exploratória de Dados (EDA):

> Explorar o comportamento histórico dos preços da gasolina, produção de petróleo, vendas de combustíveis e cotação do dólar.

> Identificar tendências, sazonalidades e correlações entre variáveis.

### Engenharia de Dados (Data Engineering):

> Limpeza e padronização de múltiplas bases de dados com diferentes formatos (CSV, PKL).

> Conversão de tipos, tratamento de valores ausentes, agregação de dados diários para semanal ou mensal, e merge final em um dataset unificado.

### Construção de Modelo Preditivo:

> Integrar dados de produção de petróleo, cotações de petróleo (Brent) e USD/BRL para prever o preço futuro da gasolina.

> Comparar diferentes técnicas de modelagem (por exemplo, ARIMAX, regressões, RandomForest, XGBoost) para avaliar a performance.

## Importância do Projeto

> Relevância Econômica: O preço dos combustíveis afeta a inflação, o custo de vida e a competitividade do setor de transporte.

> Fatores Externos: O mercado de petróleo é global e sofre influência de eventos geopolíticos, cotação cambial e políticas de preços internas.

> Tomada de Decisão: Modelos preditivos podem auxiliar governos, empresas e consumidores a planejar estratégias de compra, logística e políticas públicas.

## Modelos e Técnicas Utilizadas

### Limpeza e Padronização de Dados:

> Remoção de BOM, correção de encoding, rename de colunas, conversão de strings para datas e floats.

> Tratamento de valores ausentes com interpolação, ffill/bfill, etc.

### Agregação Temporal:

> Resample diário para semanal (preço da gasolina),

> Reamostragem mensal para semanal (produção de petróleo),

> Manutenção de séries semanais (petróleo e USD/BRL).

### Feature Engineering:

> Criação de colunas defasadas (lags), médias móveis, variações percentuais.

> Merge final em uma única base de dados.

### Visualizações (EDA):

> Histogramas, boxplots, séries temporais, scatter plots e heatmaps de correlação.

### (Em andamento) Modelagem Preditiva:

> Comparar modelos de série temporal (ARIMAX, SARIMAX) e modelos de Machine Learning (Regressões, XGBoost, etc.) para previsão de preço.

## Estrutura do Repositório

### dataset/

> Contém todos os arquivos brutos e/ou tratados (CSV, PKL) usados na análise e no modelo

### engineeringdata-cleaning.ipynb

> Notebook que contém o processo de ingestão, limpeza, conversão de tipos, agregação temporal (resample) e salvamento em formato PKL.

### engineeringdata-plots-CA.ipynb

> Notebook principal de análise exploratória (EDA) dos dados de gasolina (distribuição, evolução temporal, boxplots etc.).

### engineeringdata-plots-Extras.ipynb

> Notebook que explora dados adicionais (petróleo, câmbio, produção), gera gráficos comparativos e avalia correlações.

### data_unificados.pkl

> Arquivo gerado em um dos passos intermediários, contendo dados de gasolina consolidados antes do merge com outras fontes.

### dados_modelo_final.pkl

> Dataset unificado (semanal) com todas as variáv
