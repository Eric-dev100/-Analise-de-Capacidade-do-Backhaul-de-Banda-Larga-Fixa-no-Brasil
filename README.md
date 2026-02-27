# 🌐 Análise de Capacidade do Backhaul de Banda Larga Fixa no Brasil

## 📌 Sobre o Projeto
Este projeto realiza uma Análise Exploratória de Dados (EDA) sobre a infraestrutura de banda larga fixa no Brasil, com foco específico na capacidade e taxa de ocupação das redes de distribuição (*backhaul*). O objetivo é mapear a saúde da infraestrutura de telecomunicações do país, identificando regiões que se aproximam do limite crítico de esgotamento de rede.

## 🗂️ Conjunto de Dados
Os dados utilizados neste projeto são provenientes de bases abertas:
* **Dados da Anatel:** Informações técnicas sobre a capacidade de backhaul de banda larga fixa.
* **Diretórios Brasileiros (Base dos Dados):** Tabelas auxiliares contendo informações padronizadas sobre municípios e estados (UFs) para enriquecimento geográfico.

## 🛠️ Tecnologias e Bibliotecas Utilizadas
* **Python 3.12**
* **Pandas:** Para manipulação, limpeza e cruzamento de dados (ETL).
* **NumPy:** Para operações numéricas de suporte.
* **Matplotlib & Seaborn:** Para a criação de visualizações estatísticas e de negócios.

## 🚀 Metodologia
1. **Extração e Cruzamento (Merge):** Leitura dos arquivos CSV e junção das tabelas de capacidade técnica com a base de municípios usando chaves relacionais (`id_municipio`).
2. **Limpeza de Dados (Data Cleaning):** Tratamento de valores nulos (imputação de `0` para capacidades não preenchidas) e remoção de registros sem data de atendimento válida.
3. **Agrupamento e Cálculos:** Agregação de dados por região e ano de atendimento, e criação de uma métrica de **Série Acumulada** (`cumsum`) da capacidade de backhaul.
4. **Visualização:** Geração de gráficos de barras horizontais indicando a taxa de ocupação por região, incluindo uma linha de alerta visual configurada em 80% (indicador de possível esgotamento).

## 📊 Principais Resultados
O notebook gera visualizações claras que permitem a tomada de decisão, destacando instantaneamente quais regiões do Brasil necessitam de maior investimento em infraestrutura para evitar gargalos na distribuição de internet.
