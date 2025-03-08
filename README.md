# 🚄 IRCTC Real-Time Data Pipeline using Google Cloud (GCP)

## 📢 Overview  
The **IRCTC Real-Time Data Pipeline** is a cloud-based data processing system designed to ingest, transform, and store real-time streaming data from IRCTC (Indian Railway Catering and Tourism Corporation). This project leverages **Google Cloud Platform (GCP)** services such as **Pub/Sub, Dataflow (Apache Beam), BigQuery, and Cloud Storage** to enable seamless data processing, transformation, and analysis.


## 📊 Project Diagram
![IRCTC Flowchart](https://github.com/user-attachments/assets/ea067730-0a22-47ec-9058-44aaa2e2b40a)



## 📁 Architecture Overview  
### **🔹 Data Flow Pipeline**
1. **Data Ingestion**: Simulated **IRCTC Mock Data** is published to **Google Pub/Sub**.
2. **Data Processing**: A **Dataflow pipeline (Apache Beam)** reads data from Pub/Sub, applies **Python UDFs** for transformation and fault tolerance.
3. **Data Storage**: The transformed data is stored in **Google BigQuery** for analytics.
4. **UDF Registration**: User-defined functions (**transform_UDF.py**) are registered from **Google Cloud Storage** to BigQuery.

---

## ⚙️ Tech Stack  
- **Google Cloud Pub/Sub** → Real-time message streaming  
- **Google Dataflow (Apache Beam)** → Data processing and transformation  
- **Google BigQuery** → Data warehouse for analytics  
- **Google Cloud Storage** → Stores UDF files  
- **Python** → Apache Beam pipeline & UDF implementation  
- **SQL** → Data transformation & querying in BigQuery  
- **Terraform** (Optional) → Infrastructure as Code (IaC) for GCP setup  



## 🗄️ BigQuery Schema

| Column Name       | Data Type   | Description                          |
|------------------|------------|--------------------------------------|
| `row_key`        | STRING      | Unique identifier for each record   |
| `name`           | STRING      | Passenger's name                    |
| `age`            | INT64       | Passenger's age                     |
| `email`          | STRING      | Passenger's email address           |
| `join_date`      | DATE        | Date when the passenger joined      |
| `last_login`     | TIMESTAMP   | Last login timestamp                |
| `loyalty_points` | INT64       | Loyalty points earned               |
| `account_balance`| FLOAT64     | Account balance in INR              |
| `is_active`      | BOOL        | Indicates if the account is active  |
| `inserted_at`    | TIMESTAMP   | Timestamp when the record was inserted |
| `updated_at`     | TIMESTAMP   | Last updated timestamp              |
| `loyalty_status` | STRING      | Loyalty membership status           |
| `account_age_days` | INT64     | Total days since account creation   |

---

## 🎯 Use Cases  
- 📊 **Passenger Behavior Analysis:** Using real-time & historical data to understand customer trends.  
- 🎁 **Loyalty Program Management:** Enhancing customer engagement through data-driven rewards.  
- 🔍 **Operational Monitoring:** Identifying active/inactive users for improved service efficiency.  
- 📈 **Trend Analysis:** Leveraging BigQuery for actionable business insights.  

## 📝 Future Enhancements  
✅ **Integrate Cloud Functions** for event-driven triggers.  
✅ **Implement Dataflow Streaming Mode** for real-time analytics.  
✅ **Optimize BigQuery Queries** to enhance cost efficiency and performance.  


## ⭐ Contribute  
Contributions are welcome! If you’d like to improve the project, feel free to fork the repository and submit a pull request.


