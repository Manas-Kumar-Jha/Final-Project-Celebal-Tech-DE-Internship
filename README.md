# Azure Data Engineering ETL Pipeline using Azure Data Factory & Databricks

## Project Overview

This project demonstrates the implementation of an end-to-end ETL (Extract, Transform, Load) pipeline using Microsoft Azure services and Azure Databricks. The objective is to build a scalable data engineering workflow that ingests raw CSV files, transforms the data into different processing layers, and generates analytical datasets for reporting.

The project follows the Medallion Architecture (Bronze, Silver, and Gold layers) to organize data processing and improve data quality.

## Project Architecture

Landing Layer → Bronze Layer → Silver Layer → Gold Layer → Reconciliation Layer

- **Landing Layer:** Stores raw CSV files.
- **Bronze Layer:** Performs raw data ingestion with metadata.
- **Silver Layer:** Cleans, validates, and transforms data.
- **Gold Layer:** Creates business-ready analytical tables.
- **Reconciliation Layer:** Validates record counts across layers.

## Technologies Used

- Microsoft Azure
- Azure Storage Account (Blob Storage)
- Azure Databricks
- Azure Data Factory
- Apache Spark
- PySpark
- Delta Lake
- Python

## Azure Resources

- Resource Group
- Azure Storage Account
- Azure Data Factory
- Azure Databricks Workspace

## Dataset

The project uses four CSV files:

- Customers
- Orders
- Order Items
- Inventory

These files are uploaded to the Landing container in Azure Blob Storage.

## ETL Workflow

### Landing Layer

- Uploaded source CSV files.
- Stored raw datasets in Azure Blob Storage.

### Bronze Layer

- Read raw CSV files from Landing.
- Added ingestion timestamp.
- Added source file information.
- Stored raw data as Delta tables.

### Silver Layer

- Cleaned missing values.
- Removed duplicate records.
- Standardized data formats.
- Validated records.
- Stored cleaned data in Delta format.

### Gold Layer

Generated business-ready datasets including:

- Sales by Region
- Orders by Status
- Customer Revenue Analysis
- Top Selling Products
- Warehouse Inventory Summary

### Reconciliation Layer

Performed validation by comparing record counts between processing layers to ensure data consistency.

## Pipeline Execution

Azure Data Factory is used to automate the complete ETL workflow.

Pipeline Process:

1. Connect Azure Data Factory with Azure Databricks.
2. Execute the Databricks notebook.
3. Process Landing, Bronze, Silver, Gold, and Reconciliation layers.
4. Complete the ETL pipeline successfully.


## Project Features

- End-to-End ETL Pipeline
- Medallion Architecture
- Delta Lake Implementation
- Automated Pipeline Execution
- Data Validation
- Record Count Reconciliation
- Scalable Data Processing


## Project Structure

```
Azure Data Engineering Project
│
├── Notebook
│   └── 01_Setup.ipynb
│
├── Dataset
│   ├── customers.csv
│   ├── orders.csv
│   ├── order_items.csv
│   └── inventory.csv
│
├── Screenshots
│   ├── Azure Resource Group
│   ├── Storage Account
│   ├── Landing Container
│   ├── ADF Pipeline Design
│   └── Pipeline Execution Success
│
└── README.md
```


## Output

The project successfully performs:

- Data ingestion
- Data transformation
- Data validation
- Delta table creation
- Business analytics generation
- Automated execution using Azure Data Factory


## Learning Outcomes

Through this project, the following concepts were implemented:

- Azure Data Factory Pipeline
- Azure Databricks Notebook Integration
- Azure Blob Storage
- Apache Spark
- PySpark Transformations
- Delta Lake
- ETL Pipeline Development
- Data Validation Techniques
- Medallion Architecture
- Cloud-based Data Engineering


Azure Data Engineering Project
