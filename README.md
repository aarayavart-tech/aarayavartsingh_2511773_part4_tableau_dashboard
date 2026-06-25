# Tableau Executive Sales Dashboard

## Project Overview

This project analyzes sales, profitability, customer behavior, shipping performance, and returns using Tableau.

The objective is to provide leadership with a single executive dashboard that highlights:

* Sales performance
* Regional performance
* Category profitability
* Customer segment behavior
* Shipping efficiency
* Return patterns
* Discount impact on profit

---

## Dataset Inspection

### Date Fields

* order_date
* ship_date

### Geographic Fields

* region
* state
* city

### Categorical Fields

* customer_segment
* category
* sub_category
* ship_mode
* campaign_channel
* product_name

### Numerical Measures

* sales
* profit
* quantity
* discount
* delivery_days
* customer_rating

### Binary / Flag Fields

* return_flag

  * 0 = Not Returned
  * 1 = Returned

---

## Assumptions

### Return Flag

Assumed:

* 0 = Successful order
* 1 = Returned order

### Average Order Value

Calculated as:

Sales ÷ Distinct Count(Order ID)

because each order has a unique identifier.

### Profit Margin

Calculated as:

Profit ÷ Sales

Displayed as percentage.

### Shipping Delay

Delivery days are used as a proxy for shipping performance.

### Return Rate

Calculated as:

Returned Orders ÷ Total Orders

---

## Tableau Calculated Fields

### Profit Margin

```tableau
SUM([Profit]) / SUM([Sales])
```

### Cost

```tableau
SUM([Sales]) - SUM([Profit])
```

### Average Order Value

```tableau
SUM([Sales]) / COUNTD([Order ID])
```

### Return Rate

```tableau
SUM([Return Flag]) / COUNT([Order ID])
```

### Shipping Delay Bucket

```tableau
IF [Delivery Days] <= 2 THEN "Fast (0-2 Days)"
ELSEIF [Delivery Days] <= 5 THEN "Standard (3-5 Days)"
ELSE "Delayed (6+ Days)"
END
```

### Discount Band

```tableau
IF [Discount] <= 0.10 THEN "Low Discount"
ELSEIF [Discount] <= 0.20 THEN "Medium Discount"
ELSE "High Discount"
END
```

### Sales per Unit

```tableau
SUM([Sales]) / SUM([Quantity])
```

---

## Dashboard KPIs

1. Total Sales
2. Total Profit
3. Profit Margin %

Additional KPI options:

* Return Rate %
* Average Order Value
* Total Orders

---

## Dashboard Filters

* Region
* Category
* Customer Segment
* Date
* Ship Mode
* Campaign Channel

---

## Files Included

```text
README.md

outputs/
├── business_insights.md
├── dashboard_story.md
└── chart_selection_justification.md

screenshots/
├── full_dashboard.png
├── sales_trend_view.png
├── regional_performance_view.png
├── category_profitability_view.png
└── filter_interaction_view.png
```
