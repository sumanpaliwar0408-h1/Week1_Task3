# Task 3 --- Visualization Challenge

## Data Science Internship --- Week 1

**Organization:** WeIntern Pvt Ltd\
**Task:** Task 3 --- Visualization Challenge\
**Dashboard Tool:** Microsoft Power BI Desktop\
**Dataset:** Sample - Superstore

## Project Objective

The objective of Task 3 is to communicate business insights from the
analyzed sales dataset through professional visualizations and a
dashboard-style layout. The dashboard focuses on chart selection,
clarity, readability, interpretation, and consistent presentation.

The completed Power BI dashboard combines headline KPIs with category,
time, product, customer-segment, and regional views on a single page.

## Dataset Description

The dashboard uses the Sample Superstore dataset, which contains:

-   **9,994 order-line records**
-   **5,009 distinct orders**
-   **793 customers**
-   **1,850 products**
-   Sales records covering **2014--2017**

The source data is stored at order-line level. Therefore, order-based
metrics use **distinct Order ID** rather than row count.

## Tools Used

-   Microsoft Power BI Desktop
-   Power Query
-   DAX
-   Sample Superstore sales dataset

No Python packages are required to open or use the Task 3 dashboard.

## Dashboard KPIs

The dashboard contains four headline KPI cards:

  KPI                   Definition                               Result
  --------------------- ------------------------------ ----------------
  Total Revenue         Sum of Sales                     \$2,297,200.86
  Total Orders          Distinct Order ID                         5,009
  Average Order Value   Total Revenue / Total Orders           \$458.61
  Total Units Sold      Sum of Quantity                          37,873

## DAX Measures

The principal dashboard measures are:

``` dax
Total Revenue =
SUM('Sample - Superstore'[Sales])

Total Orders =
DISTINCTCOUNT('Sample - Superstore'[Order ID])

Average Order Value =
DIVIDE([Total Revenue], [Total Orders])

Total Units Sold =
SUM('Sample - Superstore'[Quantity])
```

## Dashboard Visualizations

### Revenue by Category --- Bar Chart

The category bar chart compares revenue across product categories.
**Technology** generates the highest category revenue at approximately
**\$836,154.03**.

### Monthly Sales Trend --- Line Chart

The line chart displays revenue over time. **November 2017** records the
highest monthly revenue at approximately **\$118,447.83**, while
**February 2014** records the lowest at approximately **\$4,519.89**.

### Revenue Share by Customer Segment --- Pie Chart

The pie chart compares the proportional revenue contribution of the
three customer segments:

-   Consumer --- approximately **\$1.16M**
-   Corporate --- approximately **\$706.15K**
-   Home Office --- approximately **\$429.65K**

The limited number of segments makes a pie chart suitable for this
proportional comparison.

### Top 10 Products by Units Sold --- Bar Chart

The dashboard ranks the ten strongest products by unit volume using a
Top N filter based on Total Units Sold.

**Staples** has the highest unit volume at **215 units**.

Unit-volume leadership is different from revenue leadership. The
highest-revenue product is **Canon imageCLASS 2200 Advanced Copier**,
generating approximately **\$61,599.82**.

### Revenue by Region

The regional visual compares revenue across the four regions:

  Region           Revenue
  --------- --------------
  West        \$725,457.82
  East        \$678,781.24
  Central     \$501,239.89
  South       \$391,721.91

The **West** contributes the highest regional revenue.

## Interactive Filters

The dashboard includes slicers for:

-   Year
-   Region
-   Category
-   Segment

These filters allow users to explore the same KPIs and visualizations
for selected subsets of the data.

## Dashboard Design

The dashboard is designed as a single-page business summary.

It includes:

-   Four KPI cards
-   Revenue by Category
-   Monthly Sales Trend
-   Revenue Share by Customer Segment
-   Top 10 Products by Units Sold
-   Revenue by Region
-   Four interactive slicers
-   A dashboard title and consistent visual layout

The visual structure is intended to keep the dashboard readable while
allowing the main business measures and comparisons to be understood
from one page.

## Key Findings

1.  The dataset generates approximately **\$2.30M in revenue** from
    **5,009 distinct orders** and **37,873 units**, with an average
    order value of **\$458.61**.
2.  **Technology** is the highest-revenue product category.
3.  **November 2017** is the highest-revenue month in the dataset.
4.  The **Consumer** segment contributes the largest share of revenue.
5.  The **West** is the highest-revenue region.
6.  **Staples** leads product unit volume, while **Canon imageCLASS 2200
    Advanced Copier** leads product revenue.

## Recommendations

-   Evaluate revenue, orders, units, and average order value together
    rather than using a single KPI to interpret performance.
-   Analyze high-revenue products separately from high-volume products
    because the two measures capture different business patterns.
-   Use the Year, Region, Category, and Segment slicers to investigate
    whether overall patterns remain consistent within narrower groups.
-   Use the dashboard as the visual summary layer and the Task 2 sales
    analysis for deeper analytical interpretation.

## Limitations and Assumptions

-   The dataset is stored at order-line level.
-   Distinct `Order ID` is used for order-based calculations.
-   `Sales` is treated as revenue.
-   `Quantity` is treated as units sold.
-   The dashboard describes historical patterns and is not a forecasting
    model.
-   Visual differences represent associations in the supplied dataset
    and do not establish causal explanations.
-   Profitability is not the primary focus of this Task 3 dashboard.

## Repository Structure

``` text
Data_Science_Week1_Task3_Visualization/
├── Data/
│   └── Raw/
│       └── Sample - Superstore.csv
├── Dashboard/
│   └── Task3_Dashboard.pbix
├── Outputs/
│   └── Dashboard/
│       └── dashboard-mockup.png
├── Reports/
│   └── Task3_Visualization_Dashboard_Report.pdf
├── Screenshots/
│   ├── dashboard-mockup.png
│   ├── kpi-cards.png
│   ├── monthly-sales-trend.png
│   └── category-product-visuals.png
├── README.md
└── requirements.txt
```

## How to Open the Project

1.  Clone or download this repository.
2.  Install **Microsoft Power BI Desktop** if it is not already
    installed.
3.  Open `Dashboard/Task3_Dashboard.pbix` in Power BI Desktop.
4.  Review the KPI cards and dashboard visuals.
5.  Use the Year, Region, Category, and Segment slicers to interact with
    the dashboard.
6.  Refer to `Reports/Task3_Visualization_Dashboard_Report.pdf` for the
    written interpretation, findings, recommendations, and limitations.

## Task 3 Deliverables

The repository contains or is structured to contain:

-   Power BI dashboard (`Task3_Dashboard.pbix`)
-   At least one bar chart
-   At least one line chart
-   At least one pie chart
-   One complete dashboard layout
-   KPI cards
-   Short interpretations of the dashboard visuals in the final report
-   Genuine dashboard screenshots/export
-   Final Task 3 report
-   README documentation
-   Source dataset

## Author

**Suman Paliwar**\
Data Science Internship --- Week 1
