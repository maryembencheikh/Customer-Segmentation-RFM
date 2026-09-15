# 🛍️ Online Retail Customer Segmentation

## 📌 Project Overview

This project focuses on customer segmentation using transactional retail data.

The objective is to identify distinct customer profiles based on their purchasing behavior, measure the business value of each segment, detect unusual customer behaviors, and translate the analytical results into actionable business strategies.

The project combines **RFM analysis, unsupervised Machine Learning, dimensionality reduction, anomaly detection, and business analytics** to build an end-to-end customer segmentation framework.

## 🎯 Business Objective

The main objectives of this project are to:

* Understand customer purchasing behavior
* Segment customers based on Recency, Frequency and Monetary Value (RFM)
* Identify high-value and at-risk customer segments
* Measure the revenue contribution of each segment
* Detect unusual customer behaviors
* Develop targeted business strategies for each customer segment
## 📊 Dataset

The project uses the **Online Retail dataset**, containing transactional data from a UK-based online retailer.

Each transaction provides information about customer purchases, including:

* Invoice number
* Product description
* Quantity
* Invoice date
* Unit price
* Customer ID
* Country

The dataset contains more than **500,000 transaction records** and provides a suitable basis for analyzing customer purchasing behavior.

## 🧹 Data Preparation

Before performing customer segmentation, the dataset was cleaned and prepared through several steps:

* Removed invalid and missing customer records
* Removed cancelled transactions where appropriate
* Checked and handled duplicate records
* Removed transactions with invalid quantities or prices
* Created the required customer-level features
* Identified and treated extreme values in the RFM variables

These steps ensured that the data used for segmentation was consistent and suitable for Machine Learning.

## 🛠️ Technologies & Tools

### Programming & Data Analysis

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical computations

### Data Visualization

* **Matplotlib**
* **Seaborn**

### Machine Learning

* **Scikit-learn**

  * K-Means Clustering
  * PCA
  * StandardScaler
  * Isolation Forest
  * Silhouette Score

### Development & Version Control

* **Jupyter Notebook**
* **Git & GitHub**

## 🔬 Methodology

The project follows an end-to-end customer segmentation workflow:

**RFM Analysis → Outlier Treatment → Standardization → K-Means Clustering → PCA → Customer Profiling → Revenue Analysis → Anomaly Detection → Business Recommendations**

### RFM Analysis

Customer behavior was summarized using **Recency, Frequency and Monetary Value (RFM)** to create customer-level purchasing profiles.

### Clustering

RFM features were standardized using **StandardScaler**, then segmented using **K-Means**. The optimal number of clusters was evaluated using the **Elbow Method** and **Silhouette Score**, resulting in **7 customer segments**.

### PCA & Customer Profiling

**PCA** was used to visualize the customer segments in a two-dimensional space and analyze the main patterns in the RFM features.

Each cluster was profiled according to customer count, RFM metrics, customer share and revenue contribution.

### Revenue & Anomaly Analysis

Revenue contribution was analyzed to identify high-impact customer segments.

**Isolation Forest** was then used to detect unusual customer behaviors within the RFM feature space.

### Business Recommendations

The analytical results were translated into targeted strategies:

* Customer retention
* Loyalty strategies
* Reactivation campaigns
* Upselling and cross-selling
* Customer development
* Selective win-back campaigns


## 📈 Key Results

The analysis identified **7 distinct customer segments** with significantly different purchasing behaviors and business value.

### 💰 Revenue Concentration

* **DELIGHT** represents only **5.27% of customers** but generates **44.68% of total revenue**.
* **PAMPER** represents **4.60% of customers** and contributes **14.76% of total revenue**.
* Together, these two segments represent only **9.87% of customers** but generate **59.44% of total revenue**.

This highlights a strong concentration of revenue among a relatively small group of high-value customers.

### 👥 Customer Segments

| Segment       | Business Profile                                          |
| ------------- | --------------------------------------------------------- |
| **DELIGHT**   | Highly active and extremely high-value customers          |
| **PAMPER**    | High-value customers requiring premium engagement         |
| **RE-ENGAGE** | Valuable customers showing signs of reduced activity      |
| **UPSELL**    | Active customers with strong growth potential             |
| **RETAIN**    | Customers requiring retention strategies                  |
| **NURTURE**   | Lower-value customers with development potential          |
| **REWARD**    | Highly inactive customers targeted for selective win-back |

### 🚨 Anomaly Detection

**Isolation Forest** identified **77 unusual customer profiles**, representing approximately **2% of the analyzed customer base**.

The **RE-ENGAGE** segment contained the majority of detected anomalies, with **60 out of 77 anomalies**.

These anomalies were not automatically considered negative. Some represented customers with relatively high historical value combined with increasing inactivity, making them potential targets for reactivation.

### 🎯 Strategic Prioritization

The segments were prioritized according to their business impact:

* **DELIGHT — CRITICAL:** Protect revenue
* **PAMPER — HIGH:** Increase loyalty
* **RE-ENGAGE — HIGH:** Reactivate valuable customers
* **UPSELL — HIGH:** Increase customer value
* **RETAIN — MEDIUM:** Improve retention
* **NURTURE — MEDIUM:** Develop customer value
* **REWARD — LOW:** Selective win-back

These results demonstrate how **unsupervised Machine Learning can transform transactional data into actionable business insights and strategic customer decisions**.

## 📊 Visualizations

The project includes several visualizations to support both the Machine Learning analysis and the business interpretation of the customer segments.

### Customer Segments in PCA Space
Visualization of the 7 customer segments after dimensionality reduction using PCA.
![alt text](image.png).

### Revenue Contribution by Customer Segment
Comparison of the revenue generated by each customer segment, highlighting the strong contribution of high-value customers.
![alt text](image-1.png)
### Customer Share vs Revenue Share
Comparison between the proportion of customers and the proportion of revenue generated by each segment.

This visualization highlights segments that contribute disproportionately to overall revenue.
![alt text](image-2.png)

### Strategic Prioritization
A business-oriented visualization combining customer share, revenue share and average monetary value to identify the strategic priority of each customer segment.
![alt text](image-3.png)

## 📁 Project Structure

```text
Online-Retail-Customer-Segmentation/
│
├── online-retail-clustering.ipynb
├── README.md
└── requirements.txt
```

### File Description

* **`online-retail-clustering.ipynb`** — Complete data analysis, customer segmentation, clustering, PCA, anomaly detection and business analysis.
* **`README.md`** — Project documentation and key results.
* **`requirements.txt`** — Python dependencies required to reproduce the project.

## ⚙️ Installation & Usage

### 1. Clone the repository

```bash
git clone https://github.com/maryembencheikh/Customer-Segmentation-RFM.git
cd Online-Retail-Customer-Segmentation
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Launch the notebook

```bash
jupyter notebook
```

Then open:

```text
online-retail-clustering.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and customer segmentation workflow.

## 📌 Conclusion

This project demonstrates how **Data Science and Machine Learning can transform transactional retail data into actionable customer insights**.

By combining **RFM analysis, K-Means clustering, PCA, anomaly detection and revenue analysis**, the project identifies distinct customer segments and translates their behaviors into targeted business strategies.

The results highlight the importance of combining **technical analysis with business understanding** to support data-driven customer management and revenue optimization.
