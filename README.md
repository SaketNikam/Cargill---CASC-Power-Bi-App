# Cargill---CASC-Power-Bi-App
This is an overview for the CASC Power Bi App project I delivered during my tenure at Cargill.

CASC Power BI App – Centralized Analytics Hub  
The CASC Power BI App is a centralized reporting and analytics platform built for Cargill’s North American operations. This app consolidates over 20 interactive reports, streamlining access to key insights across various production metrics, operational KPIs, and compliance tracking.  

Project Overview  
This solution was designed to:  
Centralize all critical reports in a single Power BI App  
Enable data-driven decisions by operators, plant managers, and regional/global leads  
Enhance operational transparency across multiple facilities  
Reduce manual reporting efforts and support a self-service analytics culture  

Architecture Breakdown  
1. Data Ingestion Layer  
Sources include:  
Apache Impala – Primary operational database  
PI Server – Real-time sensor and production data  
Azure Data Lake Gen2 – Centralized storage of structured/unstructured raw data  

2. Data Transformation & Preparation  
Multiple technologies were used to transform, clean, and model data:  
Azure Databricks – For large-scale batch processing   
Azure Synapse Analytics – For developing data warehouses, querying and transformation  
Power BI Dataflows – Used to standardize reusable ETL logic for various data entities  
Power Query – In-report transformations for final shaping and KPI logic  

3. Analytics Layer  
The cleaned and modeled data feeds:  
Power BI Semantic Models – Star schemas built with DAX for performance and reusability (in alignment with Kimball methodology)  
Combined Power BI Dataflows – Integrated datasets reused across multiple reports  
Power BI Reports – 20+ customized reports and dashboards for plant performance, safety, procedures, HR, and alarms  

4. Consolidation Layer  
All assets are delivered through a centralized:  
Power BI App – A curated package of reports and dashboards, segmented by role and region, providing a consistent user experience and security model  

Key Features  
Dynamic KPI Monitoring – Track performance metrics like alarm rate, solvent loss, and HR metrics  
Power Automate Integration – Automated notifications to plant managers based on thresholds  
Governance-Friendly Structure – Standardized reporting templates and semantic model governance  

Security & Access Control  
Workspace roles defined by user groups (Operations, Regional Leads, Corporate)  
Row-Level Security (RLS) implemented via semantic models to restrict plant-level data views  
Controlled app access through Power BI Service with lifecycle management  

Technologies Used:  
Data Sources:	Apache Impala, PI Server, Azure Data Lake Gen2  
Transformation:	Azure Databricks, Synapse, Power BI Dataflows  
Analytics:	Power BI, DAX, Power BI Semantic Models  
Consolidation: Power BI App, Power Automate  

Future Enhancements  
Integrate predictive maintenance models using Azure ML  
Expand Scorecards for daily operational reviews  
Migrate backend processing to Microsoft Fabric for real-time performance  
