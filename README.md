# 📦 Inventory & Supply Chain Analytics Dashboard

An interactive **Power BI** dashboard built to support inventory replenishment decisions, warehouse efficiency monitoring, and order fulfillment performance across regions and product categories — with an emphasis on the metrics operations and procurement teams use to set inventory parameters and flag anomalies.

![Dashboard Preview](assets/dashboard-preview.png)

---

## 📊 Overview

This dashboard helps supply chain, warehousing, and inventory teams monitor stock health at a glance, drill down by **Region** and **Category**, and identify replenishment risks such as excess backorders, low warehouse utilization, or transportation cost spikes — the kind of data-driven inputs used when setting inventory parameters, planning future demand, and running scenario analysis for warehouse stock levels.

## ✨ Key Features

- **Interactive Slicers** — Filter the entire dashboard by `Region` and `Category`
- **KPI Cards** — Quick-glance summary metrics for inventory health
- **Gauge Visual** — Warehouse utilization against a target benchmark, useful for spotting capacity gaps before they affect replenishment
- **Trend Analysis** — Units sold over time (2020–2024), a baseline for forecasting future inventory requirements
- **Comparative Bar Charts** — Transportation cost and inventory levels sliced by region and category
- **Donut Chart** — Average lead time distribution by category, relevant to setting reorder points
- **Order Status Breakdown** — Backorder counts across Fulfilled, Pending, and Canceled orders, a proxy for replenishment gaps

## 📈 KPIs & Metrics

| Metric | Description | Inventory Planning Relevance |
|---|---|---|
| **Warehouse Utilization** | 34.08% — current capacity usage against a 100% scale (target line at 75) | Flags underused capacity that could inform consolidation or reorder timing |
| **Days Sales of Inventory (DSI)** | 15.56 — average number of days inventory is held before sale | Signals whether stock is moving too slowly (obsolescence risk) or too fast (stockout risk) |
| **Inventory Turnover Ratio** | 23.47 — how efficiently inventory is sold and replaced | Core input for setting min/max inventory parameters |
| **Sum of Units Sold by Year** | Trend from 2020 to 2024 | Basis for forward-looking demand planning |
| **Average Lead Time by Category** | Accessories, Clothing, Electronics, Furniture | Directly informs reorder point and safety stock calculations |
| **Backorder Count by Order Status** | Fulfilled, Pending, Canceled | Highlights replenishment shortfalls needing investigation |

## 🧩 Visuals Included

1. **Warehouse Utilization** — Gauge chart
2. **Sum of Transportation Cost by Region and Category** — Clustered bar chart
3. **Sum of Units Sold by Year** — Area/line chart
4. **Average Lead Time by Category** — Donut chart
5. **Count of Backorder by Order Status** — Column chart
6. **Sum of Inventory Level by Category and Region** — Horizontal bar chart

## 🛠️ Tech Stack

- **Tool:** Microsoft Power BI Desktop
- **Data Source:** Excel / CSV (Inventory & Supply Chain dataset)
- **Techniques Used:** DAX measures, slicers, gauge visuals, conditional formatting, custom theming

## 📁 Repository Structure

```
inventory-supply-chain-dashboard/
├── assets/
│   └── dashboard-preview.png     # Dashboard screenshot
├── data/
│   └── inventory_data.csv        # Source dataset (or sample)
├── Inventory_Supply_Chain.pbix   # Power BI dashboard file
└── README.md                     # Project documentation
```

## 🚀 How to Use

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/inventory-supply-chain-dashboard.git
   ```
2. Open `Inventory_Supply_Chain.pbix` in **Power BI Desktop** (free download [here](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads)).
3. If prompted, update the data source path to point to your local `data/inventory_data.csv`.
4. Use the **Region** and **Category** slicers on the left panel to explore the data interactively.

## 🔍 Key Insights

- Units sold saw a sharp dip in 2021 before recovering strongly and stabilizing around ~195K–198K from 2022 onward.
- The **West** region incurs the highest transportation costs, particularly for Furniture and Electronics.
- The majority of backorders (838) are in **Fulfilled** status, with far fewer Pending (248) and Canceled (114) — worth investigating whether "Fulfilled" backorders point to a data-quality gap or a replenishment lag being masked in reporting.
- Lead times are fairly balanced across categories, ranging from ~15.3 to 16.6 days, suggesting reorder points could reasonably be standardized within a narrow band rather than set category by category.
- Warehouse utilization (34.08%) sits well below the 75% benchmark, indicating available capacity for increased stock buffers where lead-time risk is high.

## 📌 Future Improvements

- **Reorder point & safety stock calculator** — layer in lead time and demand variability to recommend reorder points by category/region, rather than only reporting historical lead time
- **ABC / criticality classification** — segment inventory by value and criticality to prioritize replenishment attention, mirroring how operations teams triage stock
- **Obsolete / non-moving inventory flag** — surface SKUs with high DSI and low turnover as candidates for a non-moving or obsolescence review
- **Forecasting** — add demand forecasting for units sold using Power BI's built-in forecasting or Python/R integration
- **Cost-per-unit efficiency metric** — tie transportation cost trends to per-unit fulfillment cost
- **Drill-through pages** — region-level deep dives for anomaly investigation

# 👨‍💻 Author

**Aryan Kharvar**

**M.Sc. Computational Sciences**

Data Analytics | Business Intelligence | Power BI | SQL | Python

💼 LinkedIn: [Aryan Kharvar](https://www.linkedin.com/in/aryankharvar)


---

⭐ If you found this dashboard useful, consider giving the repository a star!
