# 🛍️ Customer Segmentation using Clustering Techniques

## 📌 Project Overview
This project applies **unsupervised machine learning** to segment customers based on their purchasing behavior. Using real-world **Online Retail Dataset** from the UCI Machine Learning Repository, we leverage **K-Means and DBSCAN clustering** to identify meaningful customer groups and gain insights into their shopping patterns.

## 📂 Dataset Information
- **Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/machine-learning-databases/00352/Online%20Retail.xlsx)
- **Data Type**: E-commerce transactions from a UK-based online retailer.
- **Key Features**:
  - `CustomerID`: Unique identifier for customers
  - `InvoiceDate`: Date & time of purchase
  - `Quantity`: Number of items purchased
  - `UnitPrice`: Price per item
  - `Country`: Location of the customer
  - `StockCode`: Product identifier
  - **Derived Features**:
    - `Total_Bill_Size`: Total spending per customer
    - `Purchase_Interval_Days`: Time between first and last purchase

## 🛠️ Data Preprocessing
✔️ Converted **InvoiceDate** to datetime format  
✔️ Computed **Total_Bill_Size** for each customer  
✔️ Extracted **Most Common Location** and **Top Purchased Item** per customer  
✔️ Handled missing values and standardized numerical features  

## 🤖 Machine Learning Approaches
### **1️⃣ K-Means Clustering**
- **Objective**: Segment customers based on spending patterns.
- **Preprocessing**: Standardized `Total_Bill_Size`.
- **Results**:
  - Cluster 0: **Regular Customers** (Avg. Spend: $1381.65)
  - Cluster 1: **High-Spending Customers** (Avg. Spend: $30,720.77)
  - Cluster 2: **VIP Customers** (Avg. Spend: $52,637.10)

### **2️⃣ DBSCAN (Density-Based Clustering)**
- **Objective**: Detect anomalies & customer segments based on spending and frequency.
- **Preprocessing**: Normalized `Total_Bill_Size` and `Purchase_Interval_Days`.
- **Results**:
  - **Cluster 0**: Majority (Regular Buyers)
  - **Cluster 1 & 2**: High-value Customers
  - **Noise Points**: 12 (Potential outliers)

## 📌 How to Run the Project
1. **Clone the repository**
   ```bash
   git clone https://github.com/Vasanthrk29/Clustering_customer_invoice_data.git
   cd Clustering_customer_invoice_data
   ```
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Python script**
   ```bash
   python Clustering_customer_invoice_data.py
   ```

## 📊 Visualization & Insights
- **Scatter Plots** for DBSCAN clustering to identify patterns
- **Cluster Summary Reports** to analyze customer behavior
- **Comparative Analysis** of K-Means vs DBSCAN

## 🚀 Future Enhancements
🔹 Experiment with **Hierarchical Clustering** for better segmentation  
🔹 Apply **Deep Learning** models for feature extraction  
🔹 Develop a **Web Dashboard** for real-time customer insights  

## 🏆 Contributors
👨‍💻 **Your Name** – [GitHub Profile](https://github.com/Vasanthrk29)

## 📜 License
This project is licensed under the **MIT License**. Feel free to use and modify!
