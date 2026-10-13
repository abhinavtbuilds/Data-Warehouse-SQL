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

- SQL Server (T-SQL)
- Git / GitHub for version control

## 📖 Getting Started

1. Clone the repo
```bash
   git clone https://github.com/abhinavtbuilds/Data-Warehouse-SQL.git
```
2. Edit the `BULK INSERT` paths in `scripts/bronze/proc_load_bronze.sql` (they start with `/sql/datasets/`) so they point to the `datasets/` folder on your SQL Server host.
3. Run the scripts in this exact order:

   | Step | Script |
   |------|--------|
   | 1 | `scripts/init_database.sql` |
   | 2 | `scripts/bronze/ddl_bronze.sql` |
   | 3 | `scripts/bronze/proc_load_bronze.sql` |
   | 4 | `scripts/silver/ddl_silver.sql` |
   | 5 | `scripts/silver/proc_load_silver.sql` |
   | 6 | `scripts/gold/ddl_gold.sql` |

4. Check `docs/` for the data catalog and schema details.

## 📊 Source Data

Row counts of the raw CSV files in `datasets/` (excluding the header row):

| File | Source system | Rows |
|------|---------------|------|
| `source_crm/cust_info.csv` | CRM | 18,494 |
| `source_crm/prd_info.csv` | CRM | 397 |
| `source_crm/sales_details.csv` | CRM | 60,398 |
| `source_erp/CUST_AZ12.csv` | ERP | 18,484 |
| `source_erp/LOC_A101.csv` | ERP | 18,484 |
| `source_erp/PX_CAT_G1V2.csv` | ERP | 37 |

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
