# Data_eng_zoomcamp_mod_2
for submission of module 2 workflow orchestration homework 2

# Data Engineering Zoomcamp 2026 - Module 2: Workflow Orchestration with Kestra

This repository contains the solution for Module 2 of the Data Engineering Zoomcamp. The focus of this module is on orchestrating data pipelines using **Kestra**, Dockerized **PostgreSQL**, and managing large-scale data ingestion for the NYC Taxi dataset (2019-2021).

## 🚀 Project Overview

The goal of this project was to establish a robust orchestration environment to:
1.  **Extract**: Pull raw taxi data (Yellow and Green) from GitHub in CSV format.
2.  **Load**: Ingest the data into a local PostgreSQL instance running in Docker.
3.  **Verify**: Perform data quality checks and row count analysis for specific timeframes.

## 🛠️ Technology Stack
* **Orchestrator**: Kestra
* **Database**: PostgreSQL 16
* **Infrastructure**: Docker & Docker Compose
* **Version Control**: Git & GitHub

## 📂 Repository Structure
```text
.
├── docker-compose.yml         # Defines Kestra and Postgres services
├── .gitignore                 # Prevents local data/volumes from being tracked
└── flow/                      # Kestra Flow Definitions (YAML)
    ├── 04_postgres_taxi.yaml             # Main ingestion logic for 2019-2021
    └── 05_postgres_taxi_scheduled.yaml   # Scheduled flow with timezone logic (Q6)
