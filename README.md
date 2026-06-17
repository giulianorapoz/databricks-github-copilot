# Training: Databricks + GitHub Copilot in everyday life

## Overview

This training introduces the integration between Databricks and GitHub Copilot, with a practical focus on how these tools can accelerate the development of data pipelines, optimize code, and increase the productivity of data engineering teams.

---

## Agenda


### SQL Warehouse Serverless (40 min)
- Setup the SQL Warehouse serverless 2X-Small
- Integration VS Code + Databricks SQL
- ETL Exercise in SQL: Extraction, Cleansing, and the Gold Layer

---

## Repository Structure

```
databricks-treinner/
├── README.md                          # This file
├── docs/
│   ├── 01_setup_guide.md              # Environment setup guide
│   ├── 02_databricks_concepts.md      # Key Databricks concepts
│   └── 03_copilot_tips.md             # Copilot usage tips
├── notebooks/
│   └── 01_sql_warehouse_serverless/
│       ├── 01_sql_setup_and_extract.sql # Bronze SQL in a serverless warehouse
│       ├── 02_sql_cleaning_etl.sql      # Silver cleaning and ETL in SQL
│       └── 03_sql_gold_validation.sql   # Gold SQL and validations
├── data/
│   ├── raw/                           # Example raw data
│   └── processed/                     # Processed data
└── scripts/
    └── generate_sample_data.py        # Script to generate sample data
```

---

## ▶️ Choose Your Path and Get Started Now

> How it works: click on "Open Codespace" to prepare the environment, then click on "Start Path" to create the Issue with the guided steps. Each commit in the notebooks automatically advances the Issue to the next step.

--- 

### 🧪 SQL Warehouse Serverless (Conta Free)
> Perform a full ETL using only SQL Warehouse serverless 2X-Small.

<p>
  <a href="https://codespaces.new/RDMotta/skill-databricks?quickstart=1">
    <img src="https://github.com/codespaces/badge.svg" alt="Abrir Codespace"/>
  </a>
  &nbsp;
  <a href="https://github.com/RDMotta/skill-databricks/actions/workflows/start-track1.yml">
    <img src="https://img.shields.io/badge/Iniciar_Trilha-SQL_Serverless_Free-fb8500?style=for-the-badge" alt="Iniciar Trilha 4"/>
  </a>
</p>

---  

Codespace comes pre-configured with:

- ☕ Java 11 + PySpark 3.5.1 + Delta Lake (via pip, no binary download)
- 🐍 Python 3.12
- 🔧 Databricks CLI
- 🔌 Databricks Connect
- ⚡ GitHub Copilot + Copilot Chat
- 🗄️ Databricks Extension for VS Code
- 📊 Jupyter Notebook support
  
#Set up Credentials in Codespaces
Before you open the Codespace, configure the secrets in: github.com → Settings → Codespaces → New secret

| Secret | Valor |
|--------|-------|
| `DATABRICKS_HOST` | `https://community.cloud.databricks.com` |
| `DATABRICKS_TOKEN` | Token generation in Settings → Developer → Access Tokens |
| `DATABRICKS_CLUSTER_ID` | ID of the cluster created in Databricks |

---

## Prerequisites (Local Installation)

If you prefer to run locally instead of Codespaces:

- [Databricks Free Edition](https://login.databricks.com/?dbx_source=docs&intent=CE_SIGN_UP)
- VS Code install
- Extension [Databricks for VS Code](https://marketplace.visualstudio.com/items?itemName=databricks.databricks)
- GitHub Copilot (active license or trial)
- Python 3.12+ or Java 11+

---

## How to use this repository

### Via Codespaces (Recomendado)
1. Open the repository on GitHub Codespaces (button above)
2. Configuration of secrets `DATABRICKS_HOST`, `DATABRICKS_TOKEN` e `DATABRICKS_CLUSTER_ID`
3. The environment will be set up automaticall
4. Execute `make generate-data && make upload-data` Run to prepare the data
5. Follow the Issue-guided training created by the workflow `01-training-start`

### Via Local Installation
1. Follow the [Setup Guide](docs/01_setup_guide.md) to set up your environment
2. Copy `.env.example` to `.env` and fill in your credentials 
3. Execute `make setup && make generate-data`
4. Import the notebooks in the order indicated by the modules
5. Run each cell and practice with Copilot enabled

---

## Links

- [Databricks Free Edition](https://docs.databricks.com/aws/en/getting-started/free-edition)
- [Documentação Databricks](https://docs.databricks.com/)
- [GitHub Copilot Docs](https://docs.github.com/en/copilot)
- [Extensão Databricks VS Code](https://docs.databricks.com/dev-tools/vs-code-ext.html)
- [Delta Lake](https://delta.io/)
