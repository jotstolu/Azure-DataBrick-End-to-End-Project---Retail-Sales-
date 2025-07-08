# 🛍️ Retail Orders End-to-End Data Pipeline using Azure & Databricks

This project demonstrates the development of a scalable end-to-end data pipeline for processing and reporting retail order data using **Azure Cloud services**, **Delta Lake architecture**, and **Databricks**.

## 🚀 Project Overview

The project automates data ingestion, transformation, and consumption for a retail system. The final output is made available for downstream analytics in Power BI.

The architecture leverages:

- **Azure Data Factory**: For orchestrating ingestion from GitHub and storing raw data in **Azure Data Lake Gen2**.
- **Databricks & Delta Live Tables**: For creating multi-layered data pipelines (Bronze, Silver, Gold) using PySpark notebooks.
- **Power BI**: For reporting and visualization.
- **GitHub**: As the source repository for ingestion and version control.

### 🗺️ Architecture

![Retail Data Architecture](./retail%20data%20architecture.dra.png)

## 🔁 Pipeline Workflow

The Databricks workflow is orchestrated as shown below:

![Databricks Workflow Pipeline](https://github.com/jotstolu/Azure-DataBrick-End-to-End-Project---Retail-Sales-/blob/main/asset/databricks%20workflow%20pipeline.png?raw=true)

### 🔹 Stages in the Pipeline

| Layer     | Description |
|-----------|-------------|
| **Lookup** | Initial lookup data load |
| **Bronze** | Raw ingestion using AutoLoader |
| **Silver** | Cleansed and filtered data tables (Customers, Orders, Products) |
| **Gold**   | Curated business-ready dimension and fact tables |
| **Fact**   | Star schema constructed for analytical reporting |

## 📂 Project Structure

The notebooks follow the **medallion architecture**:

```
retail_orders/
├── lookup Notebook.python
├── Bronze Layer.python
├── Silver_Customers.python
├── Silver_Orders.python
├── Silver_Products.python
├── Silver_Regions.python
├── Gold_Customers.python
├── Gold_Products.python
├── Gold Orders.python


```

## 🧪 Technologies Used

- **Azure Data Factory**: Orchestration
- **Azure Data Lake Storage Gen2**: Data storage layer
- **Databricks & Spark (Delta Live Tables)**: Data transformation
- **Power BI**: Visualization and reporting
- **Delta Lake**: Storage format for time travel, versioning
- **GitHub**: CI/CD & source control

## 📊 Output

The final **Gold Layer** tables and **Fact_Orders** are pushed to Power BI for analysis. The star schema ensures performance optimization for downstream consumers and reporting tools.

## 🧾 How to Run Locally (on Databricks)

1. Import the `.dbc` archive into your Databricks workspace.
2. Set up the workflows as shown in the pipeline image.
3. Configure your **Azure Data Lake Gen2** and GitHub connectors.
4. Trigger the pipeline manually or via job scheduler.

## ✅ Key Highlights

- Fully orchestrated and automated data pipeline
- Delta Live Tables for scalable processing
- Adheres to Medallion architecture (Bronze → Silver → Gold)
- Seamless integration from ingestion to visualization
