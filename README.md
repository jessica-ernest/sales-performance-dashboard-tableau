# 📊 Sales Performance Dashboard — Tableau

---

## 1. Business Context & Objectives

### The Company
Smart Insights Co. (also referred to as Retail Insights Co.) is a 
retail business operating across multiple US states, selling products 
across several categories including furniture, technology, office 
supplies and more.

### The Problem
The company had no centralized way to monitor sales performance 
across product categories, geographic regions and time periods. 
Decision-makers lacked visibility into:
- Which product sub-categories were driving or hurting profits
- Which states were most and least profitable
- How current year sales compared to the previous year
- Which customer-dense states were actually generating profit vs loss

Without this visibility, the company could not make informed decisions 
about where to invest, which products to promote, and which regions 
needed strategic attention.

### The Objective
Design and deliver a comprehensive Tableau dashboard that gives 
Smart Insights Co. a complete, interactive view of their 2023 sales 
performance — enabling data-driven regional and product-based strategy.

**Specific goals:**
- Track Total Sales, Total Profit and Total Quantity with YoY comparison
- Compare all product sub-categories by sales and profit
- Identify states with the highest customer concentration and their profitability
- Visualize geographic sales distribution across the US

---

## 2. Data Sources & Data Preparation

### Data Sources
Four CSV files were provided and joined in Tableau:

| File | Contents |
|------|----------|
| Customers.csv | Customer demographic and ID data |
| Location.csv | Sales locations with geographic details |
| Orders.csv | Order details — sales, profit, quantity, linked to products and customers |
| Products.csv | Product categories, sub-categories and descriptions |

### Data Preparation Steps
1. Imported all 4 CSV files into Tableau
2. Built relationships between tables:
   - Orders → Customers (via Customer ID)
   - Orders → Products (via Product ID)
   - Orders → Locations (via Location ID)
3. Verified data types — dates, currency fields, numeric quantities
4. Created calculated fields for:
   - Year-over-Year (YoY) Sales Change %
   - YoY Profit Change %
   - YoY Quantity Change %
   - Current Year vs Previous Year comparison measures
5. Filtered dataset to focus on 2023 with prior year as baseline

---

## 3. Analytical Methodology & Approach

### Dashboard Design Decisions
Built a single-page executive dashboard with 5 key visual components:

**KPI Cards (Top Section)**
- Total Sales: $733K — with sparkline showing monthly trend vs PY
- Total Profit: $93K — with sparkline and YoY comparison
- Total Quantity: 12K units — with sparkline and trend line
- Each KPI shows current year (orange line) vs previous year (black line)
- Color-coded arrows: red ▼ for decline, green ▲ for growth

**Sub-Category Bar Chart (Right Panel)**
- Horizontal bar chart comparing CY vs PY sales for every sub-category
- Orange = Current Year, Black = Previous Year
- Allows instant identification of growing vs declining sub-categories

**Profit By State Map (Bottom Left)**
- Geographic map showing profit figures per state
- Color gradient to identify high vs low profit states
- Enables regional strategy decisions at a glance

**States With Over 200 Customers (Bottom Center)**
- Combined view of customer volume AND profit/loss per state
- Critical insight: high customer states are NOT always profitable
- Illinois, Ohio, Pennsylvania, Texas all show losses despite large customer base

**Interactive Filters**
- Category slicer — filter by furniture, technology, office supplies
- Select Year — enables historical comparison

### Key Analytical Approach
Used Current Year vs Previous Year (CY vs PY) methodology throughout 
to ensure every metric tells a story about growth or decline — not 
just absolute numbers.

---

## 4. Results & Key Insights

### KPI Summary
| Metric | 2023 Value | vs Prior Year |
|--------|-----------|---------------|
| Total Sales | $733K | ▼ -20.36% |
| Total Profit | $93K | ▲ +14.24% |
| Total Quantity | 12K units | ▲ +26.83% |

### Critical Business Insight
**Sales declined 20% but profit GREW 14%** — this means the company 
sold lower revenue but at better margins. This is actually a positive 
signal: they are selling smarter, not just more.

### Sub-Category Insights
**Top performing sub-categories (Sales):**
- Phones — highest sales volume by far
- Chairs — strong consistent performer
- Binders — significant sales growth vs PY

**Underperforming sub-categories:**
- Art, Fasteners, Labels — minimal sales contribution
- Recommendation: review pricing or discontinue low performers

### Geographic Insights
**Profitable states:**
- California: $29.4K profit from 577 customers ✅
- Washington: $17.3K profit ✅
- New York: $74K profit from 415 customers ✅ (highest profit state)

**Loss-making states (RED FLAG 🚨):**
- Texas: -$8.8K loss from 370 customers
- Illinois: -$13K loss from 237 customers
- Ohio: -$17K loss from 202 customers
- Pennsylvania: -$16K loss from 257 customers

**Key Insight:** The company is losing money in 4 high-customer states. 
This suggests pricing issues, high delivery costs, or unfavorable 
product mix in these regions. Immediate strategic review needed.

---

## 5. Implementation, Monitoring & Next Steps

### What Was Delivered
- Fully interactive Tableau dashboard published on Tableau Public
- Executives can filter by category and year
- All 5 business questions from the brief answered in one view
- CY vs PY comparison built into every visual

### Business Impact
- Eliminated need for manual Excel sales reporting
- Executives can identify profit/loss by state in seconds
- Sub-category performance visible at a glance for buying decisions
- Regional loss-making states identified — enabling immediate action

### Recommendations Based on Findings
1. **Investigate Texas, Illinois, Ohio and Pennsylvania immediately** — 
   selling to many customers but losing money. Root cause: pricing, 
   logistics cost or wrong product mix
2. **Double down on New York and California** — highest profit states 
   with large customer bases
3. **Review low-performing sub-categories** — Art, Fasteners, Labels 
   contribute minimal revenue; consider discontinuing or repricing
4. **Protect profit margins** — the 14% profit growth despite 20% 
   sales decline shows margin improvement; maintain this discipline

### Next Steps
1. Add customer segmentation layer (Consumer vs Corporate vs Home Office)
2. Build a profit margin % view by sub-category
3. Add quarterly drill-down for seasonal trend analysis
4. Create an automated weekly refresh connected to live sales data
5. Build a forecasting model for 2024 sales targets

---

## 🛠️ Tools Used
Tableau · Calculated Fields · CY vs PY Analysis · 
Geographic Mapping · Data Relationships · Dashboard Design

---

## 🔗 Live Dashboard
[👉 View Live Dashboard on Tableau Public](https://public.tableau.com/app/profile/jessica.ogiemwonyi/viz/salesdashboard_17208724314550/Dashboard1)

---

## 📸 Screenshots
![Sales Dashboard 2023](sales-dashboard.png)
