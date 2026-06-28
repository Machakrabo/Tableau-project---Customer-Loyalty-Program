# Customer Loyalty Program Analysis

A Tableau-based analytical dashboard examining customer purchasing behavior, loyalty tier performance, coupon marketing response, and geographic revenue distribution across four countries from 2016 to 2020.

---

## Project Overview

This project analyzes a multi-national retail loyalty program to uncover patterns in customer spending, segment engagement by loyalty tier, and evaluate the effectiveness of coupon-based marketing campaigns. The workbook provides both high-level executive summaries and granular geographic and departmental breakdowns.

The Tableau workbook (`Customer_Loyalty_Analysis.twbx`) packages the data extract and all visualizations into a single portable file.

---

## Dataset

| Property | Value |
|---|---|
| Source file | `CustomerLoyaltyProgram.csv` |
| Records | 84,436 transactions |
| Unique customers | 63,228 |
| Countries | United States, Canada, United Kingdom, Germany |
| Time period | 2016 – 2020 (Quarters Q1–Q4) |

### Schema

| Field | Type | Description |
|---|---|---|
| `Loyalty#` | Integer | Unique loyalty program ID |
| `First Name` / `Last Name` | String | Customer name |
| `Customer Name` | String | Full name (concatenated) |
| `Country` | String | Customer country |
| `Province or State` | String | Regional subdivision |
| `City` | String | Customer city |
| `Latitude` / `Longitude` | Float | Geographic coordinates |
| `Postal code` | String | Postal / ZIP code |
| `Gender` | String | male / female |
| `Education` | String | High School or Below / College / Bachelor / Master / Doctor |
| `Location Code` | String | Urban / Suburban / Rural |
| `Income` | Integer | Annual household income (local currency) |
| `Marital Status` | String | Single / Married / Divorced |
| `Order Year` | Integer | Year of purchase (2016–2020) |
| `Quarter` | String | Q1 / Q2 / Q3 / Q4 |
| `MonthsAsMember` | Integer | Program tenure in months (range 25–70) |
| `LoyaltyStatus` | String | Bronze / Silver / Gold / Platinum / Elite / VIP |
| `Product Line` | String | Product category purchased |
| `Coupon Response` | String | Coupon used in transaction (Coupons 1–6) |
| `Count` | Integer | Number of orders |
| `Quantity Sold` | Integer | Units purchased |
| `Unit Sale Price` | Integer | Sale price per unit |
| `Unit Cost` | Integer | Cost per unit |
| `Revenue` | Integer | Total transaction revenue |
| `Customer Lifetime Value` | Float | Estimated CLV score |
| `Loyalty Count` | Integer | Number of loyalty transactions |

---

## Key Metrics

| Metric | Value |
|---|---|
| Total Revenue | $228.7 M |
| Unique Customers | 63,228 |
| Average CLV | $8,007 |
| Max CLV | $83,325 |
| Average Membership Tenure | 51 months (~4.2 years) |
| Transactions | 84,436 |

---

## Loyalty Tiers

| Tier | Transactions | Share |
|---|---|---|
| Platinum | 14,447 | 17.1% |
| Gold | 14,390 | 17.0% |
| Bronze | 14,312 | 17.0% |
| Silver | 13,985 | 16.6% |
| Elite | 13,752 | 16.3% |
| VIP | 13,550 | 16.1% |

Tiers are approximately evenly distributed, indicating a mature loyalty program with broad engagement across all segments.

---

## Product Lines

| Product Line | Revenue | Transactions |
|---|---|---|
| TV and Video Gaming | $97.8 M | 33,872 |
| Computers and Home Office | $85.7 M | 19,723 |
| Photography | $24.3 M | 14,954 |
| Kitchen Appliances | $15.9 M | 7,566 |
| Smart Electronics | $5.1 M | 8,321 |

TV & Video Gaming and Computers & Home Office together account for over 80% of total revenue.

---

## Geographic Distribution

| Country | Transactions | Revenue |
|---|---|---|
| United States | 22,039 | $59.5 M |
| Canada | 21,797 | $58.1 M |
| United Kingdom | 20,774 | $57.7 M |
| Germany | 19,826 | $53.5 M |

Revenue and transaction volumes are remarkably balanced across all four markets.

---

## Revenue by Year

| Year | Revenue |
|---|---|
| 2019 | $60.3 M |
| 2018 | $51.4 M |
| 2016 | $47.5 M |
| 2017 | $39.5 M |
| 2020 | $30.0 M |

2020 shows a decline, likely reflecting reduced consumer activity or data truncation within the year.

---

## Dashboard & Worksheets

The workbook (`Customer Loyalty Analysis.twb`) contains five worksheets and one consolidated dashboard.

### Worksheets

| Sheet | Visualization | Key Dimensions |
|---|---|---|
| **Customer Lifetime Value and Quantity Sold by City** | Dual-axis bar + line chart | City × CLV + Quantity Sold |
| **DeptSales** | Scatter plot | Department-level sales scatter |
| **Marketing Response by Department** | Shape/scatter chart | Coupon Response × Quantity Sold by department |
| **QtyCouponResponse** | Bar chart | Coupon type × Quantity Sold |
| **RevenueQTYSold** | Geographic map | Revenue and Quantity Sold by latitude/longitude |

### Dashboard 1

A consolidated overview combining all five worksheets into a single interactive view. Use Tableau's filter actions on the map to cross-highlight coupon response, CLV, and department sales.

---

## Customer Demographics

| Attribute | Breakdown |
|---|---|
| **Gender** | Male 50.1% / Female 49.9% |
| **Education** | Bachelor 62.4%, College 25.4%, High School or Below 4.7%, Doctor 4.4%, Master 3.1% |
| **Location** | Suburban 33.7%, Rural 33.4%, Urban 32.9% |
| **Marital Status** | Married 58.0%, Single 27.0%, Divorced 15.0% |

---

## Coupon Program

Six coupon types were used across the dataset:

| Coupon | Transactions |
|---|---|
| Coupon 1 | 42,576 (50.4%) |
| Coupon 2 | 17,441 (20.7%) |
| Coupon 4 | 16,640 (19.7%) |
| Coupon 6 | 4,501 (5.3%) |
| Coupon 3 | 1,744 (2.1%) |
| Coupon 5 | 1,534 (1.8%) |

Coupon 1 dominates usage by a wide margin.

---

## How to Open

1. Download and install [Tableau Public](https://public.tableau.com/) (free) or [Tableau Desktop](https://www.tableau.com/products/desktop).
2. Open `Customer_Loyalty_Analysis.twbx` directly — the packaged workbook embeds the data extract, so no external data connection is required.
3. Navigate between the five worksheets using the tabs at the bottom, or open **Dashboard 1** for the consolidated view.

---

## File Structure

```
Customer_Loyalty_Analysis.twbx
├── Customer Loyalty Analysis.twb         # Workbook XML (views, charts, layout)
├── Data/
│   ├── CustomerLoyaltyProgram.csv        # Raw source data (84,436 rows)

```

---

## Tools & Versions

| Tool | Version |
|---|---|
| Tableau | 2026.1.5 (build 20261.26.0512.1609) |
| Workbook format | v18.1 |
| Data format | CSV + Hyper extract |
