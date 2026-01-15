<div align="center">

# 🚲 Bike Rental Shop

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Shell Script](https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-```bash&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![FreeCodeCamp](https://img.shields.io/badge/FreeCodeCamp-Certification-0a0a23?style=for-the-badge&logo=freecodecamp&logoColor=white)

**A command-line bike rental application built with ```bash and PostgreSQL.** *Developed as part of the freeCodeCamp Relational Database Certification.*

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-database-schema">Schema</a> •
  <a href="#-how-to-run">How to Run</a> •
  <a href="#-author">Author</a>
</p>

</div>

---

## 📖 About
This project simulates a real-world bike rental system management tool. It allows users to rent and return bikes interactively via the terminal, while a persistent PostgreSQL database tracks inventory availability and customer history in real-time.

## 📌 Features

* 🖥️ **Interactive CLI:** Menu-driven interface built entirely in ```bash.
* 🚲 **Rental Management:** Rent available bikes and return them seamlessly.
* 💾 **Persistent Storage:** Data is stored securely in PostgreSQL.
* ⚡ **Real-time Updates:** Instant availability status changes upon rental/return.
* 🛡️ **Validation:** Input validation and user-friendly error messages.

---

## 🗄 Database Schema

The system relies on three main relational tables:

| Table | Primary Key | Columns | Description |
| :--- | :--- | :--- | :--- |
| **`bikes`** | `bike_id` | `type`, `size`, `available` (BOOL) | Inventory of bikes and current status. |
| **`customers`** | `customer_id` | `name`, `phone` (UNIQUE) | Customer contact information. |
| **`rentals`** | `rental_id` | `customer_id`, `bike_id`, `date_rented`, `date_returned` | Links customers to bikes; tracks history. |

---

## 🛠 Technologies Used

* **Bash (Shell Scripting):** Core logic and user interface.
* **PostgreSQL:** Relational database management.
* **Linux/Unix Environment:** Standard command-line tools.
* **pg_dump:** For database backup and portability.

---

## ▶️ How to Run

### 1. Prerequisites
Ensure you have **PostgreSQL** installed and running on your machine.

### 2. Installation
Clone the repository and navigate to the folder:

```bash
git clone [https://github.com/your-username/bike-rental-shop.git](https://github.com/your-username/bike-rental-shop.git)
cd bike-rental-shop
```
3. Permissions
Make the script executable:

```bash

chmod +x bike-shop.sh
```
4. Setup Database
(Optional) Restore the database schema if starting fresh:

```bash

psql -U postgres < bike_rental.sql
```
5. Run the Application
Start the interactive menu:

```bash

./bike-shop.sh
```
---
💾 Database Operations
To export the current state of the database (schema + data) for backup:

```bash

pg_dump -U postgres bikes > bike_rental.sql
```
---
🧪 Workflow Example
Start App: Run ./bike-shop.sh.
Rent: Select "Rent a bike" from the menu.
Select: Choose a bike type (e.g., Mountain) and size (e.g., 28).
Customer: Enter your phone number (if new, you will be prompted for a name).
Return: Later, run the script again and select "Return a bike" to mark it available.
---
🎓 Learning Outcomes
This project demonstrates competency in:
✅ Writing advanced interactive Bash scripts.

✅ Connecting shell scripts to PostgreSQL using psql.

✅ Designing relational database schemas with constraints (FK, PK, UNIQUE).

✅ Managing application state via database transactions.

✅ Data persistence and database dumping/restoring.
---
👤 Author
Alexandru Gabriel Vasilescu Faculty of Automation and Computers
