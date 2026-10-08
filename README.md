\# RetailPro — Retail Sales \& Business Analytics Dashboard



\## 📊 Project Overview



RetailPro is an end-to-end Power BI retail analytics project designed to provide

management with a comprehensive view of sales performance, profitability,

customers, products, stores, returns, and target achievement.



The project transforms raw retail transaction data into an interactive

business intelligence solution using Power Query, DAX, data modeling,

time intelligence, and advanced Power BI features.



The solution contains 7 interactive analytical pages with synchronized

slicers, drill-through analysis, dynamic metrics, what-if analysis, and

interactive business visualizations.



\## 🎯 Project Objective



The primary objective of this project is to transform raw retail data into

actionable business insights that help stakeholders:



\- Monitor sales and profitability performance

\- Analyze monthly, quarterly, yearly, and YTD trends

\- Understand customer behavior and repeat purchasing

\- Identify high-performing products and categories

\- Compare store and geographical performance

\- Analyze product and sales returns

\- Track actual sales against targets

\- Perform what-if pricing analysis

\- Drill into detailed business dimensions

\- Support data-driven business decisions



\## 🛠️ Tools \& Technologies



\- Microsoft Power BI

\- Power Query

\- DAX

\- Microsoft Excel

\- Data Modeling

\- Star Schema

\- Time Intelligence

\- Interactive Data Visualization

---



\## 📁 Dataset \& Data Model



The project uses a synthetic retail sales dataset created for business

analytics and Power BI dashboard development.



The dataset contains sales transactions, product information, customer

information, store details, employee information, returns, and sales targets.



\### Dataset Tables



| Table | Description |

|---|---|

| `DimDate` | Date, year, quarter, month and calendar information |

| `DimProduct` | Product, category and subcategory information |

| `DimCustomer` | Customer demographics and customer segments |

| `DimStore` | Store, region, state and city information |

| `DimEmployee` | Employee information |

| `FactSales` | Retail sales transaction data |

| `FactReturns` | Product return transactions |

| `FactTargets` | Monthly sales targets by store |



\### Data Model



The Power BI solution follows a \*\*Star Schema\*\* architecture.



The central fact table is `FactSales`, which is connected to multiple

dimension tables used for filtering, grouping, and analysis.



The model includes the following fact and dimension tables:



\*\*Fact Tables\*\*

\- `FactSales` — Primary sales transaction data

\- `FactReturns` — Product and sales return information

\- `FactTargets` — Monthly store-level sales targets



\*\*Dimension Tables\*\*

\- `DimDate` — Date and time intelligence

\- `DimProduct` — Product hierarchy and product attributes

\- `DimCustomer` — Customer attributes and segmentation

\- `DimStore` — Store and geographical information

\- `DimEmployee` — Employee information

\- `DimMonth` — Monthly bridge used for target/date analysis



The model also includes two analytical hierarchies:



\- \*\*Geography Hierarchy:\*\* Region → State → City

\- \*\*Product Hierarchy:\*\* Product Category → Product Subcategory → Product Name



The model was designed to support efficient filtering, aggregation,

time-intelligence calculations, drill-through analysis, and interactive

dashboard reporting.



\---

---

## 🔄 Power Query & Data Preparation

Power Query was used in Power BI to connect to the source Excel workbook,
inspect the available tables, prepare the data, and ensure that the dataset
was ready for analysis.

The data preparation process included:

- Connecting Power BI to the Excel source workbook
- Loading the required fact and dimension tables
- Reviewing table structures and column data types
- Validating date, numeric, text, and key columns
- Ensuring that sales, cost, quantity, discount, return, and target fields
  were available for analysis
- Preparing the date-related fields required for time-intelligence analysis
- Maintaining consistent key columns for relationships between fact and
  dimension tables
- Checking the data model for missing or inconsistent relationships
- Preparing the dataset for DAX calculations and interactive reporting

Power Query was used as the data preparation layer, while DAX was used for
business calculations and analytical measures.

This separation helped keep the data model organized and allowed the report
to perform analytical calculations efficiently.

---

---

## 🧮 DAX & Business Calculations

DAX (Data Analysis Expressions) was used extensively throughout the
RetailPro project to create reusable measures and perform business
calculations.

The DAX layer was designed to support sales, profitability, customer,
product, store, returns, target, pricing, and time-based analysis.

### Core Sales & Profitability Measures

Key measures include:

- Total Sales
- Total Cost
- Gross Profit
- Profit Margin %
- Total Quantity
- Total Orders
- Average Order Value

These measures form the foundation of the dashboard and are reused across
multiple visuals and analytical pages.

### Time Intelligence

DAX time-intelligence functions were used to analyze business performance
across different time periods.

Key calculations include:

- Previous Year Sales
- YoY Sales
- YoY Sales %
- YTD Sales
- MTD Sales
- QTD Sales
- Rolling 3M Sales
- Rolling 6M Sales
- Rolling 12M Sales
- Previous Month Sales
- MoM Sales Growth %
- Previous YTD Sales
- YTD Sales Growth %

Similar time-intelligence calculations were also created for profitability
and net sales.

### Customer Analytics

Customer-focused DAX measures were created to understand customer behavior
and contribution.

Key calculations include:

- Total Customers
- Customer Sales
- New Customers
- Repeat Customers
- Repeat Customer Rate %
- Average Customer Value
- Customer Contribution %
- Customer Rank
- Customer Profit Margin %
- Sales per Customer
- Profit per Customer
- Orders per Customer
- Average Units per Customer

### Product Analytics

Product performance was analyzed using DAX measures for sales,
profitability, ranking, contribution, and product mix.

Key calculations include:

- Product Sales
- Product Cost
- Product Profit
- Product Margin %
- Product Quantity
- Product Rank
- Product Contribution %
- Product Profit % of Total
- Product Profit per Unit
- Product Sales % of Total
- Cumulative Product Sales
- Cumulative Product Sales %
- Products to 80% Sales
- Pareto 80% Line

These calculations were used to build the Product Sales Pareto Analysis and
other product performance visuals.

### Store & Geographic Analytics

DAX measures were created to compare store and geographical performance.

Key calculations include:

- Total Stores
- Average Sales per Store
- Store Contribution %
- Store Rank
- Geographic Contribution %
- Region Rank
- State Rank
- City Rank

The calculations support analysis through the Geography hierarchy of
Region → State → City.

### Returns & Net Performance

Returns analysis was implemented using dedicated DAX measures.

Key calculations include:

- Total Returned Quantity
- Total Returned Sales
- Return Rate %
- Returned Sales
- Sales Return Rate %
- Net Sales
- Net Profit
- Net Margin %
- Return Amount % of Sales
- Net Quantity
- Returned Orders
- Return Order Rate %
- YoY Net Sales %
- YTD Net Sales
- YoY Net Profit %

These measures allow the business to understand how returns affect overall
sales and profitability.

### Target Analysis

Sales target performance was calculated using DAX measures including:

- Total Sales Target
- Target Variance
- Target Achievement %
- Target Variance %
- Target Status
- Target Performance Indicator

These measures were used to compare actual sales against store and monthly
targets.

### Discount & Pricing Analysis

DAX was also used to analyze the impact of discounts and pricing.

Key calculations include:

- Total Discount
- Average Discount %
- Discounted Sales
- Full-Price Sales
- Average Selling Price
- Discount Impact %
- Discounted Sales Margin %

### Advanced Sales Performance

Additional business metrics were created to provide deeper performance
analysis:

- Units per Order
- Profit per Order
- Profit per Customer
- Profit per Unit
- Sales per Customer
- Orders per Customer
- Average Units per Customer

### What-If Analysis

A `Price Change %` what-if parameter was implemented to simulate the impact
of changing selling prices.

The scenario analysis includes:

- Scenario Sales
- Scenario Profit
- Scenario Profit Margin %

This allows users to interactively test potential pricing changes and
understand their effect on revenue and profitability.

### Dynamic Reporting & Status Measures

Dynamic DAX measures were also created to improve dashboard usability.

These include:

- Selected Year
- Selected Month
- Selected Store
- Dynamic Report Title
- Dashboard Title
- Dashboard Context
- Sales Performance Status
- Profit Performance Status
- Return Risk Status
- YoY Sales Indicator
- Target Performance Indicator

### Ranking & Contribution Analysis

Ranking and contribution calculations were implemented using functions such
as `RANKX`, `ALL`, and `ALLSELECTED`.

These calculations support:

- Product ranking
- Customer ranking
- Store ranking
- Geographic ranking
- Contribution analysis
- Pareto analysis

### DAX Techniques Used

The project demonstrates practical use of several important DAX concepts and
functions, including:

- `CALCULATE`
- `SUM`
- `SUMX`
- `DIVIDE`
- `DISTINCTCOUNT`
- `FILTER`
- `RANKX`
- `ALL`
- `ALLSELECTED`
- `REMOVEFILTERS`
- `SELECTEDVALUE`
- `HASONEVALUE`
- `SWITCH`
- `SAMEPERIODLASTYEAR`
- `DATEADD`
- `TOTALYTD`
- `TOTALMTD`
- `TOTALQTD`
- `DATESINPERIOD`
- `TREATAS`
- Variables using `VAR` and `RETURN`

The DAX layer provides the analytical foundation for the RetailPro dashboard
and enables reusable, filter-aware business calculations across all report
pages.

---

---

## 📊 Dashboard Pages & Visualizations

The RetailPro Power BI report contains **7 interactive analytical pages**.
Each page focuses on a specific area of retail business performance while
maintaining a consistent dashboard design and user experience.

### 🏠 Executive Dashboard

The Executive Dashboard provides a high-level overview of the overall
business performance.

**Key KPIs:**

- Total Sales
- Gross Profit
- Profit Margin %
- Total Orders
- Total Customers
- Net Sales
- Return Rate %
- Repeat Customer Rate %
- Target Achievement %

**Key Visuals:**

- Sales Trend
- Profit Trend
- Sales by Category
- Actual Sales vs Target
- Sales by Region
- Top 10 Products by Sales

The dashboard also includes synchronized slicers, dynamic report context,
reset filters, and interactive navigation between report pages.

### 📈 Sales Analytics

The Sales Analytics page provides detailed analysis of sales performance,
sales trends, orders, and geographical performance.

**Key KPIs:**

- Total Sales
- Rolling 6M Sales
- Rolling 3M Sales
- YoY Sales Growth %
- Total Orders
- Average Order Value
- Total Quantity

**Key Visuals:**

- Monthly Sales & YoY Growth
- Monthly Sales vs Rolling 3M Average
- Top 10 Stores by Sales
- Sales by Customer Segment
- Sales by Geography
- Annual Sales vs Gross Profit

### 👥 Customer Analytics

The Customer Analytics page focuses on customer behavior, segmentation,
customer contribution, and regional customer performance.

**Key KPIs:**

- Total Customers
- New Customers
- Repeat Customers
- Repeat Customer Rate %
- Average Customer Value

**Key Visuals:**

- Customers & Sales by Segment
- Customer Sales by Region
- Customer Segment Sales Ranking by Year
- Customer Sales Decomposition
- Customer Sales by Segment & Region

The page also supports customer drill-through analysis for detailed
customer-level investigation.

### 📦 Product Analytics

The Product Analytics page analyzes product sales, profitability,
product contribution, product mix, and product rankings.

**Key KPIs:**

- Product Sales
- Product Profit
- Product Margin %
- Product Quantity
- Product Profit per Unit

**Key Visuals:**

- Product Sales Pareto Analysis
- Product Profitability Matrix
- Product Sales Mix by Category
- Product Category Sales Ranking by Year

The page includes a Product Hierarchy and supports product-level
drill-through analysis.

### 🏪 Store Analytics

The Store Analytics page provides detailed analysis of store performance
and geographical performance.

**Key KPIs:**

- Total Stores
- Total Sales
- Average Sales per Store
- Total Orders
- Profit Margin %

**Key Visuals:**

- Store Performance Matrix
- Store Sales Contribution by Region
- Store Sales vs Profitability
- Store Sales by City

The Store Performance Matrix supports the hierarchy:

**Region → State → City → Store**

The page also supports store-level drill-through analysis.

### ↩️ Returns Analytics

The Returns Analytics page evaluates product returns and their impact on
sales performance.

**Key KPIs:**

- Total Returned Sales
- Total Returned Quantity
- Return Rate %
- Sales Return Rate %
- Net Margin %

**Key Visuals:**

- Return Sales Trend
- Return Sales by Reason
- Return Reason Ranking by Year
- Return Sales Decomposition
- Top 10 Stores by Return Rate %
- Return Quantity by Product Category

The page helps identify return trends, major return reasons, and areas with
higher return activity.

### 🎯 Target Analytics

The Target Analytics page compares actual sales performance with defined
sales targets.

**Key KPIs:**

- Total Sales
- Sales Target
- Target Achievement %
- Target Variance
- Target Variance %

**Key Visuals:**

- Monthly Sales vs Target Achievement
- Target Variance Contribution by Region
- Store Sales vs Target
- Store Target Performance Matrix

The page enables management to identify stores and regions that are
performing above or below their assigned sales targets.

### 🔗 Interactive Power BI Features

The report includes several interactive Power BI capabilities:

- Synchronized slicers across report pages
- Year filtering
- Month filtering
- Region filtering
- Product Category filtering
- Store filtering
- Reset Filters button
- Page navigation
- Drill-through analysis
- Product drill-through
- Customer drill-through
- Store drill-through
- Field Parameter for dynamic metric selection
- What-If Price Change analysis
- Interactive hierarchies
- Tooltips
- Cross-filtering between visuals
- Dynamic dashboard context

These features allow users to move from high-level business performance to
detailed analysis without leaving the Power BI report.

---

---

## ⚙️ Power BI Features & Advanced Functionality

The RetailPro Power BI solution uses a range of Power BI features to provide
an interactive, analytical, and user-friendly reporting experience.

### 🔄 Synchronized Slicers

Slicers were synchronized across all report pages to provide consistent
filtering throughout the dashboard.

The main synchronized filters include:

- Year
- Month
- Region
- Product Category
- Store

This allows users to maintain the same analytical context while navigating
between different report pages.

### 🔍 Drill-Through Analysis

Drill-through functionality was implemented to allow users to move from
summary-level analysis to detailed information.

Drill-through pages were configured for:

- Product analysis
- Customer analysis
- Store analysis

This enables users to right-click an item in a visual and navigate to the
corresponding analytical page with the selected filter context applied.

### 🧭 Hierarchies

Hierarchies were created to support structured drill-down analysis.

The geographical hierarchy is:

**Region → State → City → Store**

The product hierarchy is:

**Product Category → Product Subcategory → Product Name**

These hierarchies allow users to move from high-level summaries to
increasingly detailed business information.

### 🎛️ Field Parameter

A Power BI Field Parameter named `Metric Selector` was implemented to allow
users to dynamically switch between important business metrics.

The parameter includes:

- Total Sales
- Gross Profit
- Total Quantity
- Total Orders
- Average Order Value

This provides a flexible way to analyze multiple metrics within the same
visual without creating separate visuals for each measure.

### 💰 What-If Analysis

A What-If parameter named `Price Change %` was created to simulate changes
in selling prices.

The parameter allows users to test price changes from **-20% to +20%**.

Scenario measures include:

- Scenario Sales
- Scenario Profit
- Scenario Profit Margin %

This feature demonstrates how Power BI can be used for interactive business
scenario analysis and decision support.

### 🔄 Reset Filters

A Reset Filters button was implemented using Power BI bookmarks.

The reset functionality allows users to quickly return the dashboard to its
default filter state without manually clearing individual slicers.

### 🧭 Page Navigation

A page navigator was implemented to provide easy navigation between the
seven analytical pages.

The report includes navigation for:

- Executive Dashboard
- Sales Analytics
- Customer Analytics
- Product Analytics
- Store Analytics
- Returns Analytics
- Target Analytics

### 🏷️ Dynamic Dashboard Context

Dynamic DAX measures were used to display the currently selected reporting
context.

The dashboard can dynamically display:

- Selected Year
- Selected Month
- Selected Store

This provides users with clear visibility into the current filter context.

### 🔀 Cross-Filtering & Interactions

Visual interactions were configured throughout the report so that selecting
a category, region, product, store, or other data point can dynamically
filter or highlight related visuals.

This enables users to explore relationships between different business
dimensions interactively.

### 📊 Interactive Analytical Visuals

The project demonstrates the use of multiple Power BI visual types,
including:

- KPI Cards
- Line Charts
- Column Charts
- Bar Charts
- Combo Charts
- Matrix
- Tables
- Donut Chart
- Treemap
- Ribbon Chart
- Scatter Chart
- Waterfall Chart
- Map
- Decomposition Tree
- Slicers

### 🎨 Dashboard Design

A consistent dark and electric-cyan visual theme was applied across the
report.

The design includes:

- Dark navy backgrounds
- Electric cyan highlights
- Consistent typography
- KPI cards with visual icons
- Consistent spacing and alignment
- Interactive navigation
- Consistent slicer styling
- Clear visual hierarchy

The design was created to provide a professional, modern, and
portfolio-ready Power BI dashboard experience.

---

---

## 💡 Key Business Insights

The RetailPro analysis provides several important business insights across
sales, profitability, customers, products, stores, returns, and target
performance.

### 💰 Sales & Profitability

- Total Sales generated by the business are approximately **₹13.17 billion**.
- Gross Profit is approximately **₹2.99 billion**.
- Overall Gross Profit Margin is approximately **22.71%**.
- Net Sales after accounting for returns are approximately **₹12.18 billion**.
- Net Profit after returns and costs is approximately **₹2.00 billion**.
- Net Profit Margin is approximately **16.45%**.

These results show that the business generates strong overall revenue and
profitability, while returns have a noticeable impact on net performance.

### 📈 Sales Performance

- Total Orders are approximately **99,768**.
- Total Quantity sold is approximately **450,658 units**.
- Average Order Value is approximately **₹131.96K**.
- Sales performance shows growth across the later years of the analysis.
- Year-over-Year sales indicators show positive growth for the available
  years after the initial period.

The combination of order volume and average order value provides useful
insight into overall sales productivity.

### 👥 Customer Insights

- The dataset contains **10,000 customers**.
- The analysis identifies a **100% repeat customer rate** within the
  available transaction data.
- Repeat purchasing is therefore a significant characteristic of the
  dataset.
- Customer segmentation and regional analysis help identify differences in
  customer sales contribution.
- Customer contribution and ranking measures allow high-value customers to
  be identified.

The customer analysis demonstrates how Power BI can be used to evaluate
customer behavior, value, and contribution to overall revenue.

### 📦 Product Insights

- Product performance varies across categories, subcategories, and
  individual products.
- Product ranking identifies the highest-performing products by sales.
- Product profitability analysis highlights differences between revenue
  generation and profit contribution.
- The Pareto analysis shows that approximately **257 products account for
  80% of cumulative sales**.
- Product contribution analysis helps identify products with significant
  influence on total revenue.

This allows management to focus inventory, pricing, and promotional
strategies on products with the greatest business impact.

### 🏪 Store & Geographic Insights

- Store performance varies across regions, states, cities, and individual
  stores.
- Store ranking identifies high-performing and lower-performing locations.
- Store contribution analysis shows each location's contribution to total
  sales.
- Geographic analysis enables comparison across Region, State, City, and
  Store levels.
- Store profitability analysis helps distinguish locations generating high
  sales from those generating strong profit.

This provides a foundation for location-level performance management and
resource allocation.

### ↩️ Returns Insights

- Total Returned Quantity is approximately **33,600 units**.
- Total Returned Sales are approximately **₹986.20 million**.
- Overall Return Rate is approximately **7.46%** based on returned quantity
  versus total quantity sold.
- The Sales Return Rate is approximately **14.97%** based on returned sales
  transactions relative to total orders.
- Return analysis identifies the most significant return reasons,
  categories, stores, and geographical areas.

Returns therefore represent an important area for operational and
profitability improvement.

### 🎯 Target Performance

- Total Sales Target is approximately **₹357.19 million**.
- Actual sales significantly exceed the overall target in the synthetic
  dataset.
- Overall Target Achievement is approximately **368.57%**.
- Target Variance is approximately **₹959.31 million**.
- The overall target status is **Above Target**.

The target analysis allows management to compare actual performance with
planned targets at monthly, regional, and store levels.

### 💸 Discount & Pricing Insights

- Total discount impact is approximately **₹994.09 million**.
- Average Discount Percentage is approximately **7.02%**.
- Discounted sales account for a significant portion of total sales.
- Discounted sales have a lower margin than the overall business margin.
- The What-If Price Change analysis demonstrates how changes in selling
  price can affect sales, profit, and profit margin.

This analysis can support pricing and promotional decisions.

### 📊 Overall Business Observation

The RetailPro dashboard demonstrates that the business has strong overall
sales and profitability, positive sales growth, a highly active repeat
customer base, and sales performance above the defined targets.

At the same time, returns and discounting have a meaningful effect on net
sales and profitability. Product, store, customer, and geographical
analysis can therefore be used to identify specific opportunities for
improving margins and operational efficiency.

---

---

## 📋 Business Recommendations

Based on the analysis performed in the RetailPro Power BI dashboard, the
following business recommendations can be considered to improve sales,
profitability, customer retention, and operational performance.

### 💰 Improve Profitability

- Focus on products and stores that generate strong profit rather than
  evaluating performance only by sales revenue.
- Monitor profit margin regularly at product, category, store, and regional
  levels.
- Identify locations with high sales but comparatively low profitability
  and investigate their cost and discount structure.
- Use profit-per-order and profit-per-unit metrics to identify areas where
  profitability can be improved.

### 💸 Optimize Discount Strategy

- Monitor discount levels and their effect on profit margins.
- Avoid excessive discounting on products that already have strong demand.
- Use targeted promotions instead of applying broad discounts across all
  products.
- Use the Price Change What-If analysis to evaluate potential pricing
  scenarios before implementing major pricing changes.

### 📦 Optimize Product Portfolio

- Prioritize high-performing products that contribute significantly to
  total sales.
- Use Pareto analysis to identify the products responsible for the majority
  of revenue.
- Review low-performing products to determine whether they should be
  promoted, repositioned, or discontinued.
- Evaluate product profitability in addition to sales volume when making
  inventory and assortment decisions.

### 👥 Strengthen Customer Relationships

- Continue focusing on customer retention because repeat purchasing is a
  major contributor to sales performance.
- Identify high-value customers using customer sales, contribution, and
  ranking metrics.
- Develop targeted loyalty programs and personalized promotions for
  valuable customer segments.
- Analyze customer segments and regions to identify opportunities for
  increasing customer value.

### 🏪 Improve Store Performance

- Benchmark stores against other stores within the same region.
- Identify stores with high sales but lower profitability and investigate
  operating costs, discounts, and product mix.
- Study high-performing stores to identify successful practices that can be
  replicated across other locations.
- Use store-level target achievement to prioritize management attention and
  operational support.

### 🌎 Strengthen Geographic Strategy

- Compare performance across regions, states, and cities.
- Identify high-growth geographical areas for expansion opportunities.
- Investigate underperforming locations to understand whether the issue is
  related to customer demand, product availability, pricing, or store
  performance.
- Use geographical contribution analysis to support resource allocation.

### ↩️ Reduce Product Returns

- Investigate the most common return reasons and identify recurring issues.
- Analyze products and categories with unusually high return activity.
- Review stores with high return rates and identify operational patterns.
- Improve product descriptions, customer communication, quality controls,
  and sales processes where appropriate.
- Monitor return rate and net margin together to understand the financial
  impact of returns.

### 🎯 Improve Target Management

- Monitor target achievement at monthly, regional, and store levels.
- Investigate stores that consistently perform below their targets.
- Use high-performing stores as benchmarks for setting realistic performance
  expectations.
- Review target assumptions regularly to ensure that targets remain aligned
  with business conditions.

### 📈 Monitor Sales Trends

- Continue monitoring monthly, quarterly, and yearly sales trends.
- Use YoY, MoM, YTD, and rolling-period metrics to identify changes in
  business momentum.
- Investigate significant changes in sales or profitability as early
  indicators of potential business opportunities or risks.

### 📊 Establish a Continuous Performance Review

Management can use the RetailPro dashboard as a recurring performance
monitoring tool by reviewing:

- Sales performance
- Profitability
- Customer behavior
- Product performance
- Store performance
- Returns
- Target achievement
- Discount impact

Regular monitoring of these indicators can help management identify
performance changes early and take data-driven corrective actions.

### 🚀 Overall Recommendation

The organization should adopt a balanced performance strategy that focuses
not only on increasing revenue but also on improving profitability,
retaining valuable customers, reducing unnecessary returns, optimizing
discounts, and improving store-level performance.

The RetailPro Power BI dashboard provides a centralized analytical
framework that can support these decisions through interactive,
data-driven reporting.

---


---

## 🛠️ Technical Skills Demonstrated

The RetailPro project demonstrates practical experience across the complete
Power BI development lifecycle, from data preparation and modeling to
advanced analytics and dashboard development.

### Microsoft Power BI

- Power BI Desktop
- Interactive dashboard development
- Report and page design
- KPI development
- Visual interactions
- Cross-filtering
- Drill-through analysis
- Page navigation
- Bookmarks
- Synchronized slicers
- Tooltips
- Field Parameters
- What-If Parameters
- Hierarchies
- Dynamic reporting context

### Power Query

- Connecting Power BI to Excel data sources
- Data preparation and transformation
- Data type validation
- Fact and dimension table preparation
- Data quality checks
- Preparing data for analytical modeling

### DAX

- Measure creation
- Filter context
- Context-aware calculations
- Variables using `VAR` and `RETURN`
- `CALCULATE`
- `SUM`
- `SUMX`
- `DIVIDE`
- `DISTINCTCOUNT`
- `FILTER`
- `RANKX`
- `ALL`
- `ALLSELECTED`
- `REMOVEFILTERS`
- `SELECTEDVALUE`
- `HASONEVALUE`
- `SWITCH`
- `TREATAS`

### Time Intelligence

- Year-over-Year analysis
- Month-over-Month analysis
- Year-to-Date analysis
- Month-to-Date analysis
- Quarter-to-Date analysis
- Previous Year calculations
- Previous Month calculations
- Rolling 3-month analysis
- Rolling 6-month analysis
- Rolling 12-month analysis

### Data Modeling

- Star Schema design
- Fact and dimension table modeling
- Relationship management
- Date dimension
- Monthly bridge table
- Hierarchies
- Geographic modeling
- Product modeling
- Filter propagation
- Model validation

### Business Analytics

- Sales analysis
- Profitability analysis
- Customer analytics
- Product analytics
- Store analytics
- Geographic analysis
- Returns analysis
- Target analysis
- Discount analysis
- Pricing scenario analysis
- Customer contribution analysis
- Product Pareto analysis
- Store performance analysis

### Data Visualization

Experience with multiple Power BI visual types, including:

- KPI Cards
- Line Charts
- Column Charts
- Bar Charts
- Combo Charts
- Matrix
- Tables
- Donut Charts
- Treemaps
- Ribbon Charts
- Scatter Charts
- Waterfall Charts
- Maps
- Decomposition Trees
- Slicers

### Dashboard & UX Design

- Professional dashboard layout
- Consistent visual theme
- Dark UI design
- Electric-cyan visual styling
- KPI card design
- Visual alignment
- Page navigation
- Interactive filtering
- Dynamic report context
- User-friendly analytical experience

### Analytical & Problem-Solving Skills

- Translating business requirements into analytical metrics
- Designing reusable DAX measures
- Identifying business KPIs
- Performing trend analysis
- Comparing actual performance against targets
- Identifying performance drivers
- Analyzing profitability and returns
- Creating interactive business scenarios
- Converting raw data into actionable insights
- Building portfolio-ready business intelligence solutions

### Tools & Technologies

**Primary Tools:**

- Microsoft Power BI
- Power Query
- DAX
- Microsoft Excel

**Core Technical Areas:**

- Business Intelligence
- Data Analytics
- Data Visualization
- Data Modeling
- Time Intelligence
- KPI Development
- Dashboard Development
- Interactive Reporting

---

---

## 📁 Project Structure & File Organization

The RetailPro project is organized into separate files and folders to keep
the Power BI report, source dataset, documentation, and supporting assets
structured and easy to maintain.

### Project Folder Structure

```text
RetailPro_PowerBI_Project/
│
├── RetailPro_PowerBI_Project.pbix
├── RetailPro_PowerBI_Project.xlsx
├── README.md
│
├── Screenshots/
│   ├── Executive_Dashboard.png
│   ├── Sales_Analytics.png
│   ├── Customer_Analytics.png
│   ├── Product_Analytics.png
│   ├── Store_Analytics.png
│   ├── Returns_Analytics.png
│   └── Target_Analytics.png
│
└── Documentation/
    └── RetailPro_Project_Documentation.pdf
