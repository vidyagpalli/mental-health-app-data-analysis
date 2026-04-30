# Mental Health App Data Pipeline & Analytics (Kafka + Airflow + Snowflake)
## Project LePal Overview
This project simulates a data engineering pipeline for a mental health app, processing user sessions and engagement data to generate actionable insights.
Built using Kafka, Airflow, Snowflake, and Spark.
## Problem Statement
Mental health platforms generate high-volume user interaction data, but without structured pipelines:

- Data becomes inconsistent
- Engagement insights are unclear
- AI features cannot be optimized

This project builds a scalable pipeline to solve these challenges.
## Architecture
Pipeline Flow:
App Events → Kafka → Airflow → Snowflake → Dashboard

Technologies Used:
Apache Kafka – Real-time data ingestion
Apache Airflow – Workflow orchestration
Snowflake – Data storage and analytics
Apache Spark – Data transformation
Power BI – Dashboard and reporting

## Data Model
The pipeline processes structured datasets representing:
Users
Therapy Sessions
Events (AI interactions, feature usage)
Providers
Feedback

Example Table:
sessions(session_id, user_id, provider_id, session_start, session_end, duration)

## Data Pipeline
The pipeline consists of the following steps:

1. Data Generation
Simulated user, session, and event data using Python
2. Data Ingestion
Streaming event data using Kafka
3. Workflow Orchestration
Scheduled ETL pipelines using Airflow
4. Data Transformation
Data cleaning and transformation using Spark
5. Data Storage
Structured data stored in Snowflake
6. Data Validation
Implemented checks for missing values and data consistency

## Analytics Layer

Sample analytics queries used to generate insights:

### Daily Active Users
SELECT COUNT(DISTINCT user_id) AS dau
FROM sessions;

### Average Session Duration
SELECT AVG(duration) AS avg_session_duration
FROM sessions;

### Provider Activity
SELECT provider_id, COUNT(*) AS total_sessions
FROM sessions
GROUP BY provider_id;

## Key Insights
```bash
-> Identified user engagement trends across sessions
-> Analyzed session duration and activity patterns
-> Evaluated provider participation and activity levels
-> Simulated data-driven improvements in user engagement (~15%)
```

## Key Features
```bash
. End-to-end ETL pipeline design
. Real-time event data simulation
. Scalable data modeling for user activity
. Data validation and quality checks
. Analytics-ready data warehouse
```

## 🗂️ Project Structure

```bash
mental-health-data-pipeline/
│
├── data/
├── scripts/
│   ├── data_generator.py
│   ├── kafka_producer.py
│
├── airflow/
│   └── dag_pipeline.py
│
├── spark/
│   └── transform.py
│
├── sql/
│   ├── tables.sql
│   ├── analytics.sql
│
├── dashboard/
│   └── screenshots/
│
└── README.md
```

## How to Run
1. Generate sample data using Python scripts
2. Start Kafka producer to simulate event streaming
3. Trigger Airflow DAG for ETL processing
4. Load processed data into Snowflake
5. Execute SQL queries for analytics
6. Connect Power BI for dashboard visualization

## 📌 Note
This is a simulated project inspired by my experience contributing to data and insights workflows within a mental health application. 
My focus was on data pipeline design, data validation, and analytics use cases, reflecting the responsibilities of working alongside backend, product, and analytics teams rather than building the entire system independently.
