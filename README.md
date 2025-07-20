Azure Data Pipeline Assignment
This repository demonstrates the complete workflow for building an Azure Data Pipeline to automate the movement of CSV data from Azure Data Lake Storage into Azure SQL Database using Azure Data Factory. The project includes 9 supporting screenshots that visually document each main step.

Table of Contents
Project Overview

Screenshots

Process Steps

Repository Structure

How to Use

Contact

Project Overview
Goal: Seamlessly extract CSV files from an Azure Data Lake Storage container and load them into structured tables in Azure SQL Database through an automated Azure Data Factory pipeline.

Highlights:

Data upload to Azure Data Lake (rawfiles container)

Azure SQL Database and table creation

Setup of Data Factory with linked services and datasets

Design of Mapping Data Flows including derived columns and automatic truncation

Complete ETL orchestration

Screenshots
Below are the key screenshots included in this repository as step-by-step documentation:

#	Screenshot Filename	Description
1	adf-new-pipeline.png	Creating a new pipeline in Azure Data Factory
2	blob-uploaded-files.png	Verifying CSV file upload in Data Lake
3	data-flow.png	Building the Mapping Data Flow
4	dataset-cust-mstr.png	Dataset setup for CUST_MSTR input
5	dataset-h-ecom-order.png	Dataset setup for H_ECOM_ORDER input
6	dataset-master-child.png	Dataset setup for MASTER_CHILD input
7	final-pipeline.png	Overview of the configured ADF pipeline
8	linked-service-datalake.png	Linked service configuration: Data Lake
9	linked-service-sql.png	Linked service configuration: SQL Database
See the /screenshots/ folder for all images.

Process Steps
Upload CSV Files

Add all required CSVs to the rawfiles container in Azure Data Lake Storage.

Create Azure SQL Database

Provision the SQL database, configure firewall, and create necessary tables.

Set Up Azure Data Factory

Create a Data Factory instance in the same resource group.

Create Linked Services

Connect ADF to both Data Lake Storage and SQL Database.

Create Datasets

Define datasets for each file pattern in Data Lake and each destination SQL table.

Design Mapping Data Flows

Extract, transform, and map columns (including derived columns from filenames).

Configure and Run ETL Pipeline

Connect flows, set truncation options, publish all, and trigger execution.

Monitor & Verify

Check data loaded into SQL tables and reference screenshots for validation.
/
|-- screenshots/
|     |-- adf-new-pipeline.png
|     |-- blob-uploaded-files.png
|     |-- data-flow.png
|     |-- dataset-cust-mstr.png
|     |-- dataset-h-ecom-order.png
|     |-- dataset-master-child.png
|     |-- final-pipeline.png
|     |-- linked-service-datalake.png
|     |-- linked-service-sql.png
|
|-- README.md
|-- /docs
|-- /datafactory

