# Telecom Customer Churn Analysis & Prediction
**SQL | Power BI | Machine Learning**

---

## 📊 Project Summary

This project analyzes telecom customer data to **identify churn patterns, understand customer behavior, and predict future churners** using an end-to-end analytics pipeline built with **SQL Server, Power BI, and Python Machine Learning**.

The solution helps telecom businesses understand **why customers leave and which customers are likely to churn**, enabling targeted retention strategies.

---

## 📸 Dashboard Preview

### Executive Summary Dashboard

[View Full Image](./Summary.png)

![Executive Dashboard](./Summary.png)

---

### Churn Analysis Dashboard

[View Full Image](./Churn%20Analysis%20Dashboard.png)

![Churn Dashboard](./Churn%20Analysis%20Dashboard.png)

---

## 🎯 Business Objective

Customer churn is a major challenge in the telecom industry, where retaining existing customers is significantly cheaper than acquiring new ones.

This project helps telecom companies:

- Identify **customers at high risk of churn**
- Understand **factors driving churn**
- Monitor churn trends through **interactive dashboards**
- Predict **future churners using machine learning**

The insights help businesses design **data-driven retention campaigns and improve customer loyalty.**

---

## 📊 Power BI Dashboard Insights

The Power BI dashboard provides a comprehensive view of customer churn across **demographics, contracts, services, payment methods, and geography.**

### Key Metrics

- Total Customers  
- New Joiners  
- Total Churn  
- Churn Rate  

### Major Business Insights

- **Month-to-month contract customers have the highest churn rate**, indicating lower commitment levels.
- Customers using **Electronic Check payment methods churn significantly more** than those using automatic payments.
- **Customers with short tenure (0–12 months)** show the highest churn probability.
- **Fiber optic internet users have relatively higher churn rates**, suggesting possible pricing or service concerns.
- Customers without **additional services (streaming or security)** are more likely to churn.
- Certain **regions consistently show higher churn**, which may indicate service or infrastructure issues.

---

## 🧱 Technology Stack

| Layer | Tools Used |
|------|-------------|
| Data Storage | Microsoft SQL Server |
| Data Processing | SQL Queries, Views |
| Visualization | Power BI |
| Data Analysis | DAX Measures |
| Machine Learning | Python (Random Forest Classifier) |
| Development Tools | Jupyter Notebook, VS Code |

---

## ⚙️ Project Workflow

The project follows an **end-to-end data analytics pipeline**.

### 1️⃣ Data Extraction
- Imported telecom customer data from **CSV files**

### 2️⃣ Data Cleaning & Transformation
- Handled missing values
- Standardized categorical variables
- Structured the dataset for analysis

### 3️⃣ Data Modeling
- Created production tables in SQL Server
- Built optimized **SQL views for Power BI**

### 4️⃣ Data Visualization
- Developed **interactive Power BI dashboards**
- Created calculated columns and measures using **DAX**

### 5️⃣ Machine Learning Prediction
- Built a **Random Forest classification model**
- Predicted customers likely to churn

---

## 🔄 ETL Pipeline (SQL Server)

The ETL process converts raw telecom data into structured analytical datasets.

**Steps performed:**

1. Created database in SQL Server  
2. Imported raw **Customer_Data.csv**  
3. Cleaned and transformed data  
4. Loaded processed data into production tables  
5. Created SQL views optimized for Power BI reporting  

---

## 📊 Power BI Data Modeling

Additional transformations were performed inside Power BI.

### Calculated Columns

- Churn Status
- Age Group Segmentation
- Tenure Group
- Monthly Charge Range

### DAX Measures

```DAX
Total Customers = COUNT(prod_Churn[Customer_ID])

New Joiners =
CALCULATE(
COUNT(prod_Churn[Customer_ID]),
prod_Churn[Customer_Status] = "Joined"
)
```
Total Churn = SUM(prod_Churn[Churn Status])

Churn Rate = [Total Churn] / [Total Customers]

## 🤖 Machine Learning – Churn Prediction

A **Random Forest Classifier** was used to predict customers who are likely to churn based on their demographic, service usage, and account information.

---

### Model Development

The machine learning pipeline included the following steps:

1. **Loaded churn dataset** from the SQL view.
2. **Encoded categorical variables** using `LabelEncoder`.
3. **Removed irrelevant columns** such as `Customer_ID`.
4. **Split the dataset** into training (80%) and testing (20%) sets.
5. **Trained a Random Forest classification model**.
6. **Evaluated the model performance** using:
   - Confusion Matrix
   - Classification Report

---

## 📡 Predicting Future Churners

The trained model was then used to predict churn probability for **new customers**.

### Prediction Process

1. Loaded **new customer dataset**.
2. Applied the **same preprocessing and encoding steps** used during training.
3. Generated **churn predictions using the trained model**.
4. Exported predicted churn results to a **CSV file** for visualization in Power BI.

This allows businesses to **identify high-risk customers early and take preventive retention actions**.

---

## 📈 Business Impact

This project enables telecom companies to:

- Understand **customer churn patterns**
- Identify **high-risk customer segments**
- Monitor churn trends through **interactive dashboards**
- Predict churn using **machine learning models**
- Launch **targeted retention campaigns**

---

## ✅ Final Outcome

- Built an **end-to-end SQL + Power BI + Machine Learning analytics pipeline**
- Developed an **interactive Power BI dashboard for churn monitoring**
- Implemented a **Random Forest model to predict future churners**
- Generated **actionable business insights to improve customer retention strategies**

## Author

- Mahak Bisht
- mahak.bisht2003@gmail.com
- 8750508853
