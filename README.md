# Amazon-Sales-Intelligence-Dashboard-Excel


---
  
## An interactive Excel dashboard analyzing **100 Amazon orders** across 5 regions and 5 product categories — covering sales performance, delivery speed, and cancellation trends, built with pivot tables, XLOOKUP, conditional formatting, and a consolidated dashboard.

---

## Dashboard Preview


<img width="1239" height="761" alt="WhatsApp Image 2026-08-14 at 10 47 23 PM" src="https://github.com/user-attachments/assets/0877c6bb-4e3e-49e3-9c12-cbb81ac9f733" />

**Main Dashboard**


---

<img width="666" height="647" alt="WhatsApp Image 2026-08-14 at 10 47 59 PM" src="https://github.com/user-attachments/assets/d080e2fb-df29-4652-a36d-63d10c4dbc80" />

**Region-wise Product Sales**



---

<img width="919" height="411" alt="WhatsApp Image 2026-08-14 at 10 48 23 PM" src="https://github.com/user-attachments/assets/65ce48af-df83-4746-a86c-f5d404db4666" />


**Monthly Sales Trend**


---


<img width="995" height="260" alt="image" src="https://github.com/user-attachments/assets/b48a0a16-72a7-40cb-840f-d167a4410164" />


**Cancellation Rate by Region**




---

<img width="649" height="511" alt="WhatsApp Image 2026-08-14 at 10 48 38 PM" src="https://github.com/user-attachments/assets/e35b8643-aa0f-4157-96be-baf67f24e0af" />


**Count of orders by Delivery status**

---

## Project Overview

| | |
|---|---|
| **Project Name** | Amazon Sales Intelligence Dashboard |
| **Objective** | Analyze order-level Amazon sales and delivery data to surface revenue drivers, delivery bottlenecks, and cancellation risks |
| **Dataset** | 100 Amazon orders · 23 products · 50 customers · 5 regions |
| **Tools Used** | Microsoft Excel — Pivot Tables, XLOOKUP, Conditional Formatting, Charts |
| **File Type** | `.xlsx` |

---

## Business Problem

Amazon's order and fulfillment data needs a single consolidated view — one that connects orders, products, regions, and customers — to identify which regions/products drive revenue, where delivery through its fulfillment partners is slow, and where order cancellations are eroding sales.

---

## Solution

This project solves the problem by linking Amazon's Orders, Product Master, Region Master, and Customer Master sheets with XLOOKUP into one connected data model, then building a consolidated dashboard on top of it using pivot tables, KPI calculations, and conditional formatting. Instead of manually cross-referencing four separate sheets, stakeholders get one view showing exactly which regions/products drive revenue (North, Electronics), where fulfillment delivery is slowest (East, Central), and where cancellations are eroding sales (North at 40%) — turning raw Amazon order data into a direct, actionable operations dashboard.

---

## Data Model

| Sheet | Description | Key Columns |
|---|---|---|
| `Orders` | Transaction-level Amazon order data | Order ID, Customer ID, Product ID, Region, Sale Price/Unit, Quantity, Total Amount, Payment Method, Delivery Status, Fulfillment Partner, Order/Delivery/Cancel Date |
| `Product Master` | Product catalog | Product ID, Product Name, Category, Cost Price, Description |
| `Region Master` | Regional sales targets | Region, Sales Target |
| `Customer Master` | Customer directory | Customer ID, Customer Name, Customer Type, City, State |

`Orders` is linked to the master tables using **XLOOKUP**, pulling in Product Name, Category, and Customer Name directly rather than relying on nested VLOOKUP/MATCH formulas.

---

## Analysis Workflow

### 1. Region-Wise Product Sales
Pivot table of Total Sales Amount by Region × Product Category, revealing **North (₹10,491)** as the top-performing region and **Electronics (₹15,209)** as the top category.

### 2. Delivery Status Breakdown
Orders split by status: 34 Delivered, 30 Cancelled, 36 In Transit (out of 100 total).

### 3. Regional Average Delivery Time
Calculated per order using `=IF(Delivery Date<>"", Delivery Date - Order Date, "NA")`, then averaged by region — **East (4.25 days)** was slowest, **South (3.33 days)** fastest.

### 4. Effective Sales & Revenue
- Effective Sales (delivered orders only) = **₹35,258** total revenue.
- **% of Fast Deliveries** = Fast ÷ (Fast + Slow) = **32.4%**.
- **Top 3 performing regions:** North (₹10,491), West (₹8,359), South (₹7,317).
- **Highest-selling product by revenue:** Smartphone (₹9,644).
- **Highest-selling product by units:** Leg Set & T-Shirt (tied, 8 units each).

### 5. Trend & Conditional Formatting
- Monthly Sales Trend line chart (Jan–Dec) — peak month: **November (₹6,312)**.
- Conditional formatting applied to flag late deliveries and cancelled orders directly in the Orders table.

### 6. Cancellation Analysis
Cancellation Rate by Region (Cancelled ÷ Total Orders):

| Region | Cancellation Rate |
|---|---|
| North | 40% |
| Central | 35.7% |
| West | 34.8% |
| South | 20% |
| East | 16.7% |

### 7. Consolidated Dashboard
All KPIs and charts combined into a single interactive `DASHBOARD` sheet for at-a-glance monitoring.

---

## Key Business Insights

- **Electronics is the strongest category** — it generates the most revenue overall, driven primarily by Smartphones (₹9,644, the single highest-revenue product).
- **North region is a paradox:** it generates the highest revenue (₹10,491) but also the highest cancellation rate (40%) — pointing to strong demand alongside fulfillment/operational issues.
- **Only 32.4% of orders qualify as "fast" deliveries**, and only 11 of 100 orders were delivered within 2 days — delivery speed is a clear improvement area.
- **East, Central, and North regions have the highest average delivery times** (4.25, 4.2, and 3.63 days respectively) and should be prioritized for logistics improvements.
- **XLOOKUP significantly simplified cross-sheet analysis**, enabling direct two-way lookups without column-index limitations, improving formula accuracy and maintainability versus VLOOKUP + MATCH.

---

## Recommendations

1. Reduce regional delivery delays, especially in North, East, and Central.
2. Optimize delivery routes and strengthen courier/fulfillment partnerships to cut cancellations.
3. Implement real-time shipment tracking to catch delays early.
4. Speed up warehouse dispatch processing to shorten total delivery time.
5. Investigate root causes of cancellations in high-cancellation regions (North, Central, West).

---

## Skills Demonstrated

- Pivot tables & pivot charts for multi-dimensional business analysis
- XLOOKUP for cross-sheet data retrieval
- Conditional formatting for exception highlighting
- KPI calculation (effective sales, fast-delivery %, cancellation rate)
- Dashboard design consolidating multiple analyses into one view
- Business-question-driven analysis with written insights and recommendations

---

## Repository Contents


```

├── Datasets
└── README.md                              

```

## How to Use

1. Download `Excel_Mini_Project_1_submission.xlsx`.
2. Open in Microsoft Excel (2019+ recommended for full XLOOKUP support).
3. Explore the `DASHBOARD` sheet for the consolidated view, or open individual pivot sheets (prefixed `2.x`, `4.x`, `5.x`) to see each business question and its answer.

---






























