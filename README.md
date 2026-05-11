# Marketing-Analytics_RFM
Segmented 5,878 UK e-commerce customers using RFM analysis on 1M+ transactions. Identified £2.4M CLV at risk in the At-Risk cohort, mapped churn rates across 5 segments (9%–100%), and produced prioritised retention recommendations using Python, pandas, and matplotlib.
# Customer Segmentation & Churn Risk Analysis
### RFM analysis on 1M+ UK e-commerce transactions

This project segments e-commerce customers using RFM (Recency, Frequency, Monetary) analysis, identifies churn risk by cohort, and estimates 2-year Customer Lifetime Value replicating the decision pipeline a marketing analytics team runs on a weekly basis.

**Dataset: ** [Online Retail II] (https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci) — UCI / Kaggle. Real UK gift retailer transactions, Dec 2009 – Dec 2011. ~1M rows after cleaning.

---

## Business question

> Which customers are most valuable, which are at risk of leaving, and where should retention investment be focused first?

---

## What I did

- Cleaned and preprocessed ~1M rows: removed cancellations, nulls, and negative quantities
- Engineered RFM scores (Recency, Frequency, Monetary) per customer using a snapshot date approach
- Segmented 5,878 customers into 5 cohorts: Champion, Loyal, At-Risk, Needs Attention, Lost
- Flagged churn risk (no purchase in 90+ days) per segment
- Estimated 2-year CLV per segment using avg order value × frequency × time horizon
- Translated findings into prioritised marketing recommendations

**Tools: ** Python, pandas, matplotlib, seaborn, numpy — Google Colab – 

---

## Key findings

| Segment | Customers | Churn rate | Est. 2-yr CLV |
|---|---|---|---|
| Champion | 1,738 | 9.2% | £15,672 |
| Loyal | 1,190 | 38.8% | £3,616 |
| At-Risk | 1,220 | 63.3% | £2,000 |
| Needs Attention | 1,155 | 88.3% | £795 |
| Lost | 575 | 100% | £354 |

**Finding 1: Champions dominate CLV. ** At £15,672 estimated 2-year value, Champions are worth 4x more than Loyal customers and 44x more than Lost ones. Protecting this segment is the single highest-ROI retention action.

**Finding 2: At-Risk is the urgent problem. ** 1,220 customers with 63% churn rate represent over £2.4M in potential CLV at risk. They were once active buyers - a targeted win-back campaign is the obvious intervention.

**Finding 3:  Loyal is more fragile than the label suggests. ** Nearly 4 in 10 Loyal customers are already churning - one bad experience away from sliding into At-Risk. Proactive engagement here prevents a much more expensive recovery later.

**Finding 4: Strong seasonality. ** Revenue peaks sharply in November–December (£1.1–1.2M), dipping to £450–600K the rest of the year. Acquisition campaigns should run September–October to capture customers *before* the seasonal spike, not during it.

---

## Charts

**Monthly revenue — seasonal pattern**
![Monthly Revenue](images/monthly_revenue.png)

**RFM customer segments**
![RFM Segments](images/rfm_segments.png)

**Churn rate by segment**
![Churn Rate](images/churn_by_segment.png)

**Estimated 2-year CLV by segment**
![CLV by Segment](images/clv_by_segment.png)

---

## Marketing recommendations

| Segment | Action | Rationale |
|---|---|---|
| Champion | Referral programme + early product access | Highest CLV, lowest churn — reward and leverage |
| Loyal | Upsell + cross-sell campaigns | High value, manageable churn — grow wallet share |
| At-Risk | Win-back email — personalised offer, time-sensitive | 63% churn but still recoverable — act within 2 weeks |
| Needs Attention | Re-engagement sequence + churn reason survey | Understand drop-off before investing in recovery |
| Lost | Final win-back attempt, then sunset/re-permission | 100% churn — low ROI, low effort spend only |

---

## About

Built as part of my MSc Marketing Analytics portfolio (EDHEC Business School).  
Focus area: translating customer data into retention and growth decisions.

[LinkedIn]( [Sindhuja Rao](https://www.linkedin.com/in/k-sindhuja-rao-1748b81a3/)) · [Email](sindhuja.kasuganti@edhec.com)

