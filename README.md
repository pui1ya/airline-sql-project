# ✈️ Airline Data Analysis with SQL

This project showcases end-to-end handling of an airline dataset — from cleaning and normalization to writing analytical SQL queries — using MySQL. It simulates how real-world airline performance data can be modeled and analyzed using relational databases.

---

## 📂 Dataset Overview

The original dataset was cleaned and contained the following key features:

| Column Name                  | Description                                      |
|-----------------------------|--------------------------------------------------|
| `iata_code`                 | Unique airline identifier code                   |
| `airline_name`             | Name of the airline                              |
| `region`                   | Operating region (e.g., Asia, Europe)            |
| `functional_currency`      | Currency used in financial reporting             |
| `ebit_usd`                 | Earnings Before Interest and Tax (in USD)        |
| `load_factor`              | Percentage of available seating capacity used    |
| `low_cost_carrier`         | Boolean indicating LCC status                    |
| `airline_age`              | Age of the airline                               |
| `num_routes`               | Number of routes operated                        |
| `passenger_yield`         | Revenue earned per passenger                     |
| `ask`                      | Available seat kilometers                        |
| `avg_fleet_age`            | Average age of aircraft fleet                    |
| `fleet_size`               | Number of aircraft in operation                  |
| `aircraft_utilisation`     | Average usage per aircraft                       |

---

## 🧱 Database Design (Normalization)

To improve query efficiency and reduce redundancy, the cleaned dataset was normalized into the following relational tables:

- **Airlines**
  - `airline_id` (PK)
  - `iata_code`
  - `airline_name`
  - `airline_age`
  - `avg_fleet_age`
  - `fleet_size`
  - `low_cost_carrier` (FK from `low_cost_types`)
  - `region_id` (FK from `regions`)
  - `currency_id` (FK from `currencies`)

- **Regions**
  - `region_id` (PK)
  - `region_name`

- **Currencies**
  - `currency_id` (PK)
  - `functional_currency`

- **Low_Cost_Types**
  - `low_cost_id` (PK)
  - `low_cost_label` (e.g., Yes/No)

- **Metrics**
  - `airline_id` (FK)
  - `load_factor`
  - `ebit_usd`
  - `num_routes`
  - `passenger_yield`
  - `ask`
  - `aircraft_utilisation`

---

## 📊 Sample Analytical Queries

- Top 5 airlines by passenger yield
- Load factor comparison by region
- Fleet utilization trends across low-cost and legacy carriers
- Correlation between airline age and EBIT performance

---

## 🚀 How to Run

1. Import `cleaned_airline_data.csv` into MySQL
2. Use the schema:
   USE sql1;
3. Run the CREATE TABLE and INSERT INTO ... SELECT commands from setup.sql (link your file here)
4. Explore insights using analytical queries from analysis.sql

---

🔐 Project Goals
-Practice SQL data modeling and relational design
-Apply normalization (1NF → 3NF)
-Write insightful business intelligence queries
-Learn how to work with Git and GitHub using SSH

📁 Folder Structure
pgsql
Copy
Edit
airline-sql-project/
│
├── cleaned_airline_data.csv     # Preprocessed dataset
├── setup.sql                    # All CREATE TABLE + INSERT queries
├── analysis.sql                 # Business insights using SQL
├── ERD.png                      # Entity Relationship Diagram
└── README.md                    # Project documentation
🧠 Skills Demonstrated
SQL (DDL, DML, Joins, Group By, Subqueries)

Data normalization (1NF, 2NF, 3NF)

Database design & ERD

Git & GitHub (SSH workflow)

📌 Author
Punyashree Somashekara
Aspiring Data Analyst and AI enthusiast
LinkedIn: https://www.linkedin.com/in/punya-shree-s-624a40293/

