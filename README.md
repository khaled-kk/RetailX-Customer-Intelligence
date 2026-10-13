# 🛒 RetailX Customer Intelligence: KMeans Segmentation & Behavior Profiling

[![Field: Data Science](https://img.shields.io/badge/Field-Marketing--Analytics-blue.svg)]()
[![Method: Unsupervised Learning](https://img.shields.io/badge/Method-K--Means--Clustering-orange.svg)]()
[![Academic: MSc Data Science](https://img.shields.io/badge/Academic-University--of--Europe-red.svg)]()

## 📌 Project Overview
This project applies **Unsupervised Machine Learning** to segment a retail customer base into distinct behavioral groups. Developed as part of the **MSc Data Science – Marketing Analytics** module, the study focuses on moving beyond demographics to identify natural customer clusters based strictly on purchasing habits and engagement metrics.

---

## 🎯 Strategic Objective
To identify distinct behavioral segments and design targeted marketing frameworks that enhance:
*   **Customer Engagement:** Personalized interaction based on channel preference.
*   **Retention:** Identifying at-risk high-spenders.
*   **Revenue Growth:** Optimizing promotional spend by targeting "Deal Seekers."

---

## ⚙️ Technical Methodology

### 1. Data Engineering & Preprocessing
*   **Behavioral Focusing:** Clustered on 9 behavioral features only (`avg_order_size`, `avg_order_freq`, `crossbuy`, `multichannel`, `per_sale`, `tenure`, `return_rate`, `loyalty_card`, `avg_mktg_cnt`). Demographics (`income`, `age`, `household_size`, `married`, `own_home`, `zip_code`) are used afterwards to profile segments, not to form them.
*   **Feature Scaling:** Applied `StandardScaler` to ensure distance-based clustering was mathematically balanced.

### 2. Clustering & Model Selection
*   **Algorithm:** `KMeans` implementation.
*   **Optimization:** Evaluated $k = 2$ to $8$ using:
    *   **Elbow Method** & **Silhouette Score**.
    *   **Calinski–Harabasz Index**.
    *   **PCA Visualization** for cluster separability analysis.
*   **Optimal Choice:** **$k=3$** was selected for its superior statistical separation and strategic interpretability.

### 3. Model Validation
To check how well the clusters can be recovered, supervised models were trained to predict the segment labels from behavioral + descriptive features (70/30 stratified split, 600 test customers):

| Model | Accuracy | Macro F1 |
| :--- | :--- | :--- |
| **Logistic Regression** | 98.7% | 98.5% |
| **Random Forest** | 95.0% | 93.2% |
| **Decision Tree** | 93.5% | 91.8% |

---

## 👥 Segment Personas & Strategies

### 🔹 Segment 0: Loyalty-Driven Explorers
*   **Traits:** High `crossbuy`, active `loyalty_card`, moderate frequency.
*   **Strategy:** Gamified rewards and personalized product bundles.

### 🔹 Segment 1: Multichannel Deal Seekers
*   **Traits:** High `multichannel` usage, high `per_sale` engagement, long `tenure`.
*   **Strategy:** Flash sales and cross-channel exclusive offers.

### 🔹 Segment 2: High-Spend Occasionalists
*   **Traits:** High `order_size`, high `return_rate`, low `tenure`.
*   **Strategy:** Post-purchase engagement and satisfaction guarantees to reduce churn.

---

## 🔍 Key Feature Importance (Random Forest)
Top drivers by Random Forest importance (all 15 predictors):
1. `per_sale`
2. `tenure`
3. `crossbuy`
4. `avg_order_freq`
5. `multichannel`

---

## 🛠️ Technologies Used
*   **Languages & Tools:** Python, Jupyter Notebooks.
*   **ML Libraries:** Scikit-learn (KMeans, Random Forest, PCA), Pandas, NumPy.
*   **Visualization:** Matplotlib, Seaborn.

---

## 📁 Repository Contents

| File | Purpose |
| :--- | :--- |
| `RetailX_Customer_Segmentation_and_Classification_Analysis.ipynb` | Full analysis: scaling, k selection, final K-Means (k=3), profiling, PCA plot, classification |
| `RetailX_KM(segmentation_result).csv` | Input data: 2,000 customers with behavioral and demographic fields |
| `RetailX_Report.pdf` | Written report with the findings and marketing recommendations |

## ▶️ How to Run
1. Open the notebook in Google Colab (or Jupyter).
2. Upload `RetailX_KM(segmentation_result).csv` and update the path in the "Load data" cell (`/content/...` by default).
3. Run all cells in order.

---
*Developed by Khaled Walid*
