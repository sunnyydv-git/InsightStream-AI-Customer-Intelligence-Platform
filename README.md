# InsightStream

## AI-Powered Customer Intelligence Platform

InsightStream is a cloud-native customer intelligence platform built on AWS and Databricks.

The platform processes customer transactions, behavioral events, product interactions, and support data to generate analytical and machine-learning-driven customer insights.

## Objectives

InsightStream will demonstrate:

* Batch data engineering
* Near-real-time event streaming
* Lakehouse architecture
* PySpark data processing
* dbt analytical transformations
* Customer 360
* Churn prediction
* Customer segmentation
* Customer lifetime value prediction
* ML experiment tracking and model lifecycle management
* Real-time ML inference
* Generative AI customer intelligence
* AWS cloud architecture
* Infrastructure as Code
* CI/CD
* Data and ML monitoring

## Technology Stack

| Area           | Technology                      |
| -------------- | ------------------------------- |
| Cloud          | AWS                             |
| Storage        | Amazon S3                       |
| Lakehouse      | Databricks                      |
| Processing     | Apache Spark / PySpark          |
| Streaming      | Apache Kafka                    |
| Table Format   | Delta Lake                      |
| Transformation | dbt                             |
| ML             | Python / Scikit-learn / XGBoost |
| MLOps          | MLflow                          |
| GenAI          | Amazon Bedrock                  |
| BI             | Amazon QuickSight               |
| Infrastructure | Terraform                       |
| CI/CD          | GitHub Actions                  |

## Architecture

The platform will follow a Bronze → Silver → Gold lakehouse architecture.

Batch and streaming data will be ingested into the AWS data lake, processed through Databricks, transformed into analytical and ML-ready datasets, and consumed by ML and Generative AI workloads.

## Project Status

🚧 Phase 0 — Project Foundation

The project is being developed incrementally. Each module is implemented, tested, documented, and validated independently before integration.
