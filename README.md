
# End-to-End-Loan-Risk-Analytics-Project-Using-Dataflow

# Loan Default Risk Analytics Dashboard

## Project Overview

This project focuses on analyzing loan default behavior using Power BI, SQL Server, Power Query, DAX, and Dataflow integration.

The dashboard helps identify:
- Loan default trends
- Risk patterns
- Customer financial behavior
- Employment-based risk analysis
- Credit score impact
- Year-over-year financial changes

The complete workflow includes:
- SQL Server integration
- Power BI Dataflow creation
- Data cleaning using Power Query
- DAX measure creation
- Interactive dashboard development
- Financial risk analysis

---

# Tech Stack

| Tool | Purpose |
|---|---|
| Power BI | Dashboard Development |
| Power Query | Data Cleaning & Transformation |
| DAX | KPI & Measure Calculations |
| SQL Server | Data Storage & Connection |
| Power BI Service | Dataflow & Refresh Setup |
| CSV Dataset | Source Data |

---

# Project Workflow

## 1. Data Collection
- Imported Loan Default CSV dataset
- Connected dataset with SQL Server
- Configured SQL Authentication

## 2. Data Transformation
Performed data cleaning using Power Query:
- Null value handling
- Data type correction
- Column validation
- Calculated columns
- Data profiling

## 3. Dataflow Implementation
- Created Dataflow in Power BI Service
- Imported data into Power BI Desktop from Dataflow
- Configured scheduled refresh

## 4. DAX Development
Created multiple DAX measures for:
- Default Rate %
- YOY Loan Change
- Average Income Analysis
- Median Loan Analysis
- Credit Score Segmentation
- Risk Metrics
- Employment Analysis

## 5. Dashboard Development
Designed 3 interactive dashboard pages:
- Loan Default & Overview
- Applicant Demographics & Financial Profile
- Financial Risk Metrics

---

# Dashboard Pages


## 📊 Analytics Deep-Dive & Executive Insights

### 1. Core Portfolio & Default Overview
*   **Capital Allocation Trends:** Loan issuance is consistently balanced across functional categories. Home loans comprise the largest deployment segment at **$6,545M**, while the lowest allocation is categorized under Miscellaneous/Other at **$6,498M**.
*   **Income Stability Paradox:** Average annual income remains homogeneous across all work classifications, floating between **$82,272 (Self-employed)** and **$82,890 (Full-time)**.
*   **Employment Risk Dispersion:** Despite stable income profiles, default behaviors vary dramatically. **Unemployed individuals carry the highest structural risk with a 3.39% default rate**, followed heavily by Full-time employees at **3.01%**. Conversely, Part-time workers display the strongest repayment discipline with a default rate low of **2.36%**.
*   **Macro Default Cycle:** Loan default tracking shows a distinct cyclical volatility. Sharp risk spikes peaked in **2015 (11.70%)** and **2016 (11.75%)** before aggressively correcting to a cyclical low of **11.50% in 2017**.

### 2. Applicant Demographics & Credit Profiles
*   **Credit Score Elasticity:** Median loan amounts decrease progressively as credit rating deteriorates. Low-risk tiers request a median size of **$128,397 (Low Default Probability Tier)**, contracting down to **$127,149 for High-risk applicant tiers**.
*   **High-Credit Portfolio Demographics:** Within the elite credit segment, capital allocation is heavily driven by **Single Applicants ($128.57K / 8.43%)** and **Married Applicants ($128.35K / 8.42%)** within younger adult demographics.
*   **Volume Distribution by Education:** Loan volume is distributed equally across educational tiers. **Bachelor's degree holders account for the highest transactional volume (64,366 loans)**, while Master's and PhD brackets maintain stable, slightly lower totals (~63.5K to 63.9K).

### 3. Financial Risk Metrics & Volume Variances
*   **Year-Over-Year (YOY) Capital Volatility:** Capital disbursement underwent massive swings, dropping to a negative growth rate of **-1.53% in 2014**, before experiencing a sharp resurgence to a peak growth rate of **+1.73% in 2018**.
*   **YOY Default Correlation:** Net defaults do not map linearly to total volume. A massive default escalation occurred in **2015 (+2.7 growth variance)**, aligning directly with the historical macro cycle peak.
*   **Decomposition Tree Analysis:** Dissecting the total high-income loan portfolio volume (**$32.58bn**) reveals a perfectly uniform distribution across working sectors. High-income capital splits evenly across **Full-time ($5.44bn)**, **Part-time ($5.44bn)**, and **Self-employed ($5.43bn)** human capital sectors.


# Important DAX Measures Used

## Default Rate
```DAX
Default Rate =
DIVIDE(
    COUNTROWS(FILTER(Loans, Loans[Default] = "Yes")),
    COUNTROWS(Loans)
)
```

## Average Loan Amount
```DAX
Average Loan Amount = AVERAGE(Loans[LoanAmount])
```

## YOY Loan Change
```DAX
YOY Loan Change =
CALCULATE(
    [Total Loan Amount] - [Previous Year Loan Amount]
)
```

## Median Loan Amount
```DAX
Median Loan Amount = MEDIAN(Loans[LoanAmount])
```

---

# Dataset Information

## Dataset Used
Loan Default Dataset containing:
- Customer demographics
- Credit score
- Income details
- Employment type
- Loan purpose
- Default information
- Marital status
- Mortgage/dependent details

---

# Screenshots

## Dashboard Preview

### Loan Default & Overview


### Applicant Demographics & Financial Profile
(Add Screenshot Here)

### Financial Risk Metrics
<img width="1295" height="729" alt="Risk Metrics" src="https://github.com/user-attachments/assets/03f6a93b-820d-4407-b606-b29f4fb7d10b" />


---

# Learning Outcomes

Through this project, I learned:
- Power BI Dataflow integration
- SQL Server connectivity
- Advanced DAX calculations
- Power Query transformations
- Interactive dashboard design
- Financial risk analysis
- KPI development
- Data storytelling techniques
- Scheduled refresh implementation

---

# Business Impact

This dashboard can help financial institutions:
- Identify high-risk borrowers
- Improve loan approval strategies
- Monitor default patterns
- Analyze financial risk trends
- Understand customer segmentation
- Support data-driven lending decisions

---

# 🤝 Connect With Me

Feel free to reach out to discuss data engineering pipelines, advanced Power BI modeling, or financial analytics!

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/donthula-charan-kumar/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/charankumar08)

---
*Project engineered as part of a Professional Data Analyst Portfolio.*
