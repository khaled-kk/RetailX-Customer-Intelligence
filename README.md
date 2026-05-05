# 🛒 RetailX Customer Intelligence: KMeans Segmentation & Behavior Profiling

[![Field: Data Science](https://img.shields.io/badge/Field-Marketing--Analytics-blue.svg)]()
[![Method: Unsupervised Learning](https://img.shields.io/badge/Method-K--Means--Clustering-orange.svg)]()
[![Academic: MSc Data Science](https://img.shields.io/badge/Academic-University--of--Europe-red.svg)]()

## 📌 Project Overview
This project applies **Unsupervised Machine Learning** to segment a retail customer base into distinct behavioral groups. Developed as part of the **MSc Data Science – Marketing Analytics** module, the study focuses on moving beyond demographics to identify natural customer clusters based strictly on purchasing habits and engagement metrics.[cite: 1]

---

## 🎯 Strategic Objective
To identify distinct behavioral segments and design targeted marketing frameworks that enhance:
*   **Customer Engagement:** Personalized interaction based on channel preference.
*   **Retention:** Identifying at-risk high-spenders.[cite: 1]
*   **Revenue Growth:** Optimizing promotional spend by targeting "Deal Seekers."[cite: 1]

---

## ⚙️ Technical Methodology

### 1. Data Engineering & Preprocessing
*   **Behavioral Focusing:** Excluded demographic noise to ensure clusters were driven by actions (e.g., `avg_order_size`, `tenure`, `return_rate`).[cite: 1]
*   **Feature Scaling:** Applied `StandardScaler` to ensure distance-based clustering was mathematically balanced.[cite: 1]

### 2. Clustering & Model Selection
*   **Algorithm:** `KMeans` implementation.[cite: 1]
*   **Optimization:** Evaluated $k = 2, 3, 4$ using:[cite: 1]
    *   **Elbow Method** & **Silhouette Score**.[cite: 1]
    *   **Calinski–Harabasz Index**.[cite: 1]
    *   **PCA Visualization** for cluster separability analysis.[cite: 1]
*   **Optimal Choice:** **$k=3$** was selected for its superior statistical separation and strategic interpretability.[cite: 1]

### 3. Model Validation
To confirm the stability of the unsupervised clusters, supervised models were trained to predict the segment labels:[cite: 1]

| Model | Accuracy | Macro F1 |
| :--- | :--- | :--- |
| **Logistic Regression** | 98.7% | 98.5% |[cite: 1]
| **Random Forest** | 95.0% | 93.2% |[cite: 1]
| **Decision Tree** | 93.5% | 91.8% |[cite: 1]

---

## 👥 Segment Personas & Strategies

### 🔹 Segment 0: Loyalty-Driven Explorers
*   **Traits:** High `crossbuy`, active `loyalty_card`, moderate frequency.[cite: 1]
*   **Strategy:** Gamified rewards and personalized product bundles.[cite: 1]

### 🔹 Segment 1: Multichannel Deal Seekers
*   **Traits:** High `multichannel` usage, high `per_sale` engagement, long `tenure`.[cite: 1]
*   **Strategy:** Flash sales and cross-channel exclusive offers.[cite: 1]

### 🔹 Segment 2: High-Spend Occasionalists
*   **Traits:** High `order_size`, high `return_rate`, low `tenure`.[cite: 1]
*   **Strategy:** Post-purchase engagement and satisfaction guarantees to reduce churn.[cite: 1]

---

## 🔍 Key Feature Importance (Random Forest)
The top drivers determining customer clusters were:[cite: 1]
1. `per_sale`
2. `tenure`
3. `crossbuy`
4. `avg_order_freq`

---

## 🛠️ Technologies Used
*   **Languages & Tools:** Python, Jupyter Notebooks.[cite: 1]
*   **ML Libraries:** Scikit-learn (KMeans, Random Forest, PCA), Pandas, NumPy.[cite: 1]
*   **Visualization:** Matplotlib, Seaborn.[cite: 1]
---
*Developed by Khaled Walid*
