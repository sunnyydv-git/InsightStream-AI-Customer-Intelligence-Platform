# InsightStream — Claude Code Instructions

## Project

InsightStream is an AI-powered customer intelligence platform designed to demonstrate production-oriented Data Engineering, Machine Learning, MLOps, and Generative AI on AWS and Databricks.

The platform processes batch and near-real-time customer data to produce:

* Customer 360 datasets
* Behavioral analytics
* Churn predictions
* Customer segments
* Customer lifetime value predictions
* AI-generated customer insights and retention recommendations

## Core Architecture

Primary technologies:

* AWS S3 — cloud object storage / data lake
* Databricks on AWS — lakehouse, Spark processing, SQL, ML
* Apache Spark / PySpark — large-scale data processing
* Apache Kafka — customer event streaming
* Delta Lake — transactional lakehouse storage
* dbt — analytical transformations and testing
* MLflow — ML experiment tracking and model lifecycle
* Amazon Bedrock — Generative AI layer
* Amazon QuickSight — business analytics / dashboards
* Terraform — infrastructure as code
* GitHub Actions — CI/CD

Redshift is NOT part of the architecture.

## Engineering Principles

1. Build modules independently before integrating them.
2. Prefer simple, understandable implementations over unnecessary complexity.
3. Do not introduce AWS services without a clear architectural reason.
4. Do not add technologies merely to make the project look impressive.
5. Production-oriented code should be modular, testable, configurable, and documented.
6. Keep business logic separate from infrastructure/configuration.
7. Never hardcode credentials, secrets, API keys, bucket names, or environment-specific values.
8. Use environment variables or configuration files for environment-specific settings.
9. Add tests for important business logic.
10. Do not silently change the architecture or repository structure.
11. Before making a significant architectural change, explain the reason and wait for approval.
12. Do not implement future modules unless explicitly requested.

## Development Workflow

For every module:

1. Understand the requirements.
2. Inspect the existing repository.
3. Propose the implementation.
4. Implement only the requested module.
5. Add appropriate tests.
6. Run tests and validation.
7. Report what changed.
8. Report how the implementation was verified.
9. Identify assumptions or limitations.

Do not modify unrelated modules.

## Code Quality

* Follow standard Python conventions.
* Prefer type hints.
* Use clear function and variable names.
* Keep functions focused.
* Avoid unnecessary abstractions.
* Add docstrings where they improve understanding.
* Handle errors explicitly.
* Log meaningful operational information.
* Do not hide failures with broad exception handling.

## Data Engineering Principles

InsightStream will use a Bronze → Silver → Gold lakehouse architecture.

### Bronze

Purpose:

* Preserve source information.
* Minimal transformation.
* Maintain ingestion metadata.

### Silver

Purpose:

* Schema enforcement.
* Data type normalization.
* Deduplication.
* Data quality checks.
* Cleaning and enrichment.

### Gold

Purpose:

* Business-ready analytical datasets.
* Customer 360.
* ML-ready features where appropriate.

## ML Principles

Models must be developed with attention to:

* train/validation/test separation
* temporal leakage
* feature leakage
* reproducibility
* appropriate evaluation metrics
* model versioning
* experiment tracking

Do not optimize for accuracy alone.

## Streaming Principles

Streaming implementations must consider:

* event ordering
* duplicate events
* late-arriving events
* offsets
* checkpointing
* schema evolution
* failure recovery
* idempotency / exactly-once semantics where applicable

## AWS Principles

Use AWS resources deliberately.

Development environments should use appropriately sized resources and should be shut down when not required.

Never commit AWS credentials.

## Repository Structure

Do not reorganize the repository unless explicitly requested or a demonstrated architectural requirement makes the current structure inadequate.

## Current Stage

The project is currently in Phase 0: Project Foundation.

The next planned module is the Data Simulator.

Do not implement the Data Simulator until explicitly instructed.
