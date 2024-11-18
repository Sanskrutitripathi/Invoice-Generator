# Invoice Generator

A Python-based application for generating invoices, managing customer information, and storing data in a PostgreSQL database. The program also provides features to search, view, and delete customer information, making it a comprehensive solution for invoice and customer management.

---

## Features

- **Customer Management**: Add, search, view, and delete customer details.
- **Invoice Generation**: Create professional PDF invoices with detailed itemized information.
- **Database Integration**: Store and manage customer information and invoices using PostgreSQL.
- **Dynamic Tax Calculation**: Automatically calculates taxes and displays total amounts on invoices.

---

## Prerequisites

Ensure you have the following installed on your system:

- Python (version 3.8 or later)
- PostgreSQL (database setup required)
- Required Python libraries (install using `pip`):
  - `pandas`
  - `psycopg2`
  - `fpdf`
  - `datetime`
  - `re`

---

## Database Setup

Run the following SQL commands in your PostgreSQL database:

```sql
CREATE TABLE customer_info (
    customer_id SERIAL PRIMARY KEY,
    first_name VARCHAR(255),
    last_name VARCHAR(255),
    mobile_number VARCHAR(10),
    email VARCHAR(255),
    address VARCHAR(255),
    total_amount_spent NUMERIC(10, 2) DEFAULT 0
);

-- To view all customer data
SELECT * FROM customer_info;
