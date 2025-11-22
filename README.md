# Data Warehouse Project

A production-grade data warehouse built using the Medallion Architecture (Bronze-Silver-Gold layers) to transform raw sales data from multiple source systems into business-ready insights.

This project demonstrates end-to-end data engineering and analytics skills—from designing scalable data architecture to delivering actionable business intelligence.

---

## Project Overview
This repository showcases:
1. **Data Architecture:** Designed a modern data warehouse using the Medallion Architecture (Bronze, Silver, Gold layers)
2. **ETL Pipelines:** Built automated pipelines to extract, transform, and load data from CRM and ERP systems
3. **Data Modelling:** Developed a Star Schema optimized for fast analytical queries
4. **Data Quality Management:** Implemented comprehensive data validation, cleansing, and error handling
5. **Analytics & Reporting:** Created SQL-based analytics to deliver insights on sales trends, customer behavior, and product performance

---

## 🏗️ Architecture: Medallion (Bronze-Silver-Gold)

The data architecture for the project follows the Medallion Architecture Bronze, Silver, and Gold layers.

![Data Architecture](https://github.com/The-DataMaven/sql-data-warehouse-project/blob/4831ced1e5dcb7f38d8119c407257fce3a855d43/docs/data_architecture.png)

1. **Bronze Layer: Raw Data Storage**
  - **Purpose:** Store raw, unprocessed data exactly as received from source systems
  - **Method:** Bulk insert from CSV files into SQL Server
  - **Key Features:**
    - No transformations applied
    - Full data traceability
    - Source of truth for debugging
2. **Silver Layer: Cleaned & Standardized Data** 
  - **Purpose:** Transform raw data into clean, reliable datasets
  - **Transformations Applied:**
    - Removed duplicates using ROW_NUMBER() window function
    - Standardized inconsistent values using CASE statements
    - Handled missing data (NULLs, empty strings, invalid dates)
    - Trimmed unwanted spaces with TRIM()
    - Applied business rules and derived calculated columns
    - Implemented error handling with TRY-CATCH blocks
  - **Data Volume:** 116,000+ rows cleaned across 6 tables
  - **Result:** Reliable foundation for downstream analytics
3.  **Gold Layer:**
  - **Purpose:** Provide optimized data models for reporting and dashboards
  - **Data Model:** Star Schema
    - Fact Table: fact_sales (transactional sales data)
    - Dimension Tables: dim_customers, dim_products (descriptive attributes)
  - **Key Features:**
    - Views (not physical tables) for real-time data freshness
    - Surrogate keys for stable identifiers
    - Optimized for fast analytical queries
    - Simple joins for business users

---

## 🛠️ Technologies Used

- **Database:** SQL Server
- **Languages:** SQL (Advanced)
- **Tools:** SQL Server Management Studio, Draw.io (data modeling), Git (version control)
- **Key SQL Techniques:**
  - Window functions (ROW_NUMBER(), RANK())
  - CTEs (Common Table Expressions)
  - CASE statements for data standardization
  - TRY-CATCH error handling
  - Bulk insert operations
  - Views for real-time data access

---

## ⭐ About Me

Hi! I'm Jennifer Joseph, a Data Analyst passionate about transforming raw data into insights that drive business decisions and creates positive change.

**Connect with me:**

[LinkedIn](https://www.linkedin.com/in/jenniferjoseph-data/) | [Email](jennyashaeziembu@gmail.com)

---

## License
This project is open-source and available under the MIT License.
