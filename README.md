**Airline Data Ingestion Pipeline using AWS**
----------------------------------------------------


This project demonstrates a **real-time data ingestion** and processing pipeline for airline flight data using AWS cloud services.
It simulates the arrival of daily flight data into an AWS S3-based data lake and automates the ingestion, transformation, and loading (ETL) into Amazon Redshift for analysis.


**Project Overview**
-------------------------------


**Project Name**: Airline Data Ingestion

**Goal**: Automate ingestion of airline flight data and build an ETL pipeline using AWS.

**Use Case**: Learning project simulating real-time airline data ingestion, processing, and warehousing for analysis.

**Tech Stack**
-----------------
Languages: Python, SQL


 **AWS Services Used**
 -------------------------

| Service          | Purpose                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Amazon S3**     | Acts as a data lake; stores raw flight data in Hive-style partitions.   |
| **Amazon EventBridge** | Triggers orchestration on file arrival in S3.                      |
| **AWS Step Functions** | Orchestrates the pipeline from EventBridge to Glue and beyond.     |
| **AWS Glue**      | Crawls S3 data and transforms it using a Glue job.                      |
| **Amazon Redshift** | Stores processed data for analytics and reporting.                    |
| **Amazon SNS**     | Sends notifications on Glue job success/failure.                       |

 **Pipeline Flow**
 ------------------

 ```plaintext
S3 (daily CSV files) 
   ↓
Amazon EventBridge (file trigger)
   ↓
AWS Step Functions (orchestration)
   ↓
AWS Glue (crawler + job)
   ↓ success → Amazon Redshift (warehouse)
   ↓ failure → Amazon SNS (alert)

```

 **Project Outcome**
 ------------------------

- Built a working ETL pipeline using AWS services.
- Automatically processes airline data on a daily basis.
- Demonstrated the use of AWS native services for serverless data engineering.
- Sends real-time notifications if the ETL process fails.

**Learning Purpose**
---------------------------
This project was built for educational purposes to understand :-
- Serverless data orchestration
- Data lake and warehouse integration
- Event-driven architecture using AWS


