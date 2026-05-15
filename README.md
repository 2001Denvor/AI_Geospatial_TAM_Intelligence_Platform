A high-quality GitHub README should be both a technical manual and a business case for your project. Since your code involves complex data engineering and machine learning, this structure highlights your ability to turn raw data into a strategic intelligence tool.

---

# AI Geospatial TAM Intelligence Platform

## 🌐 Project Overview

The **AI Geospatial TAM Intelligence Platform** is an end-to-end data science solution designed to optimize telecommunications infrastructure deployment. By integrating national census data (CPH 2024) with technical network metrics, the platform identifies the **Total Addressable Market (TAM)** and highlights geographic regions with the highest expansion potential.

The platform segments over 14,000 Grama Niladhari (GN) divisions into priority tiers, allowing stakeholders to make data-driven decisions on 5G rollout, Fiber expansion, and churn mitigation.

---

## 🚀 Key Features

* **Multi-Source Data Integration:** Automated pipelines to clean and merge complex, multi-header Excel datasets (Population & Housing).
* **Feature Engineering:** Custom modeling of "Demand Scores" based on working-age demographics and "Gap Scores" to identify underserved markets.
* **Unsupervised Machine Learning:** Implementation of **K-Means Clustering** to segment regions into High, Medium, and Low expansion priorities.
* **Infrastructure Simulation:** Synthetic modeling of Fiber/DSL footprints and mobile traffic load to calculate a **Network Pressure Index**.
* **Commercial Analytics:** Tracking of ARPU (Average Revenue Per User), subscriber density, and churn risk at a granular geographic level.

---

## 🛠️ Tech Stack

* **Language:** Python
* **Environment:** Databricks
* **Data Processing:** Pandas, NumPy
* **Big Data Tools:** PySpark, Spark SQL
* **Machine Learning:** Scikit-Learn (`KMeans`, `StandardScaler`)
* **Visualization:** Databricks SQL Dashboards

---

## 📊 Methodology & Logic

### 1. Market Gap Analysis

The core logic calculates the difference between potential demand and existing infrastructure:


$$Gap\ Score = Demand\ Score - Housing\ Score$$

* **Demand Score:** Derived from the working-age population (ages 15–59).
* **Housing Score:** Derived from occupied housing units.

### 2. Clustering & Segmentation

Using **K-Means Clustering**, the model groups GN divisions into three distinct clusters based on:

1. Demand Intensity
2. Infrastructure Availability
3. Market Gap

---

## 📂 Project Structure

```text
├── GN_population_excel.xlsx    # Raw Census Population Data
├── GN_housing_excel.xlsx       # Raw Census Housing Data
├── main_analysis.py            # Data Cleaning, ML Modeling & Segmentation
├── commercial_sim.py           # Logic for ARPU and Churn simulation
├── mobile_network_sim.py       # Mobile capacity and traffic load modeling
└── README.md                   # Project Documentation

```

---

## 📈 Dashboard Insights

The platform generates several critical views for executive decision-making:

* **Top 10 Opportunity Areas:** GN divisions with the highest positive Gap Score.
* **Network Pressure Map:** Identifies areas where Traffic Load exceeds Capacity.
* **Commercial Performance Score:** A weighted index of ARPU, churn, and subscriber density.

---

## 🎯 Impact

This project provides a roadmap for:

* **Reducing Churn:** Identifying low-quality network areas with high user concentrations.
* **Strategic Growth:** Focusing capital expenditure on the **25% High Expansion** zones identified by the ML model.
* **Resource Optimization:** Efficiently allocating technical teams to high-pressure network nodes.

---

*Developed during my AI Internship at Sri Lanka Telecom.*
