# Elevate-Labs-Internship-Task-7

# Task 7: Basic Sales Summary Using SQLite and Python

## 📊 Objective
The goal of this task is to analyze a small sales dataset stored in a SQLite database using SQL queries within Python. We then visualize the results using a bar chart.

---

## 🗃️ Dataset
We use a small SQLite database `sales_data.db` containing a single table:

### Table: `sales`
| Column   | Type    | Description             |
|----------|---------|-------------------------|
| id       | INTEGER | Primary key             |
| product  | TEXT    | Name of the product     |
| quantity | INTEGER | Quantity sold           |
| price    | REAL    | Unit price of the product |

Sample data includes products like Apple, Banana, and Orange with various quantities and prices.

---

## 🛠️ Tools Used
- Python
- SQLite (via `sqlite3`)
- Pandas
- Matplotlib
- Jupyter Notebook

---

## 🔍 Steps Performed
1. **Connected to SQLite DB** using `sqlite3.connect("sales_data.db")`
2. **Executed SQL query** to get total quantity and total revenue for each product:
   ```sql
   SELECT product, SUM(quantity) AS total_quantity, SUM(quantity * price) AS revenue
   FROM sales
   GROUP BY product;
3. **Loaded results into Pandas DataFrame** using `pd.read_sql_query()`
4. **Printed DataFrame to see the sales summary**
5. **Plotted a bar chart using matplotlib to visualize revenue by product**

📈 Sample Output
product	total_quantity	revenue
Apple	35	17.5
Banana	25	7.5
Orange	17	11.9

A bar chart visualizing revenue per product was also generated.

📁 Files Included
- `sales_data.db` – SQLite database file
- `task7_sales_summary.ipynb` – Jupyter Notebook
- `sales_chart.png` - Bar Chart of Revenue by Product 
- `README.md` – this file
