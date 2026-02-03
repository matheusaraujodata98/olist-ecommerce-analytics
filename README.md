# 📊 Data Analytics Olist: Otimização de Performance e Visualização de Dados

[![Status](https://img.shields.io/badge/Status-Concluído-green)](#)
[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-ETL%20%26%20Análise%20de%20Dados-150458?logo=pandas)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualização%20de%20Dados-4C72B0?logo=python)](https://seaborn.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Data%20Visualization-11557C?logo=python)](https://matplotlib.org/)
[![Looker Studio](https://img.shields.io/badge/Looker%20Studio-Dashboard-4285F4?logo=google)](https://lookerstudio.google.com/reporting/088487fd-c2bb-410c-8a1a-2473f69f1689)

## 📝 Sobre o Projeto
Este projeto foi desenvolvido como **Projeto Final do curso de Analista de Dados (EBAC)**, com o objetivo de aplicar o ciclo completo de uma análise de dados profissional. O trabalho percorre desde a ingestão de dados brutos até a entrega de insights estratégicos, simulando um cenário real de mercado para tomada de decisão.

---

## 🏗️ Fase 1: Seleção dos Dados
A base escolhida para este projeto é o **Brazilian E-Commerce Public Dataset by Olist**, extraído do Kaggle. 

**Requisitos atendidos:**
* **Relacional**: Conjunto de 8 tabelas cruzadas via IDs únicos.
* **Variáveis Temporais**: Tabela de pedidos com múltiplos timestamps de status (Data de compra, aprovação, entrega).
* **Volumetria**: Tabelas com alto número de colunas e registros (acima de 100 mil linhas), garantindo robustez estatística.

---

## 🔍 Fase 2: Análise Exploratória (EDA)
Nesta etapa, os dados foram investigados para compreender padrões, tendências e relacionamentos fundamentais para o negócio.

**Principais análises realizadas:**
* **Distribuição e Frequência**: Análise do volume de vendas mensal para identificar sazonalidade.
* **Top Categorias**: Identificação das categorias que mais geram receita (Beleza e Saúde, Relógios Presentes, etc.).
* **Identificação de Outliers**: Uso de Boxplots para analisar a dispersão de preços e valores discrepantes.
* **Correlação Logística**: Análise de dispersão entre peso do produto e valor do frete pago.
* **Performance Logística**: Histogramas para medir a eficiência e atrasos no tempo de entrega.

---

## ⚙️ Fase 3: Tratamento e Preparação (ETL)
O pipeline de dados foi construído em Python para limpar inconsistências e preparar a **OBT (One Big Table)**.

* **Data Cleaning**: Correção de tipos de dados (strings para datetime) e tratamento de valores ausentes/nulos.
* **Modelagem Analítica**: Realização de JOINs (`merge`) entre as tabelas `orders`, `order_items` e `products`.
* **Feature Engineering (Novas Colunas)**:
    * `month_year`: Criada para facilitar a análise de safras e tendências mensais.
    * `delivery_days`: Cálculo do tempo real de entrega (Data Entrega - Data Compra).

---

## 📈 Fase 4: Visualização e Dashboard Interativo (BI)
Transformação das descobertas em um dashboard executivo no **Looker Studio**, permitindo navegação dinâmica pelos dados da Olist (2016-2018).

### Arquitetura do Dashboard
* **Data Blending**: Combinação interna entre a tabela analítica e o cadastro de clientes para possibilitar a análise geográfica por estado.
* **Visualizações Implementadas**:
    * **KPI Cards**: Receita Total, Qtd. Pedidos, Ticket Médio, Frete Médio e Prazo Médio (Dias).
    * **Gráfico de Barras**: Top 10 categorias por faturamento.
    * **Série Temporal**: Evolução do Faturamento Mensal (Barras).
    * **Mapa de Bolhas**: Distribuição de clientes por estado com precisão via `CONCAT` geográfica.
    * **Gráfico de Rosca**: Proporção de pedidos por Status (Logística e Saúde da Operação).
    * **Tabela Dinâmica**: Cruzamento analítico de Faturamento por Categoria vs. Ano.

### Interatividade e UI/UX
* **Filtros Dinâmicos**: Controle de período fixo e busca por `order_id` para auditoria.
* **Filtro Cruzado**: Seleções em um gráfico (ex: clicar em um estado) reajustam todo o dashboard automaticamente.
* **Design**: Estilização em Dark Mode com acentos em verde para consistência visual com Seaborn.

---

## 🖼️ Visualização do Dashboard Final


🔗 **[Acesse o Dashboard Interativo aqui](https://lookerstudio.google.com/reporting/088487fd-c2bb-410c-8a1a-2473f69f1689)**

---
*Projeto desenvolvido por Matheus Araujo como parte do portfólio de Data Analytics.*