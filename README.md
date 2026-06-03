# ☕ Starbucks Daily Updates — Power BI Dashboard

> A Power BI analytics dashboard built to monitor Starbucks daily business performance including sales, customer growth, order tracking, quantity sold, and user activity — all in one place.

---

## 📌 Project Overview

This dashboard provides a real-time snapshot of Starbucks daily operations. It was built using **Power BI Desktop** with a **500-user CSV dataset** and advanced **DAX queries** to deliver meaningful business insights for decision-making.

---
## 📊 Key Metrics & Features

| 📈 Metric | 💡 Description |
|---|---|
| **Daily Sales** | Total revenue generated each day |
| **New Customers** | How many new customers were added daily |
| **Order Count** | Total number of orders placed per day |
| **Total Quantity** | Units sold/consumed on a daily basis |
| **User Details** | Complete profile and activity of 500 users |
| **Last Order Update** | Most recent order status and timestamp |

---
## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard creation & visualization |
| **CSV File** | Raw data source (500 users dataset) |
| **DAX (Data Analysis Expressions)** | Custom KPIs and calculated measures |

---

## ⚙️ DAX Measures Used
```dax
-- Total Daily Sales
Daily Sales = CALCULATE(SUM(Orders[SalesAmount]), DATESINPERIOD(...))

-- New Customers Added
New Customers = CALCULATE(COUNTROWS(Users), Users[JoinDate] = TODAY())

-- Total Order Count
Order Count = COUNTROWS(Orders)

-- Total Quantity Sold
Total Quantity = SUM(Orders[Quantity])

-- Last Order Update
Last Updated = LASTDATE(Orders[UpdatedDate])
```
---
