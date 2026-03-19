# ElectroSales Analytics: Data-Driven Retail Performance Dashboard  

![Electronic sales](https://github.com/user-attachments/assets/1d03a5ee-beb1-4043-a2db-7852f4842d46)


# 🖥️ ElectroSales Analytics – Retail Performance Dashboard

> **Role:** Data Analyst | **Tools:** Power BI · DAX · Power Query · Excel | **Domain:** Retail · Electronics · Sales Analytics

---

##  Project Overview

Built an **end-to-end Power BI sales analytics dashboard** for a fictional electronics retailer — transforming raw transactional data into executive-ready insights. The dashboard provides leadership with complete visibility into **revenue trends, top-performing salespeople, high-value customers, regional performance, and payment behavior** — all on a single interactive page.

---

##  Business Problem

Retail leadership lacked a centralized analytics solution to answer critical business questions:

- **When do sales peak and dip** — and how should campaigns align with these patterns?
- **Who are the top salespeople** — and who needs support or incentivization?
- **Which customers drive the most revenue** — and how do we retain them?
- **Which regions underperform** — and where should we invest to grow?
- **What payment methods do customers prefer** — and how do we optimize checkout experience?

---

## 📊 Key KPIs & Metrics

| Metric | Value |
|---|---|
| Peak Revenue Month | December — $67K |
| Second Peak Month | June — $56K |
| Lowest Revenue Month | February — $20K |
| Top Salesperson | Nancy Freehafer — $104K |
| Top Customer | Cust-D — $67K |
| Best Region | North — $142K |
| Credit Card Payments | $259K (60% of all transactions) |

---

##  Key Findings

### Revenue by Month
| Period | Revenue | Insight |
|---|---|---|
| December | $67K — Peak | Year-end spending surge |
| June | $56K — Peak | Mid-year promotional lift |
| February | $20K — Low | Weakest month — promotional opportunity |
| April | $21K — Low | Second weakest — needs targeted campaign |

### Revenue by Salesperson
| Salesperson | Revenue | Rank |
|---|---|---|
| Nancy Freehafer | $104K | 🥇 #1 |
| Anne Larsen | $94K | 🥈 #2 |
| Andrew Cencini | $67K | 🥉 #3 |

- **Top 3 salespeople drive the majority of total revenue** — clear case for incentive programs and script replication

### Revenue by Customer
| Customer | Revenue |
|---|---|
| Cust-D | $67K |
| Cust-H | $50K |
| Cust-BB | $44K |

- High-value customers are concentrated — **retention programs targeting top 3 clients** can significantly protect revenue

### Revenue by Region
| Region | Revenue | Status |
|---|---|---|
| North | $142K | ✅ Best performer |
| East | $108K | ✅ Strong |
| South | $94K | ⚠️ Growth potential |
| West | $91K | ⚠️ Needs investment |

### Revenue by Payment Type
| Payment Method | Revenue | Share |
|---|---|---|
| Credit Card | $259K | 60% |
| Check | $129K | 30% |
| Cash | $47K | 11% |

- Credit cards dominate — **improving digital payment experience** can capture remaining cash/check customers

---

##  Strategic Recommendations

| Area | Recommendation |
|---|---|
| Seasonal Campaigns | Launch promotions in February and April to lift low-revenue months |
| Inventory Planning | Stock up for December and June peak periods |
| Sales Team | Incentivize top performers and replicate Nancy's approach across the team |
| Customer Retention | Create VIP programs for Cust-D, Cust-H, and Cust-BB |
| Regional Investment | Increase marketing spend in South and West regions |
| Payments | Streamline digital payment experience to convert cash and check users |
| Reporting | Use this dashboard as a **recurring monthly sales health check** |

---

##  Technical Approach

### Power BI
- **Star schema** data model — Customer, Sales, Product, and Region tables connected via keys
- **DAX measures** for monthly revenue, MoM growth, top N salesperson ranking, and payment share
- **Revenue binning** — transactions grouped into size buckets for distribution analysis
- **Interactive slicers** for month, region, salesperson, and payment type
- **Single-page executive dashboard** designed for leadership readability
- **KPI cards** for instant visibility into top-line metrics

### Power Query
- ETL pipeline for data cleaning, transformation, and normalization
- Null handling, data type standardization, and date dimension creation
- Customer and salesperson ID mapping for relationship building

### SQL Logic Applied (Simulated)
```sql
-- Top Salespeople by Revenue
SELECT
    salesperson_name,
    SUM(revenue) AS total_revenue,
    RANK() OVER (ORDER BY SUM(revenue) DESC) AS sales_rank
FROM sales
GROUP BY salesperson_name;

-- Monthly Revenue Trend
SELECT
    FORMAT(sale_date, 'yyyy-MM') AS month,
    SUM(revenue) AS monthly_revenue,
    LAG(SUM(revenue)) OVER (ORDER BY FORMAT(sale_date, 'yyyy-MM')) AS prev_month,
    SUM(revenue) - LAG(SUM(revenue)) OVER (ORDER BY FORMAT(sale_date, 'yyyy-MM')) AS MoM_change
FROM sales
GROUP BY FORMAT(sale_date, 'yyyy-MM');
```

---

##  Challenges Faced & Solutions

| Challenge | Solution |
|---|---|
| Data Modeling from scratch | Built star schema with proper relationships in Power BI |
| DAX Complexity | Created accurate KPIs for bins, Top N filtering, and trend logic |
| Visual Clarity | Simplified overcrowded visuals for executive-level readability |
| Simulated Data | Designed realistic business scenarios from a fictional dataset |

---

##  Repository Structure
```
📂 Electronics-Sales-Analysis-Dashboard
├── 📊 ElectroSales_Dashboard.pbix      — Interactive Power BI dashboard
├── 📄 SalesData.csv                    — Simulated electronics sales dataset
├── 🖼️  Electronics Sales Dashboard.jpg  — Dashboard preview screenshot
└── 📄 README.md                        — Project documentation
```

---

##  Dashboard Preview

![Electronics Sales Dashboard](Electronics%20Sales%20Dashboard.jpg)

---

##  About

**Khurram Naveed** — Data Analyst specializing in Power BI, SQL, and business intelligence.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/khurramnaveed3233)
[![GitHub](https://img.shields.io/badge/GitHub-Portfolio-black?logo=github)](https://github.com/Khurramnaveed3233)
[![Email](https://img.shields.io/badge/Email-Contact-red?logo=gmail)](mailto:khurramnaveed4545@gmail.com)

---

>  *This project demonstrates end-to-end Power BI dashboard development — from raw data modeling to executive-ready visual storytelling — proving that structured analytics can transform retail data into direct revenue and operational decisions.*

---

⭐ *If you are a recruiter or hiring manager — I am actively seeking Data Analyst and Business Intelligence roles. Let's connect!*
