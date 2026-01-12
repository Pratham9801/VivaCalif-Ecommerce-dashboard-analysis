# Analysis Steps & Methodology

This document outlines the analytical thinking, approach, and validation steps used to answer the business questions.

---

## 1. Business Questions Defined

The analysis was structured around the following key business questions:

1. What are the overall sales and order trends in last 13 weeks?
2. How many items do customers typically buy per order?
3. Which products are most popular and revenue-generating?
4. How does customer behavior differ by gender?
5. Where do our customers live geographically?
6. How long does order delivery take?
7. How satisfied are customers with their purchases?

Each question was designed to support business decisions related to **inventory planning, promotions, operations, and customer experience**.

---

## 2. Data Understanding & Assumptions

- Dataset contains **2,400 rows and 15 columns** of transactional data.
- Column definitions and transformations are documented in `data_dictionary.md`.

### Key Assumptions:
- "Amount" represents total order value, not profit.
- Ratings reflect customer satisfaction but may be subjective.
- Missing gender values were categorized as **Unknown**.
- Delivery delays may be influenced by external logistics factors not captured in the data.

---

## 3. Key Metrics Used

The following business metrics were created or analyzed:

- Total Orders
- Total Quantity Sold
- Total Revenue (Amount Generated)
- Average Delivery Time (Days to Deliver)
-  Average Rating Distribution (1–5)

These metrics were used consistently across analyses to ensure comparability.

---

## 4. Analysis Approach (Question-wise)

### Q1: Sales Trend Analysis
- Weekly trends were analyzed using order count and total revenue.
- Helped identify  overall demand consistency and peak periods. Relationship between orders and Amount generated, and also helped to identify key anamoly 

### Q2: Quantity Purchased per Order
- Quantity values were grouped into logical bins (1,2,3,4,5,6-10, Above 10 )to reduce noise.
- Enabled identification of bulk purchasing behavior.
- Customers most commonly purchase in small bundles rather than single items

### Q3: Product Popularity
- Products were evaluated using all three KPI-  quantity sold,amount generated , Total Orders placed for that product
- Ratings were incorporated to validate customer satisfaction.
- Enabled Identification of Core Products of the Store

### Q4: Gender-wise Analysis
- Orders, revenue, and ratings were compared across genders.
- Helped confirm whether demand was gender-driven or product-driven.

### Q5: Geographic Distribution
- County-level analysis was used to identify high-performing regions using Amount generated and Quantity Sold 
- Supported regional targeting and operational prioritization.
- Pointed to Delivery performance impacts ratings in high-volume regions

### Q6: Delivery Time Analysis
- Delivery days were grouped into buckets (0,1,2,3,4,5,6-7 days,8-10 Days,11-15 Days)  for pattern detection..
- Late deliveries were cross-checked against ratings.
- Helped us identify Delivery time impacts ratings but is not the sole driver
- Bulk Orders Delivery time were analyzed .

### Q7: Customer Satisfaction
- Rating trends were analyzed across time, product, gender, geography, and order mode.
- Identified potential quality or operational issues.

---

## 5. Validation & Quality Checks

To ensure data reliability:

- Checked for negative or zero delivery days.
- Verified no negative quantities or amounts.
- Confirmed rating values were within the valid range (1–5).
- Cross-validated totals across pivots and dashboards.

---

## 6. Limitations

- Cost and profit data were unavailable, so profitability analysis was not possible.
- Customer-level repeat behavior could not be measured.
- External factors (festivals, discounts, logistics constraints) were not included.

---

## 7. Outcome

The structured approach enabled clear, actionable business recommendations while maintaining analytical rigor and transparency.
