💻 Azure End-to-End Data Engineering Real-Time Project

This project is a complete data engineering pipeline solution designed to solve a practical business problem while enhancing hands-on learning with Azure services. 🚀

📌 Project Overview
![Project workflow](https://github.com/user-attachments/assets/c48058e7-d469-4878-bbe1-35a2d8dcc8a6)

This project builds a scalable data pipeline on Azure to extract, transform, and visualize customer and sales data. The goal is to generate actionable insights via a Power BI dashboard 📊 that highlights key performance indicators (KPIs) like gender distribution and product category sales.

📈 Business Requirements
The business needs clarity on how customer demographics (especially 👩‍🦰 gender) affect product purchases. Key deliverables:
1. 📊 Sales by Gender and Product Category
Dashboard showing total products sold, revenue, and customer gender split.
2. 🧮 Data Filtering
Filters for product category, gender, and date.
3. 🧑‍💻 User-Friendly Interface
Easy querying and exploration for stakeholders.

⚙ Solution Overview
To meet business needs, we designed the solution with these components:
1. Data Ingestion 🛠
Extract data from on-prem SQL Server 🗃
Load into Azure Data Lake Storage  via
Azure Data Factory 
2. Data Transformation 🔄
Use Azure Databricks  to clean and aggregate data
Structure it into:
🟤 Bronze (raw)
⚪ Silver (cleaned)
🟡 Gold (aggregated)
3. Data Loading & Reporting 📥📈
Load gold data into Azure Synapse Analytics 
Create dashboards using Power BI 
4. Automation ⏱
Schedule daily runs using ADF triggers
Keep dashboards always updated 🔄

🧰 Technology Stack
Tool/Service	Purpose
 Azure Data Factory	Data ingestion & orchestration
 Azure Data Lake Storage	Raw & transformed data storage
 Azure Databricks	Data transformation & ETL
 Azure Synapse Analytics	Data warehouse & reporting layer
 Power BI	Dashboards & data visualization
🔐 Azure Key Vault	Manage credentials/secrets
🗃 SQL Server (On-Prem)	Source database

⚒ Setup Instructions
🔑 Prerequisites
Azure account with sufficient credits 💳
Access to SQL Server (on-prem)

🔷 Step 1: Azure Environment Setup
1. 🔧 Create Resource Group in Azure
2. 🚀 Provision resources:
Azure Data Factory
Azure Data Lake with containers: bronze, silver, gold
Azure Databricks & Synapse
Azure Key Vault

🛠 Step 2: Data Ingestion
1. ⚙ Install SQL Server & SSMS
2. ♻ Ingest tables from AdventureWorks DB using ADF into the bronze layer

🔁 Step 3: Data Transformation
1. 📂 Mount ADLS in Databricks
2. 🧹 Clean, transform, and move data through:
bronze ➡ silver ➡ gold

📦 Step 4: Data Loading & Reporting
1. 🔄 Load gold data into Synapse SQL pool
2. 📊 Build Power BI report with filters:
Product Category
Gender
Date

⏰ Step 5: Automation & Monitoring
1. 🗓 Schedule pipelines with ADF
2. 📈 Use built-in monitoring for failures, retries, and alerting

🔐 Step 6: Security & Governance
1. 👥 Setup RBAC with Azure Active Directory
2. 🔑 Store credentials & secrets in Azure Key Vault

✅ Step 7: End-to-End Testing
1. 🔃 Insert new records into SQL DB
2. 📈 Ensure the pipeline updates the Power BI dashboard automatically

🏁 Conclusion
This Azure-based pipeline gives a real-time, automated solution to uncover insights from sales and customer data. Stakeholders get dynamic reports, filtered by relevant dimensions, updated daily through a secure and scalable setup.


This project provides a robust end-to-end solution for understanding customer demographics and their impact on sales. The automated data pipeline ensures that stakeholders always have access to the most current and actionable insights.
