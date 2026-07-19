# SQL-Practice-set-problems-with-solutions
 SQL practice project analyzing pizza sales data. Covers joins, grouping, aggregates, ranking, and window functions. Organized by difficulty (Basic–Advanced) with 13 queries showcasing real business insights from order and revenue analysis.

# Pizza Sales SQL Analysis

MySQL practice project analyzing a pizza restaurant's order data — covering
aggregate functions, multi-table joins, grouping, window-style ranking, and
revenue analysis. Solved as part of a structured SQL learning path
(WsCube Tech MySQL course) and organized here by difficulty tier.

## 📊 Dataset
The queries run against a `pizzahut` schema with the following core tables:
- `orders` — order_id, order date, order time
- `order_details` — order_details_id, order_id, pizza_id, quantity
- `pizzas` — pizza_id, pizza_type_id, size, price
- `pizza_types` — pizza_type_id, name, category, ingredients

## 📁 Structure

```
pizza-sales-analysis/
├── README.md
├── 00-setup/
│   └── create-tables.sql
├── 01-basic/
│   ├── q01-total-orders.sql
│   ├── q02-total-revenue.sql
│   ├── q03-highest-priced-pizza.sql
│   ├── q04-common-pizza-size.sql
│   └── q05-top5-ordered-pizzas.sql
├── 02-intermediate/
│   ├── q06-quantity-by-category.sql
│   ├── q07-orders-by-hour.sql
│   ├── q08-category-distribution.sql
│   ├── q09-avg-pizzas-per-day.sql
│   └── q10-top3-by-revenue.sql
└── 03-advanced/
    ├── q11-revenue-percentage-contribution.sql
    ├── q12-cumulative-revenue.sql
    └── q13-top3-by-category-revenue.sql
```

## ✅ Topics covered

| Tier | Concepts |
|---|---|
| Basic | `COUNT()`, `SUM()`, `ROUND()`, single `JOIN`, `ORDER BY` + `LIMIT` |
| Intermediate | Multi-table `JOIN`, `GROUP BY`, `HOUR()`/date functions, averages per group, ranking by revenue |
| Advanced | Percentage-of-total calculations, running/cumulative totals, window functions (`RANK()`/`ROW_NUMBER()` partitioned by category) |

## 🗂️ File format
Each `.sql` file follows a consistent, self-documenting structure:
```sql
-- Q: <question in plain English>
-- Difficulty: Basic / Intermediate / Advanced | Concept: <SQL concepts used>

<query>

-- Output: <result, where applicable>
```
This keeps each file readable on its own — no need to cross-reference a
separate answer key.

## 🚀 How to use
1. Run `00-setup/create-tables.sql` to create the `pizzahut` database and
   core table structure (`orders`, `order_details`).
2. Import/populate the `pizzas` and `pizza_types` tables with the dataset.
3. Run `USE pizzahut;` then execute any `.sql` file from `01-basic`,
   `02-intermediate`, or `03-advanced` individually.
4. Files are numbered sequentially (`q01`–`q13`) across the whole project,
   but grouped into folders by difficulty for easier navigation.

## 📌 Status
- [x] Basic (5/5)
- [x] Intermediate (5/5)
- [x] Advanced (3/3)

Project complete — 13/13 queries.

## 🙏 Acknowledgements
This project was solved while following the **Pizza Sales SQL Project**
walkthrough by **[WsCube Tech](https://www.youtube.com/@wscubetech)**
on YouTube. The dataset, business questions, and problem structure are
based on that tutorial; all queries in this repo were written and tested
independently as practice.

📺 Tutorial reference: https://youtu.be/zZpMvAedh_E
