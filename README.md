# Patient-Monitoring-Project
A fully automated real-time patient vital monitoring system built on Google Cloud Platform.
# 🏥 Patient Vital Monitoring – Real-Time Health Data Pipeline (GCP + Dataflow + Power BI)

## 📌 Project Overview
This project implements a real-time **Patient Vital Monitoring System** using Google Cloud Platform.  
Simulated health metrics — **blood pressure, heart rate, temperature, and oxygen saturation** — are generated every 2 seconds, processed through a streaming data pipeline, and visualized in a **Power BI dashboard (DirectQuery)**.

The system automatically computes the **patient risk level** (Low, Moderate, High) based on incoming data.

---

## 🚀 Architecture

The pipeline follows a fully automated, cloud-native architecture based on **GCP**.

### **1. Data Generation**
- Python script simulates vital signs every **2 seconds**
- Data streamed to **Google Pub/Sub**

### **2. Dataflow Streaming Pipeline (Apache Beam)**
Implements a **Medallion Architecture**:

| Layer | Description | Storage |
|-------|-------------|----------|
| 🟤 **Bronze** | Raw JSON data from Pub/Sub | GCS |
| ⚪ **Silver** | Cleaned and validated data | GCS |
| 🟡 **Gold** | Fully transformed analytics-ready data | BigQuery |

### **3. Storage**
- Bronze & Silver → **Google Cloud Storage**
- Gold → **BigQuery**

### **4. Visualization**
- **Power BI**
- Connected to BigQuery using **DirectQuery**
- Real-time refresh without data import

---

## 🎯 Objectives
- Simulate realistic patient data streams  
- Build a real-time Dataflow pipeline (Apache Beam)  
- Apply transformations following Medallion architecture  
- Classify patient risk level  
- Deliver a live monitoring dashboard in Power BI  
- Achieve a fully automated, serverless environment  

---

## 🛠️ Technologies Used
- Python  
- Google Pub/Sub  
- Google Cloud Storage  
- Google Dataflow (Apache Beam)  
- BigQuery  
- Power BI (DirectQuery)  
- GitHub  

---



