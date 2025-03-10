# ETL Pipeline for Retail Sales Data

 📌 Project Overview
 
This project builds an  (Extract, Transform, Load) Pipeline to automate sales data processing and store it in AWS Redshift. The pipeline handles:
- Extracting sales data from CSV files & API sources.
- Transforming data (cleaning, handling duplicates, formatting).
- Loading data into **AWS Redshift** for real-time analysis.

Built using Python, Pandas, AWS Redshift, and SQL, this pipeline automates retail data workflows.


 📌 Technologies Used
 
✅ Python (Pandas, Requests)
✅ AWS Redshift (Data Warehouse)
✅ SQL (Data Processing & Queries)
✅ Boto3 (AWS SDK for Python)



📌 Installation & Setup

1️⃣ Install Dependencies
bash
pip install pandas requests psycopg2 boto3


2️⃣ Update AWS Redshift Credentials 

- Create a **Redshift Cluster** in AWS.
- Retrieve **Host, DB Name, User, Password** and update in etl_pipeline_retail.py
python
REDSHIFT_HOST = "your-redshift-cluster.amazonaws.com"
REDSHIFT_DB = "retail_db"
REDSHIFT_USER = "admin"
REDSHIFT_PASSWORD = "your-password"
REDSHIFT_PORT = 5439


3️⃣ Run the ETL Pipeline Locally
bash
python etl_pipeline_retail.py



📌 Usage & API Endpoints

Pipeline Workflow
✅ Extract: Reads data from CSV & API.
✅ Transform: Cleans and processes data.
✅ Load:Stores processed data into AWS Redshift.

To verify, run the following SQL query in Redshift:
sql
SELECT * FROM sales LIMIT 10;



 📌 Deployment Guide 
 
Option 1: Deploy as an AWS Lambda Function
1️⃣ Install required packages:
bash
pip install serverless-wsgi pandas requests psycopg2 boto3

2️⃣ Deploy using AWS CLI:
bash
sls deploy


