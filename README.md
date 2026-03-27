airflow-pyspark-etl-salary-pipeline

📌 Project Overview
This project builds an end-to-end ETL pipeline to process employee salary data and identify employees earning above their department average. The pipeline uses PySpark for transformation and Apache Airflow for scheduling.

🎯 Problem Statement
Organizations often need to identify top-performing or highly paid employees for compensation analysis and business insights. This project solves that by calculating department-level averages and filtering employees earning above that threshold.

🏗 Architecture
Data Source → PySpark Transformation → Parquet Storage → Airflow Scheduling

⚙️ Tech Stack
Python
PySpark
Apache Airflow
SQL Concepts (Window Functions)
Parquet (columnar storage format)


▶️ How to Run

1. Install Dependencies
pip install -r requirements.txt
2. Run PySpark Job
python scripts/pyspark_job.py
3. Start Airflow
airflow standalone
4. Trigger Pipeline
Open Airflow UI
Enable DAG: salary_etl_pipeline
Trigger the DAG
📊 Data Transformation Logic
Partition data by department
Calculate average salary using window function
Filter employees with salary greater than department average

📈 Output
The transformed data is stored in:
output/above_avg_salary/
Spark will create it automatically when you run:
Python
.write.parquet("output/above_avg_salary")

Files generated:
Parquet data files
_SUCCESS indicator file


🧠 Key Learnings
Window functions in PySpark
ETL pipeline design
Scheduling with Airflow
Data storage using Parquet






