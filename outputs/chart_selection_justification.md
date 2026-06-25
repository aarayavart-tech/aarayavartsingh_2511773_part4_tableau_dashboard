# Chart Selection Justification

## 1. Sales Trend View

### Business Question

How are sales changing over time?

### Chart Type

Line Chart

### Fields Used

* X Axis: Order Date
* Y Axis: Sales
* Filter: Region, Category, Segment

### Why Appropriate

Line charts are the most effective way to show trends and seasonality over time.

### Design Principle

Temporal data visualization.

### Mistake Avoided

Avoided pie charts for time-series analysis.

---

## 2. Regional Performance View

### Business Question

Which regions perform best?

### Chart Type

Horizontal Bar Chart

### Fields Used

* Region
* Sales
* Profit

### Why Appropriate

Bar charts allow accurate comparison across regions.

### Design Principle

Easy ranking and comparison.

### Mistake Avoided

Avoided 3D charts that distort comparisons.

---

## 3. Category Profitability View

### Business Question

Which categories and sub-categories generate profit?

### Chart Type

Bar Chart

### Fields Used

* Category
* Sub-Category
* Profit

### Why Appropriate

Highlights both positive and negative profitability.

### Design Principle

Sorted descending by profit.

### Mistake Avoided

Avoided unsorted categories.

---

## 4. Customer Segment View

### Business Question

Which customer segment contributes most to performance?

### Chart Type

Stacked Bar Chart

### Fields Used

* Customer Segment
* Sales
* Profit

### Why Appropriate

Allows comparison across segments.

### Design Principle

Clear categorical comparison.

### Mistake Avoided

Avoided excessive color usage.

---

## 5. Shipping Performance View

### Business Question

How does shipping mode affect delivery performance?

### Chart Type

Bar Chart

### Fields Used

* Ship Mode
* Delivery Days
* Shipping Delay Bucket

### Why Appropriate

Clearly compares shipping efficiency.

### Design Principle

Operational performance focus.

### Mistake Avoided

Avoided cluttered tables.

---

## 6. Discount vs Profit View

### Business Question

How do discounts affect profitability?

### Chart Type

Scatter Plot

### Fields Used

* Discount
* Profit
* Category (Color)

### Why Appropriate

Scatter plots reveal relationships and outliers.

### Design Principle

Correlation analysis.

### Mistake Avoided

Avoided aggregating data into averages that hide patterns.

---

## 7. Return Analysis View

### Business Question

Where are returns concentrated?

### Chart Type

Highlight Table

### Fields Used

* Category
* Segment
* Return Rate

### Why Appropriate

Quickly identifies high-return areas.

### Design Principle

Visual emphasis through color intensity.

### Mistake Avoided

Avoided using pie charts with many categories.

---

# Dashboard Design Principles Applied

## Correct Chart Selection

Each chart matches the business question being answered.

## Clear Hierarchy

KPIs placed at top, trends in middle, diagnostics below.

## Minimal Clutter

Only essential labels and legends displayed.

## Consistent Colors

Profit = positive performance.
Returns and losses = warning colors.

## Readable Titles

All charts use business-friendly language.

## Appropriate Sorting

Bars sorted by performance metrics.

## Interactive Filtering

Region, Category, Segment, Date, Ship Mode, Campaign Channel.

## Avoidance of Misleading Scales

Axes start at logical values and maintain proportional representation.

## Focus on Business Interpretation

Every visualization supports a business decision.
