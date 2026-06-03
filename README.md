<img width="1440" height="6290" alt="image" src="https://github.com/user-attachments/assets/ffd62d32-02a5-4e5d-99d0-01f6b187c40a" /># ☕ Starbucks Daily Updates — Power BI Dashboard

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
## 📁 Project Structure

```
Starbucks_Daily_Updates/
├── starbucks.pbix          ← Main Power BI Dashboard file
├── data/
│   └── starbucks_users.csv ← 500 users dataset (CSV)
├── screenshots/
│   └── dashboard.png       ← Dashboard preview image
└── README.md
```

---
## 🖼️ Dashboard Preview

![Starbucks Dashboard]("dashboard.png")

> 📸 *Add dashboard screenshot in the screenshots/ folder*

---

## 🚀 How to Run This Project
1. **Clone the repository**
   ```bash
   git clone https://github.com/ruderapratap/Starbucks_Daily_Updates.git
   ```

2. **Open the file** in Power BI Desktop
   ```
   starbucks.pbix
   ```

3. **Update data source path** if CSV is not auto-detected:
   - Go to `Home → Transform Data → Data Source Settings`
   - Point it to your local `starbucks_users.csv` file

4. **Click Refresh** to load the latest data ✅

---
## 📂 Dataset Info

- **Total Records:** 500 users
- **Format:** CSV
- **Columns Include:** User ID, Customer Name, Join Date, Order Date, Sales Amount, Quantity, Order Status, Last Updated

---

## 👨‍💻 Author

**Rudera Pratap**
- 🔗 GitHub: [@ruderapratap](https://github.com/ruderapratap)

---
## ⭐ Support

If you found this project helpful, please give it a **star** ⭐ on GitHub!

---

## 📄 License

This project is open source — feel free to use and modify for learning purposes.
