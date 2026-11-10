# Customer Churn Analysis & Retention Dashboard

**Tools:** Python, Pandas, NumPy, SciPy, Matplotlib, Power BI, DAX, Power Query

## Project Overview

Customer churn is a major challenge for subscription-based businesses because losing customers can reduce recurring revenue and increase customer acquisition costs.

This project analyzes customer churn in a telecommunications company to understand customer retention patterns, identify high-churn segments, evaluate retention campaign opportunities, and quantify the financial impact of customer losses.

The project combines Python-based exploratory data analysis (EDA) with an interactive Power BI dashboard to translate customer data into actionable business recommendations.

## Problem Statement

The telecom company's retention and revenue assurance teams need data-driven answers to the following business questions:

- What proportion of customers leave the company?
- Which customer groups have the highest churn rates?
- How effectively could targeted retention campaigns reach customers who churned?
- How does revenue churn compare with customer churn?
- How do contract type, technical support, internet service, age group, and dependents relate to churn?
- How can management use these findings to prioritize retention activities?

The objective is to identify high-risk customer segments, measure the business impact of churn, and support better retention decisions.

## Dataset

**Dataset:** IBM Telco Customer Churn

**Source:** [IBM Telco Customer Churn Dataset](https://raw.githubusercontent.com/IBM/telco-customer-churn-on-icp4d/master/data/Telco-Customer-Churn.csv)

The dataset contains **7,043 customer records**, with one row per customer. The `Churn` column indicates whether a customer left the company.

### Key attributes

| Attribute | Description |
|---|---|
| `customerID` | Unique customer identifier |
| `gender` | Customer gender |
| `SeniorCitizen` | Indicates senior-citizen status |
| `Dependents` | Whether the customer has dependents |
| `tenure` | Number of months the customer has stayed |
| `Contract` | Contract type |
| `TechSupport` | Technical support subscription status |
| `InternetService` | Type of internet service |
| `PaymentMethod` | Customer payment method |
| `MonthlyCharges` | Customer's monthly charges |
| `TotalCharges` | Total charges recorded for the customer |
| `Churn` | Whether the customer left |

Other service attributes include online security, online backup, device protection, multiple lines, streaming TV, and streaming movies.

## Approach

### 1. Data Loading and Preparation
- Loaded the telecom customer dataset into Python using Pandas.
- Inspected the dataset structure, columns, and customer records.
- Reviewed data types and missing-value handling requirements.
- Prepared customer attributes for segmentation and analysis.

### 2. Exploratory Data Analysis
- Calculated the overall customer churn rate.
- Compared customer distribution, churn counts, and churn rates across contract types.
- Analyzed churn by technical support, gender, and senior-citizen status.
- Examined combinations of senior-citizen status, dependents, contract type, and streaming services.
- Used cross-tabulations and conditional probabilities to explore relationships between services and churn.

### 3. Retention Campaign Analysis
Compared potential campaign segments:
- Month-to-month contract customers
- Electronic-check payment customers
- Fiber-optic internet customers
- Combined customer segments

Evaluated campaign segments using their share of all churned customers and the proportion of customers within each segment who churned.

### 4. Revenue Churn Analysis
- Compared the average monthly charges of churned and retained customers.
- Examined monthly revenue associated with customers who churned.
- Compared revenue churn with customer churn to understand the financial impact of customer losses.

### 5. Statistical Analysis
- Used random customer samples to examine how observed churn rates vary with sample size.
- Simulated customer portfolios to explore variation in retention-agent outcomes.
- Simulated billing audits to investigate the sampling variability of average monthly charges.

### 6. Power BI Dashboard
The planned dashboard organizes the analysis into three pages:

- **Executive Overview:** Customer KPIs, churn rate, retention rate, and revenue at risk.
- **Churn Drivers:** Churn patterns across contracts, services, payment methods, and customer groups.
- **Retention Strategy:** Campaign segment comparisons, revenue impact, and recommended actions.

Power Query is used for data preparation, DAX for KPI calculations, and Power BI visuals for interactive business reporting.

## Key Insights

The following findings are documented in the analysis notebook.

### 1. Overall Customer Churn
- Total customers: **7,043**
- Customers who churned: **1,869**
- Customers who stayed: **5,174**
- Overall customer churn rate: **26.54%**

Approximately one in four customers in the dataset left the company.

### 2. Contract Type Is Strongly Associated with Churn
- Month-to-month customers represent approximately **55% of the customer base**.
- This segment accounts for approximately **86% of all churned customers** (1,655 of 1,869).
- Its churn rate is approximately **42%**, higher than the overall rate of 26.54%.
- Customers on two-year contracts have substantially lower churn than month-to-month customers.

**Business recommendation:** Evaluate renewal incentives, longer-term contract offers, and proactive retention campaigns for month-to-month customers.

### 3. Technical Support and Churn
- Customers without technical support have a churn rate of approximately **41%**.
- Customers with technical support have a churn rate of approximately **15%**.
- Customers without internet service have a churn rate of approximately **7%**.

**Business recommendation:** Investigate support experience and test proactive support engagement among high-risk customer groups. These associations do not establish that technical support alone causes lower churn.

### 4. Customer Demographics
- Senior citizens are approximately **1.7 times as likely to churn** as non-senior customers, according to the notebook's analysis.
- Dependents are associated with lower churn rates across age groups.
- Gender does not show a meaningful relationship with churn in this analysis.

**Business recommendation:** Investigate the needs and service experiences of senior customers, especially those without dependents, while prioritizing stronger churn indicators such as contract type.

### 5. Revenue Impact
The notebook examines average monthly charges for churned and retained customers and compares revenue churn with customer churn.

Revenue churn can differ from customer churn when departing customers have different average monthly charges from the overall customer base.

**Business recommendation:** Track monthly charges associated with churned customers alongside customer churn rate to understand the financial exposure of customer losses.

### 6. Retention Campaign Targeting
The notebook evaluates month-to-month contracts, electronic-check payments, fiber-optic internet, and combined targeting conditions.

Campaign selection should balance:
- Share of all churned customers reached
- Churn rate within the selected segment
- Number of customers contacted
- Campaign cost and potential retention value

The best target should be selected after comparing the segment metrics rather than assuming the largest or highest-churn segment is automatically the most cost-effective.

## Tools Used

| Tool | Purpose |
|---|---|
| Python | Data analysis and statistical exploration |
| Pandas | Data manipulation, aggregation, and cross-tabulation |
| NumPy | Numerical operations and sampling |
| SciPy | Statistical calculations |
| Matplotlib | Visualizing churn patterns and sampling distributions |
| Power BI | Interactive dashboard and business reporting |
| Power Query | Data cleaning and transformation |
| DAX | Customer churn, retention, and revenue KPIs |
| Jupyter Notebook | Analysis workflow and documentation |
| Git and GitHub | Version control and project sharing |

## Business Recommendations

1. Prioritize month-to-month customers for retention analysis.
2. Investigate whether proactive technical support can improve retention.
3. Compare the churn rate and revenue exposure of different customer segments.
4. Evaluate retention campaign segments using reach, churn concentration, and campaign cost.
5. Monitor both customer churn and revenue churn to support management decisions.
6. Validate campaign effectiveness using subsequent customer outcomes before claiming an improvement in retention.

## Project Structure

```text
customer-churn-analysis/
├── data/
│   └── README.md
├── notebooks/
│   └── customer_retention_analysis.ipynb
├── powerbi/
│   ├── customer_churn_dashboard.pbix
│   └── screenshots/
├── reports/
│   └── key_business_insights.md
├── README.md
├── requirements.txt
└── .gitignore
```

## Limitations

- The analysis is based on a single customer-level dataset rather than a time series of monthly customer snapshots.
- Observed relationships indicate association, not necessarily causation.
- Revenue associated with churned customers is an estimate of monthly billing exposure, not a confirmed measure of future revenue loss.
- Retention campaign effectiveness and financial returns require validation using actual campaign and post-campaign results.

## Conclusion

This project demonstrates how customer-level data can be used to investigate churn, evaluate retention campaign opportunities, and quantify revenue exposure. Combining Python EDA with Power BI reporting helps translate analytical findings into practical recommendations for business stakeholders.

---

**Author:** Vicky Ingle  
**Project Type:** Business Analytics | Customer Retention | Power BI Dashboard
