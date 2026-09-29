# 🎬 Netflix Data Analytics — dbt + Snowflake

An end-to-end analytics engineering project that transforms raw Netflix data into clean, tested, analytics-ready models using **dbt** and **Snowflake**.

Originally built by following a dbt tutorial course, then extended with [list your own additions here — e.g. "an additional revenue-by-genre mart model and custom data tests"].

## 🏗️ Architecture

Raw Netflix data (Snowflake RAW schema)
        │
        ▼
   Staging models (cleaned, renamed, typed)
        │
        ▼
  Intermediate models (business logic)
        │
        ▼
   Mart models (analytics-ready, tested)

## 🛠️ Tech Stack

- **Warehouse:** Snowflake (databases, schemas, warehouses, roles)
- **Transformation:** dbt (data build tool)
- **Language:** SQL, Jinja
- **Version control:** Git / GitHub

## 📁 Project Structure

netflix/
├── models/
│   ├── staging/       # Cleaned, standardized source data
│   ├── intermediate/  # Business logic transformations
│   └── marts/         # Final analytics-ready tables
├── tests/             # Custom data tests
├── macros/            # Reusable Jinja macros
├── seeds/             # Static reference data
└── dbt_project.yml

## ✅ Data Quality

This project uses dbt tests to enforce data quality, including:
- `not_null` and `unique` tests on primary keys
- `relationships` tests between fact and dimension models
- [Add any custom singular tests you wrote]

## 📊 Sample Insight

[One or two sentences on something the data showed — e.g. "Content added to Netflix peaked in 2019, with a notable shift toward TV shows over films after 2020."]

## 📄 Documentation

Full dbt-generated documentation (model lineage, column descriptions, test coverage) is published here:
👉 **[Live dbt docs](your-github-pages-link-here)**

## 🚀 Running This Project

1. Clone the repo and `cd netflix`
2. Install dependencies: `pip install dbt-snowflake`
3. Configure your Snowflake connection in `profiles.yml` (not committed — use environment variables for credentials)
4. Run `dbt deps` to install packages
5. Run `dbt build` to run models and tests
6. Run `dbt docs generate && dbt docs serve` to view documentation locally

## 🙋 About This Project

Built by [Muhammad Shaaf](https://github.com/MuhammadShaaf) as part of learning analytics engineering. Part of a broader portfolio including a [SQL Server data warehouse project](https://github.com/MuhammadShaaf/SQL-Data-Warehouse-Project).
