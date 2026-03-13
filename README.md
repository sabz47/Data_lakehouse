#  Bike Company Data Lakehouse Project

This project demonstrates the implementation of a modern **Data Lakehouse architecture** for a bike company using **Databricks, SQL, and Python**.

The objective of this project is to design a scalable data platform that can ingest raw data from multiple sources, transform it into high‑quality structured datasets, and make it ready for business analytics and reporting.

To achieve this, the project follows the **Medallion Architecture (Bronze → Silver → Gold)**, which is a widely used architecture pattern in modern data platforms.

The system ensures:  
- Reliable data ingestion  
- Data quality and consistency  
- Scalable transformations  
- Analytics‑ready datasets for BI tools  

---

## **1. Bronze Layer – Raw Data Ingestion**

The Bronze layer contains raw data ingested directly from source systems.

Sources may include:  
- CRM systems  
- ERP systems  
- Transactional databases  
- CSV / external data files  

**Characteristics of this layer:**  
- Data is stored as‑is with no transformation  
- Maintains historical raw data  
- Provides data traceability  
- Serves as the single source of truth  

The Bronze layer allows reprocessing of data if transformation logic changes in later stages.

---

## **2. Silver Layer – Data Cleaning and Transformation**

The Silver layer focuses on data quality improvement and transformation.  
In this stage, the raw data from the Bronze layer is processed to create clean, standardized, and structured datasets.

**Key operations performed:**  
- Data cleaning  
- Data type casting  
- Data standardization  
- Data validation  

The goal of this layer is to produce reliable datasets with high quality that can be safely used for business analysis.

---

## **3. Gold Layer – Analytics‑Ready Data**

The Gold layer contains analytics‑ready datasets.

In this layer, business logic and aggregation rules are applied to transform the cleaned Silver data into business‑friendly models.

This layer is designed to support:  
- Business intelligence dashboards  
- Data analytics  
- Reporting tools such as Power BI or Tableau  

Data in this layer is typically modeled using dimensional modeling techniques such as **fact and dimension tables**, followed by a **star schema**.

---
