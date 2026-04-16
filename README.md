# Credit Score Analysis — Financial Behaviour Study
**Tools Used:** Python (Pandas) | SQL (SQLite)
**Domain:** Banking, Financial Services & Insurance (BFSI)
**Dataset:** Credit Score Classification Dataset — Kaggle

---

## Problem Statement
Credit scores are the backbone of lending decisions in the Indian banking 
sector. A wrong credit assessment directly leads to NPAs and financial losses.
This project analyses 44,568 customer records to understand what financial 
behaviours drive Good vs Poor credit scores and identify high-risk customer 
segments for proactive intervention.

---

## Key Business Insights

### 1. Credit Score Distribution
| Credit Score | Customers | Percentage |
|--------------|-----------|------------|
| Standard     | 23,546    | 52.83%     |
| Poor         | 13,870    | 31.12%     |
| Good         | 7,152     | 16.05%     |

- Only 16% of customers have a Good credit score
- Nearly 1 in 3 customers (31%) fall in the Poor category
- Recommendation: Banks must focus on converting Standard → Good 
  customers through financial literacy and structured repayment plans

### 2. Financial Profile — Good vs Poor Credit Customers
| Metric                | Good Score | Poor Score |
|-----------------------|------------|------------|
| Avg Annual Income     | ₹1,97,063  | ₹1,67,144  |
| Avg Monthly Salary    | ₹5,273     | ₹3,242     |
| Avg Outstanding Debt  | ₹821       | ₹2,138     |
| Avg Days Delayed      | 11 days    | 30.4 days  |
| Avg Monthly EMI       | ₹1,563     | ₹1,407     |

- Good score customers earn 18% more annually than Poor score customers
- Poor score customers carry 2.6x more outstanding debt
- Payment delay is the strongest differentiator — Good customers 
  delay by only 11 days vs 30 days for Poor customers

### 3. Credit Score by Occupation
- Teachers have the highest Good score rate at 17.70%
- Writers have the lowest Good score rate at only 12.02%
- Entrepreneurs show the highest Poor score concentration
- Insight: Occupation is a meaningful proxy for financial stability 
  and should be weighted in credit scoring models

### 4. Impact of Payment Delays
- Good score customers delay payments by avg 11 days
- Poor score customers delay by avg 30.4 days — nearly 3x more
- Outstanding debt of Poor customers (₹2,138) is 2.6x that of 
  Good customers (₹821)
- Recommendation: Early warning triggers should fire at 15+ days 
  delay to prevent credit score deterioration

### 5. Bank Accounts vs Credit Score
| Bank Accounts | Customers | Good Score % |
|---------------|-----------|--------------|
| Low (1-2)     | 5,272     | 45.60%       |
| Medium (3-5)  | 15,400    | 23.08%       |
| High (6+)     | 23,896    | 4.99%        |

- Customers with 1-2 bank accounts have a 45.60% Good score rate
- Customers with 6+ accounts have only 4.99% Good score rate
- Insight: Too many bank accounts signals financial stress and 
  correlates strongly with Poor credit behaviour

### 6. Payment Behaviour Impact
- High spend + Large value payments = best Good score rate (21.37%)
- Low spend + Small value payments = worst profile (38.63% Poor rate)
- Customers making small value payments consistently are 3.5x more 
  likely to have a Poor credit score
- Recommendation: Flag Low_spent_Small_value_payments customers 
  for proactive outreach before they deteriorate further

### 7. High Risk Customer Segments
- Very High Risk = Delayed Payments > 15 + Outstanding Debt > ₹1,000 
  + Credit Utilization > 30%
- Media Managers and Mechanics appear most frequently in the 
  Very High Risk Poor score segment
- These customers show outstanding debt as high as ₹4,997 with 
  24+ delayed payments

---

## Key Recommendations for BFSI Risk Teams
1. Flag customers with 6+ bank accounts for enhanced credit review 
   — only 5% achieve Good scores
2. Trigger early intervention at 15 days payment delay — 
   before the 30-day threshold that defines Poor score customers
3. Weight payment behaviour in credit models — 
   Low_spent_Small_value customers default at 38.63%
4. Target Standard score customers (52.83%) with structured 
   repayment plans to convert them to Good — largest opportunity segment
5. Use income + outstanding debt ratio as primary risk filter — 
   Poor customers carry 2.6x more debt on 18% lower income

---

## Project Structure
credit-score-analysis/
│
├── train.csv                          # Original dataset
├── credit_score_analysis.ipynb        # Jupyter notebook with all code
└── README.md                          # Project documentation

---

## Tools & Skills Demonstrated
- Data Cleaning with Pandas
- SQL queries — CASE statements, GROUP BY, aggregations, subqueries
- Customer segmentation using multi-condition risk logic
- Business insight generation from financial behaviour data
- Executive summary reporting
