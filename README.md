🧠 Mental Health App Data Pipeline & Analytics

(LePal.ai Inspired Project)

📖 Overview

This project simulates a data engineering pipeline for a mental health application, processing user sessions, therapy interactions, and engagement data to generate actionable insights.

It is inspired by my experience working with data and analytics workflows in mental health platforms, focusing on scalable data pipelines and user engagement analysis.

🎯 Problem Statement

Mental health platforms generate high-volume user interaction data (sessions, AI interactions, feedback). Without structured pipelines:

Data becomes inconsistent and unreliable
Engagement insights are unclear
AI-driven features cannot be effectively optimized

This project builds a scalable data pipeline to enable reliable analytics and data-driven decision-making.

🏗️ Architecture

Pipeline Flow:
App Events → Kafka → Airflow → Snowflake → Dashboard

Technologies Used:

Apache Kafka – Real-time data ingestion
Apache Airflow – Workflow orchestration
Snowflake – Data storage and analytics
Apache Spark – Data transformation
Power BI – Dashboard and reporting
🗂️ Data Model

The pipeline processes structured datasets representing:

Users
Therapy Sessions
Events (AI interactions, feature usage)
Providers
Feedback

Example Table:

sessions(session_id, user_id, provider_id, session_start, session_end, duration)
⚙️ Data Pipeline

The pipeline consists of the following steps:

Data Generation – Simulated user, session, and event data using Python
Data Ingestion – Streaming event data using Kafka
Workflow Orchestration – Scheduled ETL pipelines using Airflow
Data Transformation – Data cleaning and transformation using Spark
Data Storage – Structured data stored in Snowflake
Data Validation – Checks for missing values and data consistency
📊 Analytics Layer

Sample queries used to generate insights:

-- Daily Active Users
SELECT COUNT(DISTINCT user_id) AS dau
FROM sessions;

-- Average Session Duration
SELECT AVG(duration) AS avg_session_duration
FROM sessions;

-- Provider Activity
SELECT provider_id, COUNT(*) AS total_sessions
FROM sessions
GROUP BY provider_id;
📈 Key Insights
Identified user engagement trends across sessions
Analyzed session duration and activity patterns
Evaluated provider participation and activity levels
Simulated ~15% improvement in engagement using data-driven insights
🚀 Key Features
End-to-end ETL pipeline design
Real-time event data simulation
Scalable data modeling for user activity
Data validation and quality checks
Analytics-ready data warehouse
🗂️ Project Structure
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
⚡ How to Run
Generate sample data using Python scripts
Start Kafka producer to simulate event streaming
Trigger Airflow DAG for ETL processing
Load processed data into Snowflake
Execute SQL queries for analytics
Connect Power BI for dashboard visualization
📌 Note

This is a simulated project inspired by my experience contributing to data and insights workflows within a mental health application.

My focus was on data pipeline design, data validation, and analytics use cases, reflecting the responsibilities of working alongside backend, product, and analytics teams rather than building the entire system independently.
