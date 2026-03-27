# AdventureWorks Fabric Analytics

End-to-end analytics project built on Microsoft Fabric using the AdventureWorks OLTP database (2019, 2022, 2025).

## Architecture

This project follows the Medallion architecture pattern (Bronze → Silver → Gold) on Microsoft Fabric, with Power BI reports connected to a Semantic Model.
```
Source (SQL Server)
    └── Bronze Lakehouse (raw parquet)
        └── Silver Lakehouse (cleaned Delta tables)
            └── Gold Lakehouse (star schema)
                └── Semantic Model (DAX measures)
                    └── Power BI Reports
```

## Dashboards

| Dashboard | Description |
|---|---|
| Sales & Revenue | Revenue trends, top customers, sales by territory |
| Inventory & Production | Stock levels, work orders, product performance |
| Historical Comparison | Year-over-year analysis 2019 vs 2022 vs 2025 |

## Project Structure
```
├── notebooks/          # PySpark notebooks (Bronze → Silver → Gold)
├── reports/            # Power BI report files (.pbip)
├── docs/               # Architecture and data dictionary
├── scripts/            # Local utility scripts
└── data/               # Sample data and schemas
```

## Tech Stack

- Microsoft Fabric (Lakehouse, Notebooks, Data Pipeline, Semantic Model)
- Power BI Desktop
- PySpark / Python
- Delta Lake
- GitHub (version control + Fabric Git Integration)

## Data Source

[AdventureWorks sample databases](https://learn.microsoft.com/en-us/sql/samples/adventureworks-install-configure) — 2019, 2022, 2025 versions.