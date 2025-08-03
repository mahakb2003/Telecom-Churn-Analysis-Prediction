# Telecom Customer Churn Analysis & Prediction (SQL + Power BI + ML)

## 🔍 Project Overview
This end-to-end project aims to help a telecom company (e.g., **Airtel**) identify, analyze, and predict **customer churn**. 

By integrating **SQL**, **Power BI**, and **Python (Random Forest)**, we have created a business-intelligent solution to:
- Understand why customers leave
- Segment high-risk customer groups
- Predict future churners
- Recommend actionable strategies to reduce churn and increase customer retention

---

## 💼 Business Objective
In the telecom industry, retaining existing customers is more cost-effective than acquiring new ones. This project enables decision-makers to:
- **Visualize key churn metrics** across customer segments
- **Predict at-risk customers** using machine learning
- **Design targeted retention campaigns** (by contract type, tenure, demographics, etc.)

---

## 🧱 Tech Stack
| Layer          | Tools Used                                |
|----------------|---------------------------------------------|
| Data Storage   | Microsoft SQL Server                       |
| Data Modeling  | SQL Views, Power BI Query Editor           |
| Data Analysis  | SQL Queries, Power BI DAX Measures         |
| Visualization  | Power BI Dashboards                        |
| ML Model       | Python (Random Forest Classifier)          |
| Deployment     | Predictions exported as CSV / SQL Table    |

---

## 🔧 Step 1 – ETL Process in SQL Server

1. **Created Database:**

2. **Imported Raw CSV File**

3. **Data Cleaning & Null Handling**

4. **Transform & Load into Production Table**


5. **Created Views for Power BI**


---

## 📊 Step 2 – Power BI Transformations

- Added calculated columns:
  - **Churn Status**: 1 if churned, else 0
  - **Monthly Charge Range**: Bins of charges
  - **Age Group & Tenure Group**: Segmented by logic (e.g., `<20`, `20-35`, etc.)

- Created reference tables:
  - `mapping_AgeGrp`, `mapping_TenureGrp`, `prod_Services` (using unpivot)

---

## 🧮 Step 3 – Power BI Measures
DAX
Total Customers = COUNT(prod_Churn[Customer_ID])
New Joiners = CALCULATE(COUNT(prod_Churn[Customer_ID]), prod_Churn[Customer_Status] = "Joined")
Total Churn = SUM(prod_Churn[Churn Status])
Churn Rate = [Total Churn] / [Total Customers]


---

## 📈 Step 4 – Power BI Dashboards

### 📌 Summary Page
- **Top Cards:** Total Customers, New Joiners, Total Churn, Churn Rate
- **Demographics:** Gender, Age Group vs Churn
- **Accounts:** Contract Type, Payment Method, Tenure Group
- **Geographic:** Top 5 States with Highest Churn
- **Service Usage:** Internet Type & Streaming Service vs Churn
- **Churn Distribution:** Category & Tooltip: Reason

### 🧠 Churn Prediction Page
- Load CSV from prediction model output
- Charts by: Age, Gender, Marital Status, State, Contract, Payment Method
- Grid View: Customer ID, Revenue, Tenure, etc.

---

## 🤖 Step 5 – Machine Learning Churn Prediction

### 🧰 Tools
- Jupyter Notebook (via Anaconda)
- `RandomForestClassifier` from `sklearn`

### 🔬 Process
1. Loaded data from `vw_ChurnData` view using Excel
2. Encoded categorical columns using LabelEncoder
3. Dropped irrelevant columns like `Customer_ID`, `Churn_Reason`
4. Trained model using 80-20 train-test split
5. Evaluated using confusion matrix and classification report
6. Feature importance visualized to interpret key drivers

### 📡 Predict Future Churners
- Loaded `vw_JoinData`
- Transformed using saved encoders
- Ran `.predict()`
- Filtered only churners → Exported to CSV (`Predictions.csv`)

---

## 💼 Business Impact
This solution equips telecom stakeholders with:
- **Descriptive analytics**: Who churned, from where, and why
- **Diagnostic insights**: High-risk segments (e.g., Prepaid users, older age groups)
- **Predictive power**: Identify new customers likely to churn
- **Strategic levers**: Use actionable dashboards to plan:
  - Loyalty campaigns
  - Contract upgrades
  - Personalized offers

---

## 🗂️ File Structure

📁 Churn-Analysis-Project
│
├── 📂 SQL Scripts
│   └── churn_etl.sql
│
├── 📂 PowerBI
│   └── Churn_Dashboard.pbix
│
├── 📂 ML_Model
│   ├── churn_predictor.ipynb
│   └── Predictions.csv
│
├── 📂 Data
│   ├── Customer_Data.csv
│   └── Prediction_Data.xlsx
│
└── README.md


---

## ✅ Final Outcome
✅ Comprehensive Dashboard showing real-time churn trends  
✅ Machine Learning model that predicts new churners with accuracy  
✅ Executive insights to design **targeted retention campaigns**  
✅ Improved **customer satisfaction** and **business profitability**

---

**This project showcases how business analytics, data engineering, and machine learning can be combined to solve a real-world business problem and drive retention strategy in a competitive industry.**
