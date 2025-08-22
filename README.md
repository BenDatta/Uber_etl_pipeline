# 🚖 Uber ETL Pipeline with Airflow & GCS  

## 📌 Overview  
This project demonstrates an **end-to-end ETL pipeline** for Uber ride data using **Apache Airflow**.  
The pipeline:  
- 📥 Extracts raw CSV data  
- 🧹 Transforms it into a clean format  
- ☁️ Loads it into **Google Cloud Storage (GCS)** for further analytics & visualization  

This project highlights my **Data Engineering skills** in:  
✔️ Pipeline automation  
✔️ Data cleaning  
✔️ Cloud integration  
✔️ Data Analysis and Visualization

*(Click image to view interactive dashboard)* 
[![Uber ETL Dashboard](https://raw.githubusercontent.com/BenDatta/Uber_etl_pipeline/main/dashboard.png)](https://lookerstudio.google.com/s/k9dSeSe-nJk)

---

## ⚙️ Tech Stack  

- 🐍 **Python** → Core ETL scripting & transformations  
- 📦 **Pandas** → Data cleaning and wrangling  
- ☁️ **Google Cloud Storage (GCS)** → Cloud data lake  
- 🛠️ **Apache Airflow** → Orchestration & workflow automation  
- 🐳 **Docker (Optional)** → Containerized Airflow deployment  
- 📊 **Looker Studio / Power BI** → Analytics & dashboards  

---

📥 **Extract**  
- Read raw Uber CSV dataset from local storage  
- Validate file presence & row count  

🧹 **Transform**  
- Drop unused/unnecessary columns  
- Fill missing values with median/mode strategies  
- Standardize column names & output cleaned dataset  

☁️ **Load**  
- Upload transformed data as **`uber_cleaned.csv`** into GCS bucket  

⚙️ **Orchestration**  
- Airflow DAG runs daily with retry logic  
- Uses **XCom** to pass metadata between tasks  

---

## 📊 Example Use Cases
With the cleaned dataset stored in GCS, you can build:

🚖 Trip Analytics → Trips by day, city, time of day  
💵 Revenue Reports → Average booking value & total revenue  
🌍 Geospatial Analysis → Pick-up and drop-off heatmaps  
⭐ Driver Performance → Ratings, cancellations, and service quality  

---

## 🔧 Code Walkthrough
DAG File → `uber_etl_dag.py`  

extract_data() → Reads the raw CSV file  
transform_data() → Cleans, imputes, and restructures data  
load_to_gcs() → Uploads cleaned file to GCS bucket  

Airflow DAG Flow:  
extract_task >> transform_task >> load_task  

➡️ Ensures correct order: **Extract → Transform → Load**

---

## 🚀 How to Run

1️⃣ **Clone Repository**  
git clone https://github.com/BenDatta/Uber_etl_pipeline.git  
cd Uber_etl_pipeline  

2️⃣ **Install Requirements**  
pip install -r requirements.txt  

3️⃣ **Setup Google Cloud**  
- Create a GCS bucket (e.g., `uber_data_etl`)  
- Authenticate with a GCP service account:  
```bash
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/key.json"e.g., uber_data_etl)

Authenticate with a GCP service account:

export GOOGLE_APPLICATION_CREDENTIALS="/path/to/key.json"

4️⃣ Run Airflow DAG

Start Airflow:

airflow standalone


Enable DAG: uber_etl_dag
Check logs for ETL execution 🚀

🎯 Key Highlights

✅ Production-ready ETL pipeline with Airflow
✅ Data cleaning & quality checks using Pandas
✅ Automated scheduling with Airflow DAGs
✅ Integrated with Google Cloud Storage for scalable storage
✅ Designed for real-world analytics & BI dashboards
