# E-Commerce Data Pipeline & Dashboard

## Overview
This project demonstrates an end-to-end data pipeline for an online store system, from data ingestion to visualization. The pipeline processes raw data and transforms it into meaningful insights using modern data engineering tools.

---

## Tools Used
- PySpark
- Azure Data Factory
- Azure Databricks
- Delta Lake (Medallion Architecture)
- Azure SQL Database
- Power BI

---

## Project Flow

### 1. Data Ingestion (Bronze Layer)
- Source: JSON data (Products, Carts)
- Loaded raw data into Data Lake using Azure Data Factory
- Stored as-is in .json format

### 2. Data Transformation (Silver Layer)
- Cleaned and structured data using PySpark
- Exploded nested JSON fields (e.g., carts, products)
- Removed duplicates and handled missing values

### 3. Data Aggregation (Gold Layer)
Created business-level tables:
- `gold_category_quantity` → Total quantity per category  
- `gold_category_revenue` → Revenue per category  
- `gold_daily_revenue` → Daily revenue trend  
- `gold_top_products` → Top performing products  

---

## Dashboard (Power BI)
Built an interactive dashboard with:
- KPI Cards (Total Revenue, Total Quantity)
- Category-wise Revenue & Quantity Charts
- Daily Revenue Trend
- Top Products Analysis

---

## Key Features
- End-to-end ETL pipeline
- Medallion Architecture (Bronze → Silver → Gold)
- Scalable data processing using PySpark
- Interactive business insights using Power BI

---

## Learnings
- Data pipeline design and implementation
- Handling nested JSON data
- Data transformation using PySpark
- Data visualization best practices

---

## Project Structure

```
E-Commerce-Data-Pipeline/
│
├── notebooks/
│   ├── bronze_ingestion.ipynb
│   ├── silver_transformation.ipynb
│   └── gold_aggregation.ipynb
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── curated/
│
├── powerbi/
│   └── Ecommerce Dashboard.pbix
│
└── README.md
```

---

## Conclusion
This project showcases how raw data can be transformed into actionable insights using modern data engineering and visualization tools.
