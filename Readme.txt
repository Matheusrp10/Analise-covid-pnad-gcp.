# Análise de Impacto da COVID-19 (PNAD) 📊🏥

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Google Cloud](https://img.shields.io/badge/Google_Cloud-BigQuery-red?style=for-the-badge&logo=google-cloud)
![Status](https://img.shields.io/badge/Status-Concluído-success?style=for-the-badge)

Este projeto compõe a **Fase 3 do Tech Challenge** do curso de Data Analytics. O objetivo principal foi analisar os impactos clínicos, econômicos e comportamentais da pandemia no Brasil, utilizando dados da **PNAD-COVID-19 (IBGE)** processados em nuvem.

## 🎯 Objetivos do Projeto
O estudo buscou responder a perguntas estratégicas para o planejamento hospitalar e econômico:
1.  **Economia:** Qual a relação entre a renda média da população e o recebimento do Auxílio Emergencial?
2.  **Comportamento:** A presença de sintomas respiratórios graves aumenta a procura imediata por hospitais?
3.  **Sazonalidade:** Como os sintomas clínicos evoluíram ao longo dos meses de 2020?

## 🛠️ Tecnologias e Ferramentas
O projeto foi desenvolvido inteiramente em nuvem e Python:

* **Cloud Computing:** Google Cloud Platform (GCP).
* **Data Warehouse:** Google BigQuery (Armazenamento e consultas SQL).
* **Linguagem:** Python.
* **Bibliotecas de Análise:** `pandas`, `google-cloud-bigquery`.
* **Visualização de Dados:** `matplotlib`, `seaborn`.

## 🏗️ Arquitetura da Solução
O fluxo de dados seguiu uma esteira de Engenharia de Dados moderna:

1.  **Ingestão:** Dados brutos da PNAD (CSV) carregados no **Google Cloud Storage**.
2.  **Armazenamento:** Criação de tabelas e tratamento de dados no **Google BigQuery**.
3.  **Análise:** Conexão via Python para extração de insights e geração de relatórios.

```mermaid
graph LR
A[Dados PNAD/IBGE] -->|Upload| B(Google Cloud Storage)
B -->|Ingestão| C(Google BigQuery)
C -->|SQL + Python| D[Jupyter Notebook]
D -->|Insights| E[Relatório Executivo]
