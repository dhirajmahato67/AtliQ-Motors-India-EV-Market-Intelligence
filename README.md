# ⚡ AtliQ Motors — India EV Market Intelligence

> **An end-to-end Microsoft Fabric data analytics solution to evaluate India's EV market, identify high-potential markets, forecast growth, and recommend a market-entry strategy for AtliQ Motors.**

![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-Data%20Platform-blue)
![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow)
![PySpark](https://img.shields.io/badge/PySpark-Data%20Transformation-orange)
![SQL](https://img.shields.io/badge/SQL-Analytics-blue)
![Azure SQL](https://img.shields.io/badge/Azure%20SQL-Database-0078D4)
![Data Engineering](https://img.shields.io/badge/Data%20Engineering-ETL-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📌 Executive Summary

AtliQ Motors is a leading automotive company headquartered in the USA with approximately **25% market share in the electric and hybrid vehicle segment in North America**.

As part of its international expansion strategy, AtliQ Motors plans to enter the Indian EV market, where its current market share is **below 2%**.

Before investing in manufacturing, distribution, marketing, and product launches, the leadership team needs to understand:

- Where EV demand is strongest
- Which states have the highest EV penetration
- Which manufacturers dominate the market
- How EV sales are evolving over time
- Which states have the strongest growth potential
- When demand peaks and declines
- Where AtliQ Motors should establish manufacturing operations
- How government incentives and charging infrastructure influence adoption
- Which customer and marketing strategies can accelerate adoption

This project was developed as an **end-to-end data and business intelligence solution** to answer these questions and provide actionable recommendations to AtliQ Motors leadership.

---

# 🎯 Business Objective

The primary objective is to help **Bruce Haryali, Chief of AtliQ Motors India**, make a data-driven decision regarding the company's entry into the Indian EV market.

The solution combines:

**Data Engineering + Data Transformation + Data Warehousing + Business Intelligence + Market Research + Forecasting**

to transform raw EV data into strategic business recommendations.

---

# 🏢 Business Problem

AtliQ Motors has successfully established itself in the North American EV and hybrid vehicle market.

However, entering India presents several strategic challenges:

- Highly competitive EV market
- Different adoption patterns across states
- Significant variation in EV penetration
- Strong presence of established local manufacturers
- Differences in government incentives and policies
- Uneven charging infrastructure
- Different consumer preferences
- State-level differences in manufacturing attractiveness
- Uncertainty around future EV demand

A simple dashboard would not be sufficient.

AtliQ Motors needed a **scalable analytics pipeline** capable of continuously transforming raw data into reliable business insights.

---

# 💡 Solution Approach

I designed an end-to-end Microsoft Fabric analytics architecture following a **Medallion Architecture**:

```text
Azure SQL Database
        │
        ▼
    Raw Data
        │
        ▼
┌──────────────────┐
│ Bronze Layer     │
│ Raw / Source Data│
└──────────────────┘
        │
        ▼
   Fabric Pipeline
        │
        ▼
┌──────────────────┐
│ Silver Layer     │
│ Cleaned &        │
│ Transformed Data │
└──────────────────┘
        │
        ▼
     PySpark
   Transformations
        │
        ▼
┌──────────────────┐
│ Gold Layer       │
│ Business-Ready   │
│ Analytical Data  │
└──────────────────┘
        │
        ▼
     Warehouse
        │
        ▼
   Semantic Model
        │
        ▼
     Power BI
        │
        ▼
Business Intelligence
& Strategic Decisions
