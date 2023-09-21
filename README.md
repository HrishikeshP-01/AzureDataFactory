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

## Why ADF?
- Easy for big data
- Cloud based service for complex hybrid ETL & data integration

## Some ADF Concepts
- *Pipeline* – A logical group of activities that performs some work
- *Activity* – an individual processing step in the pipeline
- *Linked Services* – Define the connection information needed for ADF to connect to external resources. They are like connection strings.
- *Datasets* – The data used in your activities. They represent the data structures within data stores that point to/reference the data you want to use.
- *ADF Triggers* – Allows us to define when data pipelines run in ADF

## Different tools to work with ADF:
- Azure Portal
- Azure PowerShell
- .NET
- Python
- REST
- Resource Manager Template (Azure PowerShell Az Module) – They are json files with pre-defined values that are used to create ADF

## Data pipelines & pipeline runs
*A trigger fires a pipeline run.*

*Pipeline run* – a single execution of a pipeline. A single batch of values are loaded from the source, transformed as needed and then stored in a target/sink data source

Each pipeline run has a unique pipeline ID
#### A pipeline can be triggered in 2 ways:
1. *On-demand execution* – With a button click in the UI we can manually force the immediate creation & execution of a new pipeline. This is done either for one-off pipelines or for debugging purposes.
2. *Triggered execution* – a new pipeline run is created & executed each time a trigger is fired.
