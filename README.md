# RavenStack: Customer Retention & Revenue Risk Analysis

Bootcamp case study (Dibimbing Data Analyst Bootcamp). Identifies who is churning, why, and how much recurring revenue is at risk for RavenStack, a SaaS company with 500 customers, using SQL, Python, and Tableau.

**Full portfolio write-up with dashboard:** [Notion](https://concrete-kidney-703.notion.site/RavenStack-Customer-Retention-Revenue-Risk-Analysis-3c33c020afa8806fb241c8dae47ddc35)
**Interactive dashboard:** [Tableau Public](LINK_TABLEAU_PUBLIC_KAMU)

## Business Questions

1. Who is churning? (by industry and plan tier)
2. Which factors are associated with churn? (engagement, satisfaction, support)
3. How much revenue is affected by churn, and why are customers leaving?

## Method

- **SQL:** data preparation and analysis across four areas: customer and revenue, engagement, support, and churn and revenue impact.
- **Python:** data connection and merging, missing value investigation, exploratory data analysis, feature engineering, correlation analysis with heatmap, and supporting visualizations.
- **Tableau:** KPI dashboard covering Net MRR trend, churn by segment, churn vs engagement, churn vs satisfaction, and revenue impact by churn reason.

## Result

| Metric | Value |
|---|---|
| Total customers | 500 |
| Active customers | 390 |
| Churned customers | 110 |
| Churn rate | 22.00% |
| Recurring revenue | 1,214,351 |
| Revenue at risk | 157,461 |

**Key findings**

- Churn is concentrated in specific segments: DevTools - Enterprise is highest at 37.14%, while EdTech - Enterprise is lowest at 4.17%.
- Churn peaks in the Q3 engagement tier (28.80%), so higher usage alone does not guarantee retention.
- Satisfaction is not a strong predictor of churn: high-rated customers churned at 23.16%, versus 19.74% for low-rated customers.
- Top churn reasons by revenue lost: support (37K), budget (35K), and pricing (34K).

## Recommendations

1. **Prioritize retention programs for DevTools - Enterprise.** Its churn rate (37.14%) is well above the 22.00% average, and Enterprise accounts usually carry higher contract value, so each lost account weighs more on revenue. Investigating the specific needs of this segment should give the largest impact on reducing revenue at risk.
2. **Build an early warning system based on behavioral signals, not just complaints.** Satisfaction ratings alone are a weak signal: customers with no rating (23.53%) and high ratings (23.16%) churned at similar rates. Flagging accounts that stop giving feedback or show declining activity is more reliable than waiting for support tickets.
3. **Investigate the root causes behind support, budget, and pricing.** These three reasons contribute almost equally to revenue impact, so improvements likely need to address more than one area at once, for example reviewing support response and resolution quality while checking whether pricing matches the value customers perceive in each tier.
4. **Make retention a KPI on par with acquisition.** Churned MRR grows as the business grows, and churn is easy to treat as a reactive issue handled only after problems escalate. Tracking target churn rate and revenue at risk as regular metrics will help RavenStack sustain net revenue growth.

## Repository Structure

```
ravenstack-customer-retention-analysis/
├── sql/
│   └── queries.sql        # SQL analysis (customer/revenue, engagement, support, churn impact)
├── notebooks/
│   └── analysis.ipynb     # Python data cleaning, EDA, and visualization
└── README.md
```

## Tools

SQL, Python (pandas, matplotlib/seaborn), Jupyter Notebook, Tableau

## Data

[RavenStack SaaS Subscription & Churn Analytics Dataset (Kaggle)](https://www.kaggle.com/datasets/rivalytics/saas-subscription-and-churn-analytics-dataset)
