# 🏦 Banking Transactions & Customer Financial Behavior Analysis

> **A data-driven framework using Python, SQL, and Power BI to decode customer financial behavior, reduce risk, and unlock revenue opportunities.**

---

## 📌 Project Overview

Financial institutions generate large volumes of transactional and customer data, but converting that data into actionable business decisions remains a challenge.

This project develops an **end-to-end banking analytics framework** using **Python, SQL, and Power BI** to analyze customer financial behavior, identify risk patterns, evaluate branch and channel performance, and support data-driven lending decisions.

The analysis addresses **five critical banking business challenges**:

* 🔴 Fraud exposure and anomalous transactions
* 💰 Revenue concentration and high-value customer retention
* 🏦 Loan approval and credit decision inefficiency
* 📊 Branch performance gaps
* 📱 Digital channel underutilization

The final solution combines **data cleaning, exploratory analysis, SQL analytics, feature engineering, and interactive Power BI dashboards** to transform raw banking data into actionable business intelligence.

---

## 🎯 Business Objectives

The project aims to help banking decision-makers:

1. Identify potentially fraudulent transactions using behavioral patterns.
2. Identify and retain high-value customers.
3. Improve loan approval decision-making using credit score segmentation.
4. Understand differences in branch-level revenue and performance.
5. Identify customer channel preferences and digital adoption opportunities.
6. Build executive and operational dashboards for continuous monitoring.

---

# 🏢 Business Challenges

### 01 — Fraud Exposure

Undetected fraudulent transactions can lead to financial losses and reduced customer trust.

The analysis identifies unusual transaction behavior based on:

* Transaction amount
* Customer spending patterns
* Geographic changes
* Transaction frequency
* Average ticket size

A rule-based fraud screening approach flags transactions that significantly deviate from normal customer behavior.

---

### 02 — Revenue Concentration Risk

A relatively small group of customers contributes a disproportionate share of transaction value.

This creates a retention risk because losing a small number of high-value customers can have a significant impact on revenue.

**Solution:**

* Rank customers by transaction value.
* Identify the highest-value customer segment.
* Develop targeted retention and relationship-management strategies.

---

### 03 — Loan Decision Inefficiency

Inconsistent lending decisions can create two problems:

* Rejecting creditworthy customers and losing potential revenue.
* Approving risky applicants and increasing default exposure.

Credit score segmentation provides a data-driven foundation for more consistent loan decision-making.

---

### 04 — Branch Performance Gaps

Branch-level analysis reveals significant differences in:

* Revenue
* Transaction volume
* Customer mix
* Operational performance

Top-performing branches can be analyzed to identify practices that may be replicated across lower-performing locations.

---

### 05 — Channel Underutilization

Customer activity varies significantly across banking channels.

Understanding channel preferences allows the bank to better align:

* Digital investment
* Product development
* Customer experience
* Fraud prevention
* Marketing strategies

---

# 🛠️ Technology Stack

| Technology                  | Purpose                                         |
| --------------------------- | ----------------------------------------------- |
| 🐍 **Python**               | Data cleaning, EDA, feature engineering         |
| 🗄️ **SQL**                 | Business queries, aggregation, decision metrics |
| 📊 **Power BI**             | Interactive dashboards and visualization        |
| 🐼 **Pandas**               | Data manipulation and transformation            |
| 🔢 **NumPy**                | Numerical analysis                              |
| 📈 **Matplotlib / Seaborn** | Exploratory data visualization                  |
| 🔧 **Git & GitHub**         | Version control and project management          |

---

# 🔄 Project Workflow

```text
Raw Banking Data
       ↓
Business Understanding
       ↓
Data Cleaning & Validation
       ↓
Exploratory Data Analysis
       ↓
Feature Engineering
       ↓
SQL Business Analysis
       ↓
Power BI Dashboard
       ↓
Business Insights
       ↓
Actionable Recommendations
```

The workflow ensures that business requirements defined at the beginning of the project directly influence the metrics, visualizations, and recommendations delivered at the end.

---

# 🧹 Data Engineering & Preparation

The data preparation process follows a structured six-step validation framework.

### 1. Missing Value Treatment

Missing values are handled according to column type:

* **Numerical fields:** Median-based imputation
* **Categorical fields:** Mode-based imputation

Blanket deletion is avoided to prevent unnecessary bias in the dataset.

### 2. Deduplication

Transaction-level duplicates are removed using composite uniqueness logic based on:

```text
Customer ID + Timestamp + Transaction Amount
```

This prevents duplicated transactions from artificially inflating financial metrics.

### 3. Type Normalization

Data types and formats are standardized for analytical compatibility.

Examples include:

* Date parsing
* Currency standardization
* Categorical normalization
* Numeric conversion

### 4. Feature Engineering

Additional analytical features are created, including:

* Transaction frequency
* Average transaction value
* Credit score bands
* Customer value segments
* Channel preference indicators

### 5. Outlier Detection

Potentially anomalous transactions are identified using:

* IQR-based detection
* Z-score analysis

Outliers are preserved for investigation rather than blindly removed.

### 6. Validation

Post-cleaning validation checks include:

* Row-count verification
* Null-rate analysis
* Data-range checks
* Duplicate verification
* Data-type validation

---

# 🔍 Exploratory Data Analysis

EDA was used to identify behavioral, financial, and operational patterns within the banking dataset.

## 📱 Transaction Channel Distribution

The analysis shows the following channel distribution:

| Channel        |   Usage |
| -------------- | ------: |
| Online Banking | **45%** |
| ATM            | **25%** |
| Mobile         | **18%** |
| Branch         | **12%** |

### Key Insight

**Online banking is the dominant transaction channel at 45%.**

This indicates that digital banking investment should remain a strategic priority, while the **18% mobile share** represents an opportunity for further digital adoption.

---

## 💰 Pareto Revenue Effect

Customer transaction value demonstrates a concentration pattern where a relatively small segment contributes a large proportion of total revenue.

### Business implication

High-value customers should receive:

* Dedicated relationship management
* Personalized product recommendations
* Proactive retention campaigns
* Premium banking opportunities

---

## 🏦 Branch Performance

Branch-level analysis identifies substantial differences between high-performing branches and the median branch.

Performance differences are influenced by factors such as:

* Customer composition
* Transaction volume
* Product mix
* Operational practices

This creates an opportunity to identify successful branch strategies and replicate them across the network.

---

## 🚨 Fraud Signal Clustering

Potentially anomalous transactions show patterns around:

* Unusually high transaction values
* New geographic locations
* Deviations from normal customer spending behavior
* Specific time periods

These patterns provide a foundation for rule-based fraud monitoring.

---

## 👥 Customer Segmentation

Behavioral analysis identifies two major customer profiles:

### High-Frequency / Low-Value

Potential strategy:

* Loyalty programs
* Rewards
* Cross-selling
* Digital engagement

### Low-Frequency / High-Value

Potential strategy:

* Premium banking services
* Personalized financial products
* Dedicated relationship management
* Private banking pathways

---

# 🗄️ SQL Analysis

SQL was used to transform cleaned transactional data into decision-ready business metrics.

## Key Queries

### 01 — Branch Revenue Ranking

Aggregates revenue by branch to identify:

* Top-performing branches
* Underperforming branches
* Revenue concentration

### 02 — High-Value Customer Identification

Customers are ranked based on total transaction value.

The highest-value segment is flagged for retention and relationship-management initiatives.

### 03 — Fraud Flagging Logic

Potentially suspicious transactions are identified using rules such as:

```text
Transaction Amount > 3 × Customer Average Ticket Size
```

or transactions originating from previously unseen geographic locations.

### 04 — Channel Preference by Segment

Customer segments are cross-tabulated against transaction channels to identify digital adoption gaps.

### 05 — Monthly Transaction Trends

Monthly aggregation is used to monitor:

* Transaction volume
* Transaction value
* Growth patterns
* Revenue trends

### 06 — Loan Approval Analysis

Loan approval rates are evaluated across credit score bands.

---

# 💳 Loan Approval Analysis

The analysis identified a strong relationship between credit score and historical approval rates.

| Credit Score Band | Approval Rate |
| ----------------- | ------------: |
| < 550             |       **22%** |
| 550–649           |       **41%** |
| 650–749           |       **68%** |
| 750+              |       **87%** |

### Key Insight

Approval rates increase significantly as credit scores improve.

The **750+ segment reaches an 87% historical approval rate**, while the **<550 segment has a 22% approval rate**.

This suggests that credit score banding can serve as an important input into standardized lending decision frameworks.

> **Note:** These historical approval rates should support decision-making rather than be treated as automatic approval rules. Real-world lending should incorporate additional risk, affordability, regulatory, and fairness considerations.

---

# 📊 Power BI Dashboard

The Power BI solution is designed for both **executive-level monitoring** and **operational decision support**.

## Dashboard Views

### 1. Executive Summary

Provides high-level KPIs including:

* Total revenue
* Transaction volume
* Active customers
* Loan approval rate

Designed to provide executives with a rapid overview of banking performance.

### 2. Branch Performance

Includes:

* Branch revenue ranking
* Transaction volume
* Geographic analysis
* Performance comparisons

### 3. Customer Segmentation

Analyzes customers based on:

* Transaction frequency
* Transaction value
* Customer tier

This helps relationship managers identify high-value customer groups.

### 4. Fraud Monitoring

Provides visibility into flagged transactions with filters such as:

* Date
* Branch
* Risk indicators
* Transaction characteristics

### 5. Channel Analytics

Tracks customer usage across:

* Online banking
* ATM
* Mobile
* Branch

This supports digital investment and channel strategy.

### 6. Loan Analysis

Provides loan approval analysis by:

* Credit score band
* Loan type
* Branch

This converts SQL analysis into an interactive decision-support layer.

---

# 💡 Key Business Recommendations

## 01 — Double Down on Digital

Online banking represents **45% of channel usage**.

Recommended actions:

* Improve online banking UX
* Expand digital features
* Strengthen digital fraud controls
* Increase mobile adoption

---

## 02 — Build a High-Value Customer Retention Program

Identify the highest-value customers and provide:

* Personalized offers
* Dedicated relationship management
* Premium products
* Proactive retention campaigns

---

## 03 — Improve Loan Decisioning

Use credit score bands as one component of a standardized lending framework.

Historical approval rates suggest:

* **750+:** 87% approval rate
* **650–749:** 68% approval rate
* **550–649:** 41% approval rate
* **<550:** 22% approval rate

This can help prioritize applications for automated processing or additional review while maintaining appropriate risk controls.

---

## 04 — Replicate Top Branch Practices

Analyze the characteristics of high-performing branches, including:

* Customer mix
* Product mix
* Transaction volume
* Staff practices

Create a structured playbook that can be tested across lower-performing branches.

---

## 05 — Strengthen Real-Time Fraud Detection

Integrate behavioral fraud rules into transaction monitoring.

Example:

```text
Flag transaction when:

Transaction Amount > 3 × Customer Average
                    OR
Transaction originates from a new geography
```

This enables faster compliance review and reduces dependence on batch-based analysis.

---

## 06 — Implement Segment-Driven Marketing

### High-frequency / low-value customers

Focus on:

* Rewards
* Loyalty programs
* Cross-selling
* Engagement campaigns

### Low-frequency / high-value customers

Focus on:

* Premium services
* Personalized products
* Relationship management
* Wealth/private banking opportunities

---

# 📈 Key Project Outcomes

This project demonstrates how banking data can be transformed from raw transactions into business decisions.

### The framework delivers:

* ✅ End-to-end data analytics workflow
* ✅ Validated and cleaned transactional data
* ✅ Customer behavioral analysis
* ✅ Fraud-risk identification framework
* ✅ Revenue concentration analysis
* ✅ Branch performance analysis
* ✅ Loan approval analysis
* ✅ Channel utilization analysis
* ✅ SQL-based decision metrics
* ✅ Interactive Power BI dashboards
* ✅ Actionable business recommendations

---

# 📁 Suggested Repository Structure

```text
Banking-Transactions-Customer-Financial-Behaviour-Analysis/
│
├── 📂 data/
│   ├── raw/
│   └── cleaned/
│
├── 📂 python/
│   ├── data_cleaning.py
│   ├── eda.py
│   └── feature_engineering.py
│
├── 📂 sql/
│   └── banking_analysis.sql
│
├── 📂 powerbi/
│   └── banking_dashboard.pbix
│
├── 📂 notebooks/
│   └── banking_analysis.ipynb
│
├── 📂 dashboard/
│   └── dashboard_screenshots/
│
├── README.md
└── requirements.txt
```

---

# 🚀 How to Use This Project

### 1. Clone the repository

```bash
git clone https://github.com/anuraghh88/-Customer-Financial-Behaviour-Analysis.git
```

### 2. Navigate to the project

```bash
cd -Customer-Financial-Behaviour-Analysis
```

### 3. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the analysis

Open the Jupyter Notebook or execute the Python scripts in the `python/` directory.

### 5. Explore the SQL analysis

Open:

```text
sql/banking_analysis.sql
```

and execute the queries against the cleaned dataset.

### 6. Open the Power BI dashboard

Open the `.pbix` file located in the `powerbi/` directory using Power BI Desktop.

---

# 📌 Skills Demonstrated

### Data Analytics

* Exploratory Data Analysis
* Customer segmentation
* Behavioral analysis
* Outlier detection
* Trend analysis
* KPI development

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Data cleaning
* Feature engineering

### SQL

* Aggregations
* CASE statements
* GROUP BY
* Window functions
* CTEs
* Ranking
* Business intelligence queries

### Power BI

* Dashboard development
* KPI cards
* Interactive filtering
* Drill-down analysis
* Data visualization
* Executive reporting

### Business Intelligence

* Fraud analytics
* Customer retention
* Revenue optimization
* Credit analysis
* Branch performance
* Channel strategy

---

# 👨‍💻 Author

**Anuraghh88**

Data Analytics Project — Banking Transactions & Customer Financial Behavior Analysis

---

⭐ **If you found this project useful, consider giving the repository a star!**
