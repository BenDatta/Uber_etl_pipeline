# 🚖 Uber ETL Pipeline with Airflow & GCS  

## 📌 Overview  
This project demonstrates an **end-to-end ETL pipeline** for Uber ride data using **Apache Airflow**.  
The pipeline:  
- 📥 Extracts raw CSV data  
- 🧹 Transforms it into a clean format  
- ☁️ Loads it into **Google Cloud Storage (GCS)** for further analytics & visualization

![Workflow](https://raw.githubusercontent.com/BenDatta/Uber_etl_pipeline/main/Workflow.png)  
---

## ⚙️ Tech Stack  

- 🐍 **Python** → Core ETL scripting & transformations  
- ☁️ **Google Cloud Storage (GCS)** → Cloud data lake  
- 🛠️ **Apache Airflow** → Orchestration & workflow automation  
- 📊 **Looker Studio ** → Analytics & dashboards  

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

## 📊 Visualization
With the cleaned dataset stored in GCS, you can build:

🚖 Trip Analytics → Trips by day, city, time of day  
💵 Revenue Reports → Average booking value & total revenue  
🌍 Geospatial Analysis → Pick-up and drop-off heatmaps  
⭐ Driver Performance → Ratings, cancellations, and service quality  

[![Uber ETL Dashboard](https://raw.githubusercontent.com/BenDatta/Uber_etl_pipeline/main/dashboard.png)](https://lookerstudio.google.com/s/k9dSeSe-nJk)

🎯 Key Highlights

✅ Production-ready ETL pipeline with Airflow
✅ Data cleaning & quality checks using Pandas
✅ Automated scheduling with Airflow DAGs
✅ Integrated with Google Cloud Storage for scalable storage
✅ Designed for real-world analytics & BI dashboards
