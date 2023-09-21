# Data engineering on Microsoft Azure: Data Factory

This course is designed to prepare us for Microsoft Data Engineering on Azure **DP203** exam

*Azure Data Factory* – we need some mechanism to transform data into a usable format. ADF is a data integration service that is used to create automated data pipelines that can be used to copy & transform data.
ADF is Azure’s ETL & data integration services that allows users to create data-driven workflows for orchestrating data movement & transforming data at scale

*Workflow:* SSIS (SQL Server Integration Service)->ETL->Destination data->Power BI

Eg: A game company has a game which:
- Logs – azure data lake storage: Bigdata
- Customer info & market campaigns – On premises storage
- You want to analyze the logs with customer data & generate a meaningful report to find which modes are frequently used & which ads are frequently played.
We use ADF to extract, transform & load data to say Azure SQL which is then used in Power BI.

