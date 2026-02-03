Flight Price Prediction – End-to-End MLOps System

Python Streamlit FastAPI Airflow Grafana License

Flight Price Prediction is a complete MLOps system designed to simulate a production-grade workflow for predicting flight prices, validating incoming data, scheduling predictions, and monitoring model & data health through dashboards. This project integrates FastAPI, Streamlit, Airflow, Great Expectations, Grafana, and PostgreSQL into one cohesive pipeline.

Project Highlights
On-demand flight price predictions through Streamlit UI
FastAPI backend to expose ML model and store results in PostgreSQL
Scheduled predictions with Airflow DAGs
Data validation & preprocessing with Python
Monitoring dashboard using Grafana
Pie chart for model performance (accuracy)
Bar chart for high-alert inputs
End-to-end pipeline for data ingestion, validation, prediction, and monitoring
Demo Screenshots
Streamlit App
Streamlit UI 1	Streamlit UI 2	Streamlit UI 3
Streamlit 1	Streamlit 2	Streamlit 3
Airflow DAGs
Data Ingestion DAG	Prediction DAG
Airflow Ingestion	Airflow Prediction
PostgreSQL Database (Predictions Storage)
Database Prediction	Database Statistics
Postgres 1	Postgres 2
Grafana Dashboards
Ingestion	Prediction
Grafana Ingestion Dashboard	Grafana Prediction Dashboard
Tech Stack
Language: Python 3.10+
Libraries:
pandas, numpy, requests, scikit-learn, SQLAlchemy
Web Framework: Streamlit, FastAPI
Workflow Orchestration: Apache Airflow
Monitoring & Visualization: Grafana
Database: PostgreSQL
IDE: VS Code
Version Control: Git + GitHub
How It Works
User Interface (Streamlit)

Users provide flight details and get real-time predictions.
Historical predictions are displayed with input features.
ML Model API (FastAPI)

Exposes /predict endpoint for model predictions.
Saves results to the database with features and timestamp.
Database (PostgreSQL + SQLAlchemy)

Stores all prediction records.
Enables historical analysis for monitoring model performance.
Scheduled Prediction Pipeline (Airflow)

Ingests new data and triggers predictions at defined intervals.
Logs all scheduled runs for auditing and debugging.
Data Validation & Preprocessing

Ingested raw data is checked for missing or invalid values.
Cleaned and transformed data is stored as “good data” for predictions.
Monitoring Dashboard (Grafana)

Pie Chart: Shows model accuracy (Correct, Incorrect, Skipped).
Bar Chart: Highlights input features triggering high alerts.
Enables visual tracking of model performance and data quality over time.
Project Structure

predictive-pipeline/
│
├── airflow/
│   ├── dags/
│   │   ├── ingestion_dag.py
│   │   └── prediction_dag.py
│   ├── data/
│   │   ├── raw_data/
│   │   ├── good_data/
│   │   ├── bad_data/
│   │   ├── reports/
│   │   ├── error_data/
│
├── great_expectations/
│
├── logs/
│
├── app/                     # FastAPI application
│   ├── businessLogic/
│   ├── controllers/
│   ├── helpers/
│   ├── databaseLogic/
│   └── main.py
│
├── streamlit/               # Streamlit UI
│   ├── pages/
│   └── predictions.py
│
├── database/
│   ├── db-setup.sql
│
├── scripts/
│   ├── split_dataset.py
│   ├── pricePrediction.ipynb
│   ├── generate_data_errors.ipynb
│
├── docker-compose.yml
├── requirements.txt
└── README.md
Getting Started
1. Clone the repository
git clone https://github.com/visalibaskarankalpana/predictive-pipeline.git
cd predictive-pipeline
2. Set up Python environment
python -m venv venv
# Linux/Mac
source venv/bin/activate  
# Windows
venv\Scripts\activate     
pip install -r requirements.txt
3. Run FastAPI
uvicorn src.api.main:app --reload
4. Run Streamlit
streamlit run streamlit/predictive.py
5. Start Airflow
airflow db init
airflow webserver --port 8080
airflow scheduler
** Conclusion**
Flight Price Prediction demonstrates a complete end-to-end ML workflow including:

Prediction API

User-facing interface

Scheduled data processing

Monitoring and visualization

It’s an excellent example of production-ready ML pipelines integrating Python, Airflow, FastAPI, Streamlit, PostgreSQL, and Grafana.
