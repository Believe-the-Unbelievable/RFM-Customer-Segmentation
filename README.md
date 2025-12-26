# Customer Segmentation using RFM Analysis
## Overview
This project performs customer segmentation using RFM (Recency, Frequency, Monetary) analysis on retail transaction data.
The goal is to identify high-value customers and group customers into meaningful segments that can support targeted marketing and retention strategies.
## Problem Statement
Businesses often have large volumes of transaction data but lack clarity on:
* Who their most valuable customers are
* Which customers are at risk of churn
* Where to focus marketing and retention efforts
This project addresses these challenges by transforming raw transaction data into actionable customer segments.
## Dataset
The dataset contains transactional information such as:
* Customer ID
* Invoice number
* Invoice date
* Quantity purchased
* Unit price

The dataset is publicly available on Kaggle:
https://www.kaggle.com/datasets/ulrikthygepedersen/online-retail-dataset
## Approach
1. Data Cleaning
* Removed records with missing customer IDs
* Filtered out returns and invalid transactions
* Converted invoice dates to datetime format
2. Feature Engineering
* Created TotalAmount to represent transaction-level revenue
* Defined a reference date to calculate recency
3. RFM Metrics Calculation
For each customer:
* Recency: Days since the last purchase
* Frequency: Number of purchases
* Monetary: Total amount spent
4. RFM Scoring
* Customers were scored from 1 to 4 using quartile-based thresholds
* Recency was inversely scored (more recent purchases receive higher scores)
5. Customer Segmentation
Combined R, F, and M scores to generate overall RFM scores
Customers were grouped into:
* Low-value
* Mid-value
* High-value
  
Additional business-friendly segments such as VIP/Loyal, Potential Loyal, At Risk, and Lost were defined
## Visualizations
The project includes multiple visualizations to interpret results:
* Bar charts showing customer distribution by segment
* Treemap illustrating hierarchical customer segmentation
* Box plots analyzing VIP customer behavior
* Correlation heatmap of RFM scores
* Grouped bar charts comparing RFM metrics across segments
<img width="1198" height="479" alt="Screenshot 2025-12-26 154747" src="https://github.com/user-attachments/assets/4ed29df7-3e7b-4d4b-ac04-c33da5094ccf" />
<img width="857" height="345" alt="Screenshot 2025-12-26 154826" src="https://github.com/user-attachments/assets/28f589cf-47fc-44d1-824c-43fbbea81270" />
<img width="884" height="372" alt="Screenshot 2025-12-26 154842" src="https://github.com/user-attachments/assets/8bf2fe9d-ea81-4d8c-84ef-982efe71ddaa" />
<img width="885" height="390" alt="Screenshot 2025-12-26 154900" src="https://github.com/user-attachments/assets/5f5d4d95-efcd-465f-9f0b-670636b3231a" />
<img width="1392" height="420" alt="Screenshot 2025-12-26 154920" src="https://github.com/user-attachments/assets/dd5dd4a5-a65d-4569-b443-a3688a154705" />

## Insights 
* A small group of customers contributes a large portion of revenue
* VIP/Loyal customers exhibit high frequency and monetary value with low recency
* At-risk and lost customers show low engagement and spending
* RFM segmentation provides clear guidance for targeted marketing actions
## Business Recommendations
* Retain VIP/Loyal customers through loyalty programs and personalized offers
* Upsell and cross-sell Mid-value customers
* Re-engage At-risk customers with targeted campaigns
* Limit spending on Lost customers unless reactivation is cost-effective
## Tools and Libraries Used
* Python
* Pandas
* NumPy
* Plotly
* Jupyter Notebook
## Conclusion
This project demonstrates how RFM analysis can transform raw transaction data into meaningful customer insights.
The approach is transparent, business-friendly, and suitable for real-world analytics and decision-making.
## Author
## 👤 Muhammed Azeem
Machine Learning & Data Science Enthusiast

Any queries: muhammedazeemph15@gmail.com
