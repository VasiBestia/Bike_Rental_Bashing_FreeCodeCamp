# 🚲 Bike Rental Shop — Bash & PostgreSQL

A command-line bike rental application built with **Bash** and **PostgreSQL**, developed as part of the **freeCodeCamp Relational Database Certification**.  
The project simulates a real-world bike rental system where users can rent and return bikes, while the database keeps track of availability and rentals.

---

## 📌 Features

- Interactive **CLI menu** built in Bash
- Rent available bikes
- Return rented bikes
- Persistent data storage using **PostgreSQL**
- Real-time bike availability updates
- Input validation and user-friendly messages

---

## 🛠 Technologies Used

- **Bash** (Shell scripting)
- **PostgreSQL** (Relational Database)
- **psql / pg_dump**
- Linux command-line environment

---

## 🗄 Database Schema

The database includes the following main tables:

- **bikes**
  - `bike_id` (PRIMARY KEY)
  - `type`
  - `size`
  - `available` (BOOLEAN)

- **customers**
  - `customer_id` (PRIMARY KEY)
  - `name`
  - `phone` (UNIQUE)

- **rentals**
  - `rental_id` (PRIMARY KEY)
  - `customer_id` (FOREIGN KEY)
  - `bike_id` (FOREIGN KEY)
  - `date_rented`
  - `date_returned`

---

## ▶️ How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/bike-rental-shop.git
   cd bike-rental-shop
Make the script executable:
```

```bash
chmod +x bike-shop.sh
```
Run the application:

```bash
./bike-shop.sh
```
---
##💾 Database Export
To export the PostgreSQL database as a .sql file:

```bash
pg_dump -U postgres bikes > bike_rental.sql
```
This allows easy backup, sharing, or reuse of the database schema and data.
---
##🧪 Example Workflow
Start the application
Choose a bike to rent
Enter customer details
Return the bike
Bike becomes available again
---
##🎓 What I Learned
Writing interactive Bash scripts
Connecting Bash scripts to PostgreSQL using psql
Designing relational databases
Using constraints (PRIMARY KEY, FOREIGN KEY, UNIQUE)
Managing application state through a database
Exporting and importing databases with pg_dump
---
##📎 Certification
This project is part of the
freeCodeCamp – Relational Database Certification
---
##👤 Author
Alexandru Gabriel Vasilescu
Faculty of Automation and Computers
University Politehnica of Bucharest
