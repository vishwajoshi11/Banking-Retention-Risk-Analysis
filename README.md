# 🏦 Retail Banking Customer Retention & Risk Analytics Dashboard

An executive-level interactive retail banking analytics dashboard developed in **Microsoft Excel**. This project models 10,000 European customer accounts across France, Germany, and Spain to diagnose customer flight, evaluate capital balance exposure, and provide data-backed retention strategies for banking leadership.

---

## 📊 Dashboard Overview



> ![Dashboard Preview](dashboard_preview.png)

---

## 📌 Executive Summary & Key KPIs

Customer attrition directly impacts a commercial bank's Net Interest Margin (NIM) and Customer Acquisition Cost (CAC). This analytics model analyzes portfolio-level churn dynamics, multi-product holding patterns, and demographic attrition vectors across €764.86M in customer balances.

* **Portfolio Size:** 10,000 Customers
* **Total Balance Exposure:** €764.86M
* **Baseline Portfolio Churn Rate:** 20.37% (2,037 lost accounts)
* **Active Membership Engagement Ratio:** 51.51%

---

## 🔍 Core Risk Insights & Portfolio Vulnerabilities

### 1. Regional Disparity (The German Anomaly)
* **France** (~16.15%) and **Spain** (~16.67%) maintained stable baseline attrition.
* **Germany** exhibited an acute **32.44% churn rate**—more than double other operating regions.
* The highest flight risk in the entire portfolio is among **German female account holders at 37.55%**.

### 2. Multi-Product Cross-Selling Breakdown
* Holding **1 product** reflects a 27.71% churn rate, while customers with **2 products** are the stickiest segment at **7.58% churn**.
* Retention collapses at higher product depths: **3 products surge to an 82.71% churn rate**, and accounts with **4 products experience a 100.00% attrition rate**.
* *Strategic Implication:* Aggressive bundling without integrated account utility creates operational friction rather than deeper customer loyalty.

### 3. Demographic Aging Vectors
* Customers in the **Senior cohort (50+)** demonstrated an acute **45.45% churn rate**.
* In contrast, core working-age adults (18.37%) and young adults (7.56%) exhibited substantially lower churn.

---

## 🛠 Technical Architecture & Implementation

* **Platform:** Microsoft Excel (Data Modeling, Pivot Engines, Slicers, Form Controls)
* **ETL & Data Transformation:**
  * Cleaned raw European transactional data.
  * Extracted demographic segments (`Young Adult`, `Adult`, `Senior`) via logical conditional formulas.
  * Formatted binary fields for dynamic percentage aggregations (`Exited`, `IsActiveMember`).
* **Decoupled Backend Calculation Layer (`Sheet5`):**
  * Built dedicated calculation matrices separate from the front-end canvas to prevent formula errors.
  * Configured summarized metrics (`Average of Exited` for precise churn rates, `Sum of Exited` for customer volume).
* **Interactive Front-End Canvas:**
  * Slicer cross-filtering configured across 3 independent Pivot Tables simultaneously.
  * Dynamic KPI shape scorecards tied to backend reference cells using formula bar references (`=Sheet5!Cell`).
  * Visual suite: Age Distribution Stacked Bar, Country Demographics Clustered Bar, and Product Risk 100% Stacked Column.

---

## 📈 Strategic Business Recommendations

1. **German Branch Network Intervention:** Deploy localized discovery surveys in German branches to investigate regional fee sensitivity, digital UX friction, and competitor interest rate spreads.
2. **Revise Cross-Selling Sales Incentives:** Immediately freeze sales targets pushing 3rd and 4th product acquisitions until the root cause of 82–100% attrition is audited.
3. **Senior Wealth Concierge Support:** Develop personalized relationship management, retirement wealth advisory, and tiered interest benefits for accounts aged 50+ to protect primary deposit bases.

---

## 📁 Repository Structure

```text
├── data/
│   └── Churn_Modelling.csv                    # Raw retail banking source data
├── dashboards/
│   └── Bank_Customer_Retention_Dashboard.xlsx # Full interactive Excel workbook
├── assets/
│   └── dashboard_preview.png                  # High-resolution canvas screenshot
└── README.md                                  # Executive summary & technical documentation
