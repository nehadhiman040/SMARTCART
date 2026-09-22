# SMARTCART
AI-powered customer segmentation system that uses unsupervised machine learning and clustering algorithms to identify customer behaviour patterns and support personalised marketing and customer retention.


# SmartCart Customer Clustering & Analytics System 🛒📊

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Unsupervised_ML-orange.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Preprocessing-green.svg)

## 📌 Executive Summary
SmartCart is an e-commerce platform operating across multiple countries. Prior to this project, the company utilized generic, one-size-fits-all marketing strategies. This lack of segmentation led to inefficient marketing spend, missed customer retention opportunities, and high churn rates.

This project implements an **Intelligent Customer Segmentation System** using **Unsupervised Machine Learning (Clustering)** to analyze customer purchase behaviors, demographics, web activity, and engagement patterns for targeted marketing and customer retention strategies.

---

## 📊 Dataset Overview
The dataset contains **2,240 customer records** across **22 baseline attributes**:

* **Demographics:** `ID`, `Year_Birth`, `Education`, `Marital_Status`, `Income`, `Kidhome`, `Teenhome`, `Dt_Customer`
* **Purchase Behavior (Monetary Spent):** `MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`
* **Purchase Behavior (Frequency & Channels):** `NumDealsPurchases`, `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`, `NumWebVisitsMonth`
* **Customer Engagement & History:** `Recency`, `Complain`, `Response`

---

## 🛠️ Data Preprocessing & Feature Engineering

1. **Handling Missing Values:**
   * Missing values in `Income` (24 records) were imputed using the column **median**.
2. **Derived Features:**
   * **`Age`**: Calculated as $2026 - \text{Year\_Birth}$.
   * **`Customer_Tenure_Days`**: Days enrolled relative to the latest transaction date.
   * **`Total_Spending`**: Aggregated sum of all category spend variables (`MntWines` + `MntFruits` + `MntMeatProducts` + `MntFishProducts` + `MntSweetProducts` + `MntGoldProds`).
   * **`Total_Children`**: Sum of `Kidhome` and `Teenhome`.
3. **Categorical Recoding:**
   * **`Education`**: Re-grouped into `Undergraduate`, `Graduate`, and `Postgraduate`.
   * **`Living_With`**: Mapped from `Marital_Status` into simplified groups (`Partner` or `Alone`).
4. **Feature Selection:**
   * Dropped non-informative identifiers and redundant raw columns (`ID`, `Year_Birth`, `Marital_Status`, `Kidhome`, `Teenhome`, `Dt_Customer`, and raw category spending columns).

---

## 🏗️ Technical Stack
* **Language:** Python 3.x
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Clustering Algorithms, StandardScaler, PCA)

---

## 🚀 How to Run

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/your-username/smartcart-clustering.git](https://github.com/your-username/smartcart-clustering.git)
   cd smartcart-clustering