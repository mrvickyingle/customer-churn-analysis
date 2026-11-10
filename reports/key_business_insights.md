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
