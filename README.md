# Customer Segmentation Using Credit Card Data

## Introduction
This project uses the [Credit Card Dataset for Clustering](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata/data), which contains the usage behavior of **8,950 customers** across various attributes such as **balance, purchases, credit limits, payments, and tenure**.  

The goal of this analysis is to perform **unsupervised learning (clustering)** to group customers into meaningful segments based on their credit card usage patterns. Such segmentation can help financial institutions **identify customer types, design targeted marketing strategies, and improve customer relationship management**.  

## Project Workflow
- **Data Preprocessing**
  - Handled missing values (`MINIMUM_PAYMENTS` filled with median, dropped rows with missing `CREDIT_LIMIT`).  
  - Removed non-numeric column `CUST_ID`.  
  - Applied **outlier treatment** using the IQR method.  
  - Standardized features using `StandardScaler`.  

- **Exploratory Data Analysis (EDA)**
  - Visualized feature distributions before and after preprocessing.  
  - Analyzed correlations and feature spread across clusters.  

- **Clustering**
  - Applied **KMeans clustering**.  
  - Used the **Elbow method** to determine the optimal number of clusters (`k=4`).  
  - Assigned descriptive labels to each cluster based on their behavior:
    - **Cluster 0:** Revolvers (High balance, cash advance users)  
    - **Cluster 1:** Low-Usage Customers  
    - **Cluster 2:** Premium/Transactors (High spend, pay in full)  
    - **Cluster 3:** Responsible Users (Moderate spenders, disciplined payments)  

- **Dimensionality Reduction**
  - Used **PCA (2D)** for visualization of customer segments.  

## Results
- Customers were grouped into **4 distinct clusters** with unique behavioral patterns.  
- Cluster interpretation provides business insights such as identifying **high-value customers, low-engagement users, and risky profiles**.  
- PCA visualization helps illustrate separations between groups.  

## Tech Stack
- **Python**  
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`  

## 🚀 How to Run
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/credit-card-clustering.git
