# Tableau-Orders-Dashboard-Modern-App-Design
# 📊 Orders Dashboard — Modern Business Analytics

![Tableau](https://img.shields.io/badge/Tableau-Desktop-blue?logo=tableau&logoColor=white)
![Excel](https://img.shields.io/badge/Data-Excel%20%2F%20XLSX-217346?logo=microsoft-excel&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![Records](https://img.shields.io/badge/Records-21%2C900%20orders-orange)

---

## 📌 Project Overview

The **Orders Dashboard** is a modern, interactive business intelligence dashboard built in **Tableau Desktop**. It provides a comprehensive view of order fulfillment, sales performance, customer behavior, operational efficiency, and cost distribution across three fiscal years (2022–2024).

Built on a transactional dataset of **21,900 orders** spanning **10 countries** and **3 customer segments**, the dashboard empowers stakeholders to monitor KPIs, track trends, and make data-driven business decisions — all from a single, polished visual interface.

---

## 🎯 Objectives

- Analyze overall sales performance across segments, categories, and geographies
- Monitor order fulfillment efficiency and on-time delivery rates
- Track customer purchasing behavior and repeat purchase patterns
- Identify return patterns and operational bottlenecks
- Evaluate cost distribution across key business functions
- Provide executive-level KPI reporting through interactive dashboards

---

## 📂 Dataset Description

The project uses a single Excel workbook (`DATASET.xlsx`) containing four sheets, each serving a distinct analytical purpose.

| Sheet Name | Records | Description |
|---|---|---|
| `Order-Sales Data` | 21,900 | Main transactional order dataset |
| `Metrics` | 12 | Business KPI metrics by customer segment |
| `Cost Data` | 60 | Quarterly business costs by cost type |
| `Waffle Chart` | 100 | Helper coordinates for waffle chart visualization |

### Dataset Highlights

| Metric | Value |
|---|---|
| Total Sales (3-year) | $3,203,440 |
| Total Orders | 21,900 |
| Unique Customers | 2,726 |
| On-Time Delivery Rate | 90.7% |
| Return Rate | 7.6% |
| Repeat Customer Rate | 46.7% |
| Date Range | Jan 2022 – Dec 2024 |

---

## 🗂️ File Descriptions

| File | Type | Description |
|---|---|---|
| `DATASET.xlsx` | Excel Workbook | Source dataset: sales transactions, KPI metrics, cost data, and waffle chart helper data |
| `Orders_Dashboard_Modern_Design_waseem.twbx` | Tableau Packaged Workbook | Complete Tableau project including dashboard layouts, visualizations, calculated fields, and embedded data extracts |
| `Image/Green Blue Purple Gradient.png` | PNG Image | Background design asset used in the dashboard canvas |
| `Image/Order Fulfillment Background - Tableau.png` | PNG Image | Section background image for the Order Fulfillment view |
| `Data/Extracts/*.hyper` | Tableau Hyper Extract | Pre-built data extract for fast dashboard load performance |
| `README.md` | Markdown | Project documentation (this file) |

> **Note:** The `.twbx` (Tableau Packaged Workbook) format bundles the workbook and all data sources into a single portable file — no separate connection setup is needed.

---

## 🔍 Column / Feature Explanation

### Sheet: Order-Sales Data

This is the primary dataset used for all sales and fulfillment analysis.

| Column | Data Type | Description |
|---|---|---|
| `Order ID` | String | Unique identifier for each order (e.g., `ORD-4122170`) |
| `Order Date` | DateTime | Date and time the order was placed |
| `Ship Date` | DateTime | Date and time the order was shipped |
| `Segment` | String | Customer segment: `Consumer`, `Corporate`, or `Home` |
| `Category` | String | Product category: `Furniture`, `Office Supplies`, or `Technology` |
| `Subcategory` | String | Product subcategory (e.g., `Sofas`, `Chairs`, `Laptops`) |
| `Sales` | Float | Revenue generated from the order (USD) |
| `Customer ID` | String | Unique customer identifier (e.g., `CUST-2968`) |
| `Customer Name` | String | Full name of the customer |
| `Country` | String | Customer's country (10 countries represented) |
| `Returns` | Binary (0/1) | Whether the order was returned (`1` = returned) |
| `Status` | String | Order status: `Complete`, `Pending`, or `Cancelled` |
| `Repeat Customer` | Binary (0/1) | Whether the customer has placed previous orders (`1` = repeat) |
| `On Time` | Binary (0/1) | Whether the order was delivered on time (`1` = on time) |

### Sheet: Metrics

Business KPI values segmented by customer group.

| Column | Description |
|---|---|
| `Metric` | KPI name: `GPM` (Gross Profit Margin), `OPM` (Operating Profit Margin), `ROA` (Return on Assets), `ROE` (Return on Equity) |
| `Segment` | Customer segment the metric applies to |
| `Metric Value` | Decimal KPI value (e.g., `0.38` = 38%) |

**Sample KPI values:**

| Metric | Consumer | Corporate | Home |
|---|---|---|---|
| GPM | 38% | 24% | 16% |
| OPM | 12% | 8% | 15% |
| ROA | 7% | 10% | 5% |
| ROE | 18% | 25% | 14% |

### Sheet: Cost Data

Quarterly cost breakdown across five business functions, spanning 2022–2024.

| Column | Description |
|---|---|
| `Quarter-Year` | Reporting period (e.g., `2022 Q1`) |
| `Cost` | Monetary cost value (USD) |
| `Type of Cost` | Cost category: `Operational`, `Product`, `Marketing`, `Shipping`, `Return` |

**Total cost by type (2022–2024):**

| Cost Type | Total |
|---|---|
| Operational | $814,894 |
| Product | $679,078 |
| Marketing | $543,263 |
| Shipping | $407,447 |
| Return | $271,631 |

### Sheet: Waffle Chart

Contains X/Y coordinate helper data used to render waffle chart visualizations in Tableau. Not intended for direct analysis.

| Column | Description |
|---|---|
| `Columns` | X-axis position (1–10) |
| `Rows` | Y-axis position (1–10) |

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Tableau Desktop** | Dashboard development, visualization, and interactivity |
| **Tableau Hyper Extract** | Optimized data extraction for fast rendering |
| **Microsoft Excel** | Raw data storage and pre-processing |

---

## ⚙️ Installation Instructions

### Prerequisites

Before opening this project, ensure you have:

- **Tableau Desktop** (version 2021.1 or later recommended)
- **Microsoft Excel** or compatible spreadsheet software (for dataset inspection)

### Steps

**1. Clone the repository**

```bash
git clone https://github.com/yourusername/orders-dashboard.git
cd orders-dashboard
```

**2. Open the Tableau workbook**

Double-click the packaged workbook file, or open it from Tableau's File menu:

```
Orders_Dashboard_Modern_Design_waseem.twbx
```

> The `.twbx` file already contains the embedded data — no additional connection setup is needed.

**3. (Optional) Reconnect to the raw dataset**

If you want to connect to the source Excel file directly:

```
DATASET.xlsx
```

Navigate to **Data → Edit Data Source** in Tableau to point to your local copy.

**4. Refresh data if needed**

Go to **Data → Refresh All Extracts** to reload the latest data from the source.

---

## 📖 Usage Guide

### Navigating the Dashboard

1. Open the Tableau workbook
2. Use the tab bar at the bottom to switch between dashboard views
3. Use on-canvas **filter controls** to slice by segment, category, country, or date range
4. Hover over any chart element to view **tooltip details**
5. Click a chart element to cross-filter other views on the same dashboard

### Business Questions This Dashboard Answers

| Question | Where to Look |
|---|---|
| Which customer segment generates the highest sales? | Sales by Segment chart |
| What percentage of orders are delivered on time? | Fulfillment KPI panel |
| Which product categories and subcategories perform best? | Category / Subcategory breakdown |
| How much is spent on operational and marketing costs? | Cost Analysis view |
| What is the repeat customer rate? | Customer Analytics panel |
| How are profits trending quarter over quarter? | KPI Metrics view |

---

## 🔧 Data Preprocessing Steps

The following steps were applied to prepare the data before building the dashboard.

### 1. Data Cleaning

- Removed or flagged records with missing values in critical fields (`Order ID`, `Sales`, `Customer ID`)
- Standardized date formats across `Order Date` and `Ship Date` columns
- Validated all `Order ID` and `Customer ID` values for uniqueness and correct formatting

### 2. Feature Engineering

- Created binary flags for `Returns`, `Repeat Customer`, and `On Time` to support calculated KPIs
- Derived customer segmentation fields from existing transaction data
- Added fulfillment lag calculation (days between order and ship date)

### 3. KPI Calculation

- **Gross Profit Margin (GPM):** Revenue minus cost of goods, divided by revenue
- **Operating Profit Margin (OPM):** Operating profit divided by revenue
- **Return on Assets (ROA):** Net income divided by total assets
- **Return on Equity (ROE):** Net income divided by shareholder equity
- **On-Time Rate:** Count of on-time orders divided by total completed orders
- **Return Rate:** Count of returned orders divided by total orders

### 4. Tableau Data Extraction

- Created `.hyper` extract files from `DATASET.xlsx` for optimized in-memory performance
- Configured extract refresh schedule for production deployment readiness

---

## 📈 Example Outputs / Results

### Sales Performance

| Segment | Total Sales | Share |
|---|---|---|
| Consumer | $1,461,543 | 45.6% |
| Corporate | $983,524 | 30.7% |
| Home | $758,373 | 23.7% |

| Category | Total Sales |
|---|---|
| Furniture | $1,345,629 |
| Office Supplies | $1,056,993 |
| Technology | $800,818 |

**Top 5 Subcategories by Sales:**

| Subcategory | Sales |
|---|---|
| Sofas | $293,340 |
| Tables | $281,153 |
| Cabinets | $269,856 |
| Bookcases | $260,440 |
| Chairs | $240,841 |

### Geographic Reach

| Country | Sales |
|---|---|
| United States | $917,488 |
| India | $562,443 |
| France | $354,709 |
| Australia | $299,221 |
| Japan | $215,077 |

### Order Fulfillment

| Status | Count | Percentage |
|---|---|---|
| Complete | 19,265 | 88.0% |
| Pending | 1,759 | 8.0% |
| Cancelled | 876 | 4.0% |

### Year-over-Year Sales Growth

| Year | Approx. Annual Sales | Trend |
|---|---|---|
| 2022 | ~$987,000 | Baseline |
| 2023 | ~$1,012,000 | ↑ +2.5% |
| 2024 | ~$1,204,000 | ↑ +18.9% |

---

## 📁 Folder Structure

```
orders-dashboard/
│
├── DATASET.xlsx                               # Source data (sales, costs, KPIs)
│
├── Orders_Dashboard_Modern_Design_waseem.twbx # Tableau packaged workbook
│
├── Data/
│   └── Extracts/
│       └── *.hyper                            # Tableau optimized data extracts
│
├── Image/
│   ├── Green Blue Purple Gradient.png         # Dashboard background asset
│   └── Order Fulfillment Background - Tableau.png
│
└── README.md                                  # Project documentation (this file)
```

---

## 🚀 Future Improvements

- [ ] **Real-time data connectivity** — connect the dashboard to a live database or API feed instead of static Excel extracts
- [ ] **Sales forecasting** — integrate Tableau's built-in forecasting or connect to an external predictive model
- [ ] **Automated KPI alerts** — configure email or Slack alerts when KPIs drop below defined thresholds
- [ ] **Geographic heatmap** — add a world map view showing sales density by country or region
- [ ] **Advanced customer segmentation** — use RFM (Recency, Frequency, Monetary) scoring to classify customers more granularly
- [ ] **Tableau Cloud deployment** — publish the workbook to Tableau Cloud/Server for web-based access and scheduled refresh
- [ ] **Mobile-optimized layout** — design a Tableau Mobile-friendly view for on-the-go executive access
- [ ] **Return root-cause analysis** — add a dedicated view drilling into return reasons by product, region, and segment

---

## 👤 Author

**Waseem**

- 🧑‍💻 Tableau Developer & Data Analyst
- 📊 Business Intelligence Enthusiast
- 🌐 [GitHub Profile](https://github.com/yourusername)
- 💼 [LinkedIn](https://linkedin.com/in/yourprofile)

---

## 🙏 Acknowledgements

- [Tableau](https://www.tableau.com/) — for their powerful data visualization platform and community resources
- The open-source analytics community — for shared knowledge, tutorials, and inspiration
- Dataset contributors and business intelligence practitioners whose work shaped the KPI framework used in this project

---

*Last updated: June 2026*
