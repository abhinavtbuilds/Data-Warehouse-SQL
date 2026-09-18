# Data Warehouse SQL Project

A SQL-based data warehouse built to practice modern data engineering and analytics workflows — taking raw source data through cleansing and modeling into a business-ready analytical layer.

## 🏗️ Architecture

This project follows the **Medallion Architecture**, organizing data into three layers:

| Layer | Purpose |
|-------|---------|
| **Bronze** | Raw data ingested as-is from source systems (CSV files → database tables) |
| **Silver** | Cleansed, standardized, and normalized data, ready for transformation |
| **Gold** | Business-ready data modeled into a star schema for reporting and analytics |

## 📂 Repository Structure
Data-Warehouse-SQL/
│
├── datasets/ # Raw source data (e.g. ERP/CRM CSV files)
├── docs/ # Documentation — data catalog, architecture diagrams, naming conventions
├── scripts/ # SQL scripts for ETL and transformations (bronze → silver → gold)
├── tests/ # Data quality checks and validation scripts
├── LICENSE # MIT License
└── README.md # Project overview (this file)

## 🚀 Project Goals

- **Data Engineering:** Consolidate data from multiple source systems into a single, clean, analytics-ready warehouse.
- **Data Modeling:** Design fact and dimension tables using a star schema optimized for querying.
- **Analytics:** Write SQL queries to surface insights on things like customer behavior, product performance, and sales trends.

## 🛠️ Tools

- SQL (specify your engine — e.g. SQL Server, PostgreSQL, MySQL)
- Git / GitHub for version control

## 📖 Getting Started

1. Clone the repo
```bash
   git clone https://github.com/abhinavtbuilds/Data-Warehouse-SQL.git
```
2. Load the raw files from `datasets/` into your database.
3. Run the scripts in `scripts/` in order (bronze → silver → gold) to build out each layer.
4. Check `docs/` for the data catalog and schema details.

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
