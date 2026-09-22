# Customer Segmentation using RFM Analysis and K-Means Clustering

This repository contains a Python Jupyter Notebook (`Sales analysis notebook.ipynb`) that performs customer segmentation on a retail sales dataset. By leveraging RFM (Recency, Frequency, Monetary) analysis and K-Means clustering, the project groups customers based on their purchasing behavior to help identify key customer profiles.

## Overview

The analysis processes transactional data to extract meaningful customer metrics, scales the features, and applies unsupervised machine learning to find distinct customer segments.

Key steps in the workflow include:

* **Data Cleaning:** Removing missing values, cancelled orders, and invalid quantities/prices.
* **RFM Feature Engineering:** Calculating Recency (days since last purchase), Frequency (number of purchases), and Monetary (total spend) for each customer.
* **Data Scaling:** Standardizing the RFM values using `StandardScaler` to ensure even feature weighting.
* **Optimal Cluster Selection:** Utilizing the Elbow Method to determine the ideal number of clusters.
* **Model Building:** Applying K-Means clustering (k=2) to segment the customer base.
* **Evaluation:** Assessing cluster quality using the Silhouette Score and Davies-Bouldin Index.

## Dataset

The project uses an Excel dataset named `sales2.xlsx`. The required columns for this analysis are:

* `Invoice`: Invoice number
* `Quantity`: Item quantity per transaction
* `InvoiceDate`: Date and time of the transaction
* `Price`: Unit price of the item
* `Customer ID`: Unique identifier for the customer

## Dependencies

To run this notebook, you will need the following Python libraries installed:

* `pandas`
* `scikit-learn`
* `matplotlib`
* `openpyxl` (required by pandas to read Excel files)

You can install these via pip:

```bash
pip install pandas scikit-learn matplotlib openpyxl
```

## Project Workflow

```text
Sales Dataset
      ↓
Data Loading
      ↓
Data Cleaning
      ↓
RFM Feature Engineering
      ↓
Data Scaling
      ↓
Elbow Method
      ↓
K-Means Clustering
      ↓
Customer Segmentation
      ↓
Cluster Evaluation
```

## RFM Analysis

RFM analysis is used to understand customer purchasing behavior through three key metrics:

### Recency

Measures how recently a customer made a purchase.

### Frequency

Measures how often a customer made purchases.

### Monetary

Measures the total amount spent by a customer.

These three metrics are used as the input features for customer segmentation.

## K-Means Clustering

The project uses **K-Means Clustering** to group customers with similar purchasing behavior.

The analysis uses:

```python
KMeans(n_clusters=2)
```

The RFM features are standardized before applying K-Means using:

```python
StandardScaler()
```

## Model Evaluation

The clustering results are evaluated using:

### Silhouette Score

Measures how well-separated and internally cohesive the clusters are.

### Davies-Bouldin Index

Measures the similarity between clusters. It is used to evaluate the quality of the generated customer segments.

## Key Learning Outcomes

Through this project, the following Machine Learning concepts were practiced:

* Data cleaning
* Feature engineering
* RFM analysis
* Data standardization
* Unsupervised Machine Learning
* K-Means clustering
* Elbow Method
* Customer segmentation
* Silhouette Score
* Davies-Bouldin Index
* Data analysis using Pandas
* Data visualization using Matplotlib

## Project Structure

```text
Customer-Segmentation/
│
├── Sales analysis notebook.ipynb
├── sales2.xlsx
└── README.md
```

## 🚀 How to Run the Project

### 1. Install Required Libraries

```bash
pip install pandas scikit-learn matplotlib openpyxl
```

### 2. Add the Dataset

Make sure the following file is available in the project directory:

```text
sales2.xlsx
```

### 3. Open the Notebook

Open:

```text
Sales analysis notebook.ipynb
```

using:

* Google Colab
* Jupyter Notebook
* VS Code

### 4. Run the Notebook

Execute the cells in order to perform:

1. Data loading
2. Data cleaning
3. RFM feature engineering
4. Data scaling
5. Elbow Method analysis
6. K-Means clustering
7. Customer segmentation
8. Cluster evaluation

## 👩‍💻 Author

**Karthikeyan R**

> BCA Student | Aspiring Full Stack Developer & Data Analyst
