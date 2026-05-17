# Customer Segmentation Analysis using RFM + K-Means Clustering

## Project Overview

This project performs **customer segmentation analysis** on online retail transaction data using:

- **RFM Analysis** (Recency, Frequency, Monetary)
- **K-Means Clustering**
- **Customer behavioral segmentation**

The goal is to identify meaningful customer groups that businesses can use for:

- Personalized marketing
- Customer retention strategies
- Revenue optimization
- Loyalty program targeting

---

## Dataset

Dataset used: **Online Retail II**

The dataset contains transactional data for a UK-based online retail store.

### Features include:

- Invoice Number
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

---

## Project Workflow

### 1. Data Loading

Loaded the dataset from Excel and selected the **2010–2011 transaction records**.

---

### 2. Data Cleaning

Performed preprocessing by:

- Removing missing Customer IDs
- Removing cancelled orders
- Removing negative/zero quantities
- Removing zero/negative prices
- Filtering transactions to **United Kingdom customers only**

---

### 3. Exploratory Data Analysis (EDA)

Analyzed:

- Transaction distributions
- Country distribution
- Revenue trends over time
- Top spending customers
- Quantity and pricing anomalies

---

### 4. Feature Engineering (RFM)

Created customer-level features:

### Recency
Days since last purchase

### Frequency
Number of unique purchases

### Monetary
Total amount spent

---

### 5. Data Transformation

Applied:

- Log transformation (`log1p`)
- Feature scaling using `StandardScaler`

This improved clustering performance by reducing skewness.

---

### 6. Optimal Cluster Selection

Used:

- **Elbow Method**
- **Silhouette Score**

to determine the optimal number of clusters.

Selected:

**K = 4**

---

### 7. K-Means Clustering

Segmented customers into 4 groups:

- **Champions**
- **Loyal Customers**
- **At-Risk Customers**
- **Lost Customers**

---

### 8. Customer Insights

## Champions
High spending, frequent purchases, recent activity

**Strategy:**  
Reward with VIP offers and exclusive promotions

---

## Loyal Customers
Consistent repeat buyers

**Strategy:**  
Upsell and cross-sell products

---

## At-Risk Customers
Previously active but becoming inactive

**Strategy:**  
Re-engagement campaigns

---

## Lost Customers
Low activity and low spending

**Strategy:**  
Win-back offers or reduced marketing spend

---

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- OpenPyXL

---

## Key Machine Learning Concepts Applied

- Unsupervised Learning
- K-Means Clustering
- Feature Scaling
- Log Transformation
- Silhouette Analysis
- Customer Segmentation

---

## Project Structure

```bash
customer-segmentation/
│
├── customer_segmentation.ipynb
├── online_retail_II.xlsx
└── README.md