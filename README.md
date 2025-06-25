# Portfolio
Projects 1 and 2
Project Description: Descriptive Analysis of the City of Vancouver’s Open Data log.
Project Title: Understanding Changes in Vancouver’s Open Data Log and Implementing a Secure Cloud-Based Data Pipeline.
Objective: To conduct a descriptive analysis of changes in the City of Vancouver's Open Data Catalogue (2010–2024) and build a fully-functional, secure ETL pipeline on AWS for ingesting, cleaning, cataloging, and monitoring open data, providing insights into data transparency and infrastructure maturity over time.
Dataset: The dataset includes transactional data from Open Data Log over the past year, containing the following key features:
Source: City of Vancouver Open Data Change Log
Fields include:
•	Year of change
•	Count and type of change
•	Metadata such as dataset name, change description, and timestamp
•	Period Covered: 2010–2024
Methodology:
1-	Data Collection & Ingestion:
•	Downloaded Change Log datasets from the City’s portal.
•	Uploaded raw files to an S3 bucket (‘van raw man’) built in a secure VPC.

2-	Data Profiling & Cleaning:
•	Used AWS Glue DataBrew to profile the dataset (checking for missing values, duplicates, data types).
•	Created transformation recipes to clean, standardize, and output to Parquet (system folder) and CSV (user folder) formats.
3-	Cataloging & ETL Workflow:
•	Employed AWS Glue Crawler to detect schema and generate catalog tables for Athena queries.
•	Set up AWS Glue ETL jobs for full data pipeline: ingestion - transformation - output.
4-	Security, Governance & Monitoring:
•	Enabled AWS KMS customer-managed keys for bucket encryption and versioning.
•	Configured cross-bucket replication for resilience.
•	Implemented data governance via passed/failed record folders based on Glue data quality rules.
•	Deployed CloudTrail for auditing API usage and CloudWatch dashboards (BucketSizeBytes, Glue/job metrics) for monitoring and alerting.

5-	Evaluation & Cost Optimization:
•	Critically assessed the implementation using AWS Well-Architected Framework: Operational Excellence, Security, Reliability, Performance, and Cost efficiency.
•	Estimated annual cost using AWS Pricing Calculator, demonstrating cost-effectiveness.
Tools and Technologies:
S3, Glue data brew, Glue Crawler, Glue ETL, Athena, CloudTrail, CloudWatch, Athena SQL, AWS Calculator.
Deliverables:
•	Secure, cloud-based ETL pipeline using AWS services.
•	Data quality governance framework with passed/failed data segregation.
•	Interactive dashboards in QuickSight/Athena.
•	Cost analysis document demonstrating minimal annual cost 
