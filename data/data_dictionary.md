# Data Dictionary

This document describes the structure, meaning, and purpose of each column used in the analysis.

---

## Raw / Source Columns

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Product | Categorical | Name of the product ordered |
| Quantity | Numeric | Number of units purchased in a single order |
| Amount | Numeric | Total Amount (Quantity × Unit Price) |
| Order Date | Date | Date on which the customer placed the order |
| Ship Date | Date | Date on which the order was shipped |
| Customer Gender | Categorical | Gender of the customer (Male, Female, Other, Unknown) |
| Order Mode | Categorical | Channel through which the order was placed (App, Website, Instagram) |
| County | Categorical | County where the order was delivered |

---

## Calculated / Derived Columns

| Column Name | Data Type | Description |
|------------|----------|-------------|
| Days to Deliver | Numeric | Number of days between Order Date and Ship Date |
| Week Number | Numeric | Calendar week number extracted from Order Date |
| Gender Value | Text | Standardized gender labels (expanded from M/F to Male/Female) |

---

## Notes & Assumptions

- Missing gender values were categorized as **"Unknown"**.
- Calculated fields were created to support trend, delivery, and customer behavior analysis.
