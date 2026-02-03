✈️ Flight Price Prediction – End-to-End MLOps System

Python | Streamlit | FastAPI | Apache Airflow | PostgreSQL | Grafana

Flight Price Prediction is a complete end-to-end MLOps system that simulates a production-grade workflow for predicting flight prices, validating incoming data, scheduling predictions, and monitoring model & data health through dashboards.

The system integrates FastAPI, Streamlit, Airflow, Great Expectations, Grafana, and PostgreSQL into a unified pipeline.

🚀 Project Highlights

On-demand flight price predictions through Streamlit UI

FastAPI backend exposing ML model and storing results in PostgreSQL

Scheduled predictions using Apache Airflow DAGs

Data validation & preprocessing with Python and Great Expectations

Monitoring dashboards using Grafana

Pie chart for model performance (accuracy)

Bar chart for high-alert inputs

End-to-end pipeline: ingestion → validation → prediction → monitoring

🧱 Architecture Overview

Streamlit UI → User inputs flight details

FastAPI Service → Runs model & stores predictions

PostgreSQL → Stores predictions & metadata

Airflow DAGs → Scheduled ingestion & predictions

Great Expectations → Data quality checks

Grafana → Monitoring & visualization

🛠 Tech Stack

Language

Python 3.10+

Libraries

pandas, numpy, requests, scikit-learn, SQLAlchemy

Web Frameworks

Streamlit, FastAPI

Workflow Orchestration

Apache Airflow

Monitoring & Visualization

Grafana

Database

PostgreSQL

Tools

VS Code, Git, GitHub, Docker

⚙️ How It Works
1. Streamlit User Interface

Users enter flight details

Displays real-time predictions

Shows historical predictions

2. FastAPI ML Model API

/predict endpoint for inference

Stores prediction + features + timestamp

3. PostgreSQL Database

Stores all prediction records

Enables historical monitoring

4. Airflow Scheduled Pipeline

Ingests new data

Triggers batch predictions

Logs execution details

5. Data Validation & Preprocessing

Checks missing/invalid values

Separates good & bad data

6. Grafana Dashboard

Pie Chart → Model accuracy

Bar Chart → High-alert features

Tracks model & data health

📁 Project Structure
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
├── logs/
│
├── app/                     # FastAPI app
│   ├── businessLogic/
│   ├── controllers/
│   ├── helpers/
│   ├── databaseLogic/
│   └── main.py
│
├── streamlit/
│   ├── pages/
│   └── predictions.py
│
├── database/
│   └── db-setup.sql
│
├── scripts/
│   ├── split_dataset.py
│   ├── pricePrediction.ipynb
│   ├── generate_data_errors.ipynb
│
├── docker-compose.yml
├── requirements.txt
└── README.md

▶️ Getting Started
1️⃣ Clone Repository
git clone <your-repo-url>
cd predictive-pipeline

2️⃣ Create Virtual Environment
python -m venv venv


Linux/Mac

source venv/bin/activate


Windows

venv\Scripts\activate

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Run FastAPI
uvicorn src.api.main:app --reload

5️⃣ Run Streamlit
streamlit run streamlit/predictive.py

6️⃣ Start Airflow
airflow db init
airflow webserver --port 8080
airflow scheduler

✅ Conclusion

This project demonstrates a complete production-style ML workflow including:

Prediction API

User-facing UI

Scheduled batch processing

Data validation

Monitoring & visualization

It showcases how modern ML systems are built and deployed using Python, FastAPI, Streamlit, Airflow, PostgreSQL, and Grafana.

📜 License

This project is open-source and available
