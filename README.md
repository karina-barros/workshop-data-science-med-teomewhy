# **Workshop de Data Science - MeD & Téo Me Why**

Este repositório contém o projeto desenvolvido durante o Workshop de Data Science promovido pela comunidade Mulheres em Dados, em parceria com o Téo Me Why. O projeto foi conduzido utilizando Databricks, com etapas baseadas nas metodologias CRISP-DM e SEMMA.

## **Sumário**

- [Introdução](#introdução)
- [Objetivo do Projeto](#objetivo-do-projeto)
- [Entendimento do Negócio](#entendimento-do-negócio)
- [Entendimento dos Dados](#entendimento-dos-dados)
- [Preparação dos Dados](#preparação-dos-dados)
- [Modelagem e Avaliação](#modelagem-e-avaliação)
- [Implementação](#implementação)
- [Conclusões](#conclusões)
- [Referências](#referências)

## **Introdução**

Este projeto foi realizado em grupo, sob orientação do Téo Me Why, no Workshop de Data Science realizado em agosto de 2024. Utilizamos Databricks para todo o fluxo de trabalho, que incluiu SQL e Python, focando em um problema de **churn prediction**.

## **Objetivo do Projeto**

O objetivo principal do projeto foi desenvolver um modelo preditivo capaz de identificar clientes com alta probabilidade de churn, utilizando dados transacionais disponíveis nas tabelas do Databricks.

## **Entendimento do Negócio**

Na etapa de entendimento do negócio, discutimos os objetivos do projeto e as expectativas quanto aos resultados, vislumbrando as vantagens na utilização de modelos preditivos para atingir o objetivo.
Definiu-se que um cliente seria considerado "churn" (1) se não realizasse transações por mais de 28 dias consecutivos.

## **Entendimento dos Dados**

Exploramos e analisamos os dados disponíveis nas seguintes tabelas do Databricks:

- `silver.upsell.cliente`
- `silver.upsell.transacoes`
- `silver.upsell.transacao_produto`

Criamos um **dicionário de dados** que pode ser acessado [aqui](dicionario-dados.md).

## **Preparação dos Dados**

Nesta etapa, os dados foram transformados e preparados para a modelagem. Utilizamos técnicas de **limpeza**, **tratamento de valores ausentes** e **criação de novas features**, incluindo:

- `periodoDoDiaNum`
- `periodoDoDiaStr`
- `produtoMaisComprado`

**Template de consultas SQL e transformações realizadas**: [link para consultas](https://teomewhy-primary.cloud.databricks.com/browse/folders/3088628433384683?o=2977606981748304).

## **Modelagem e Avaliação**

Seguindo a metodologia SEMMA, as etapas realizadas foram:

### **1. Sample**

Selecionamos uma amostra representativa dos dados para a análise.

### **2. Explore**

Realizamos a Análise Exploratória dos Dados (EDA) utilizando `pandas`, `seaborn` e `matplotlib`. [Gráficos e insights aqui](graficos.md).

### **3. Modify**

Realizamos o tratamento de dados ausentes, seleção de variáveis, e criamos a ABT (Analytical Base Table).

### **4. Model**

Diversos modelos de classificação foram treinados, e hiperparâmetros ajustados usando `GridSearchCV`. [Veja detalhes dos modelos e acurácia aqui](https://teomewhy-primary.cloud.databricks.com/?o=2977606981748304#notebook/541788629925308).

### **5. Assess**

Os modelos foram comparados com base na acurácia e AUC, e o melhor foi validado no conjunto de teste. O modelo final foi implementado para prever churn em novos dados.

## **Implementação**

O modelo final foi aplicado em novos dados para verificar sua capacidade de generalização. A implementação foi realizada no Databricks, com uso da Feature Store.

## **Conclusões**

Os modelos apresentaram acurácia entre 79% e 81% na base de teste.
O projeto mostrou a importância da preparação adequada dos dados e da seleção criteriosa de features. Sendo assim, propõe-se definição de modelo a partir das features de maior relevância para caracterização da variável target, visando aprimoramento do desempenho do modelo preditivo.

## **Referências**

- [Documentação do scikit-learn](https://scikit-learn.org/stable/supervised_learning.html#)
- [Twitch - Téo Me Why](https://teomewhy.org/twitch)
- [Integrando DATABRICKS e GITHUB!!](https://www.youtube.com/watch?v=16naBdipd1Q&t=81s)
- [Passo a passo para construir PIPELINES!](https://www.youtube.com/watch?v=LRmmtT20290)
- [pipeline_tutorial](https://github.com/yukioandre/youtube/blob/master/pipeline_tutorial.ipynb)

---