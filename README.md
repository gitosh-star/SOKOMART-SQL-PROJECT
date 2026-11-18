# SokoMart Kenya --- Data Engineering & Analytics Project

**Programme:** LuxDevHQ Data Engineering / Data Analytics --- Cohort 9\
**Project:** SokoMart Kenya\
**Database:** PostgreSQL\
**Schema:** `sokomart`

## Project overview

This project uses a retail database for SokoMart Kenya to practise SQL
for data analysis and data engineering. The work focuses on querying
customer purchases, product pricing, sales performance, profitability,
payments, database objects, data quality, and query performance.

## Objectives

-   Analyse customer spending and purchasing behaviour.
-   Compare product prices within categories.
-   Calculate monthly revenue, cost, gross profit, and profit margin.
-   Identify products that have never been ordered.
-   Practise joins, subqueries, common table expressions (CTEs), and
    window functions.
-   Build and test database objects such as views, functions,
    procedures, triggers, and indexes.
-   Apply transactions and data-validation techniques.

## Database structure

The project uses the `sokomart` schema. Main tables include:

-   `customers` --- customer details and county.
-   `products` --- product details, category, selling price, cost price,
    and stock.
-   `orders` --- order dates, customer references, status, and shipping
    information.
-   `order_items` --- products and quantities included in each order.
-   `payments` --- payment records.
-   `product_price_history` --- historical product prices.
-   `audit_logs` --- records of selected database actions.
-   `order_status_history` --- order status changes.
-   `payment_staging` --- staged payment records for cleaning and
    deduplication.

Use the supplied project setup scripts and data dictionary as the
authority for the exact columns and constraints in your database.

## Project sections

The assignment contains 25 marked questions and 10 unmarked practice
drills.

  Section   Main topics
  --------- -----------------------------------------------
  A         CTEs and subqueries
  B         Window functions
  C         Views, functions, procedures, and triggers
  D         Transactions and data integrity
  E         Query performance, indexing, and advanced SQL

Refer to the original assignment brief for the exact requirements and
expected output columns for each question.

## Important business rules

-   Revenue is calculated from `order_items.line_total` for orders whose
    status is `completed`.
-   Do not include delivery fees in revenue.
-   Do not use `payments.amount` as sales revenue; use it only for
    payment-related analysis.
-   Product cost is calculated as
    `order_items.quantity * products.cost_price`.
-   Gross profit is revenue minus cost.
-   Profit margin percentage is `(gross profit / revenue) * 100`.
-   Use `customers.county` for a customer's county and
    `orders.shipping_county` when the question asks for the shipping
    county.
-   For timestamp date ranges, use an inclusive start and exclusive end,
    for example:
    `order_date >= '2025-01-01' AND order_date < '2026-01-01'`.

## Tools used

-   PostgreSQL
-   pgAdmin
-   SQL
-   Git
-   GitHub

## How to run the project

1.  Install PostgreSQL and pgAdmin.
2.  Create or open the project database.
3.  Run the supplied database setup scripts in the order specified by
    the assignment.
4.  Confirm that the `sokomart` schema and its tables exist.
5.  Run the SQL solutions section by section.
6.  Compare the results with the assignment requirements.
7.  Save your SQL scripts and supporting documentation in this project
    folder.

**Note:** Do not run scripts that modify or reset data until you have
saved any results or screenshots you need. Follow the assignment's reset
instructions if you need to restore the original data.

## Suggested repository structure

``` text
sokomart-sql-project/
├── README.md
├── sql/
│   ├── section_a_ctes_subqueries.sql
│   ├── section_b_window_functions.sql
│   ├── section_c_database_objects.sql
│   ├── section_d_transactions.sql
│   └── section_e_advanced_sql.sql
└── screenshots/
    └── query-results/
```

Adjust the filenames and folders to match the files you actually create.
Do not upload database passwords, private connection details, or other
secrets to GitHub.

## Author

Add your name and any required cohort details here before publishing.
