Subscription Fatigue & Churn Risk Analysis
An end-to-end product and business analytics project using Python, SQL, and Tableau.

## Project Overview
Subscription-based products often experience churn due to declining engagement and excessive communication, commonly known as subscription fatigue.
This project analyzes user behavior to identify early signs of fatigue, classifies users by churn risk, and quantifies the revenue impact. The goal is to help product and business teams take proactive, data-driven retention decisions.

## Business Problem
Despite steady user acquisition, the business observed declining retention and renewals. Traditional acquisition funnels were insufficient to explain revenue loss, indicating issues after users subscribed.
Key questions addressed:
- Which users are showing signs of subscription fatigue?
- How does fatigue translate into churn risk?
- How much revenue is at risk due to potential churn?
- Which users should be prioritized for retention efforts?

## Data Description
The project uses simulated but realistic subscription data across multiple sources:
- users.csv: User-level details such as signup date and acquisition channel  
- subscriptions.csv: Subscription plans, start dates, and cancellation status  
- engagement.csv: Weekly user engagement metrics  
- communication.csv: Weekly push notification and email counts  
- revenue.csv: Monthly billing and payment information  
All datasets are linked using a common user_id.

## Tools & Technologies
- Python (pandas) – Data analysis and transformation  
- SQL (SQLite) – Joins, aggregations, and churn logic  
- Tableau Public – Dashboard and visualization  
- Google Colab – Development environment  
- CSV / Excel – Data storage format  

## Methodology
1. Data Integration  
   All datasets were loaded into a SQLite database and joined using SQL.
2. Fatigue Detection  
   Subscription fatigue was defined using:
   - Low engagement (≤ 1 session per week)
   - High communication pressure (≥ 5 push notifications per week)
3. Churn Risk Classification  
   Weekly fatigue signals were aggregated to user level:
   - 0 fatigue weeks → Low Risk  
   - 1 fatigue week → Medium Risk  
   - 2+ fatigue weeks → High Risk  
4. Revenue & LTV Analysis  
   User-level revenue and active duration were used to estimate Lifetime Value (LTV) and quantify revenue exposure.
5. Visualization  
   Insights were presented using interactive Tableau dashboards.

## Key Insights
- High-risk users contribute a disproportionate share of total revenue, indicating significant financial exposure.
- Repeated fatigue signals are associated with lower average lifetime value.
- Low-risk users show more stable engagement and revenue behavior.
- Fatigue indicators appear before churn, enabling early intervention.

## Tech Stack
- Python (Pandas, NumPy)
- SQL (data aggregation & joins)
- Tableau (data visualization & dashboards)

## Interactive Dashboard
Tableau Public Dashboard:  
https://public.tableau.com/app/profile/ishika.verma5181/viz/shared/KHRDDQ87W

## Business Recommendations
- Reduce notification frequency for users showing early fatigue signals.
- Prioritize high-risk users with high LTV for retention efforts.
- Improve onboarding and early engagement experience.
- Monitor fatigue indicators as part of ongoing retention strategy.

## Conclusion
This project demonstrates how behavioral data can be translated into actionable business insights. By linking engagement patterns to churn risk and revenue impact, it provides a practical framework for improving retention in subscription-based products.

## Project Structure
The repository is organized as follows:

Subscription-Fatigue-Analysis/

├── README.md                                                             # Project overview and business context
├── subscription_fatigue_analysis.ipynb                    # Python & SQL analysis notebook
├── users.csv                                                                    # User-level data
├── engagement.csv                                                       # Weekly engagement metrics
├── communication.csv                                                 # Push notification data
├── subscriptions.csv                                                     # Subscription details
├── revenue.csv                                                              # Billing and revenue data
├── user_summary.csv                                                  # Final user-level summary
├── revenue_risk.csv                                                     # Revenue at risk by churn segment
└── tableau_dashboard_link.txt                                   # Tableau Public dashboard URL
