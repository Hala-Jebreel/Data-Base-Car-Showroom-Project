#  Car Showroom Management System | Final Database Project

This is a full-stack car showroom system built with **MySQL** (for database backend) and **Flask** (for web frontend). It allows admins and users to manage cars, customers, services, appointments, and sales interactively.



---

## Project Structure

| File / Folder                     | Description                                      |
|----------------------------------|--------------------------------------------------|
| `SQL.txt`                        | Full SQL schema with test data for all tables    |
| `app.py`                         | Python Flask backend with routes, views, logic   |
| `templates/` (not shown)         | Jinja2 HTML templates for the UI                 |
| `static/images/`                 | Uploaded car images                              |

---

##  Technologies Used

- **MySQL** – Relational DB (with advanced constraints, FKs, triggers, view)
- **Python Flask** – Web framework
- **HTML/CSS + Jinja2** – Frontend rendering
- **Bootstrap** – For UI styling (if applied)
- **MySQL Connector/Python** – DB connectivity

---

## Features

###  Car Management
- Add, update, delete cars with images
- Filter cars by year, make, and price

### 👥 Employee Management
- CRUD employee records with phone and email
- Grouped by role (e.g., Technician, Salesperson)
- Status toggle (active/inactive)

### 📅 Appointment Booking
- Add, edit, search, delete appointments
- Analytics (peak reservation times, top purposes)

### 👨‍👩‍👧 Customer Management
- View and add customers
- Delete functionality included

### 🧾 Sales and Invoicing
- Record car or service sales
- Auto-update car status to “Sold”
- Generate digital invoice (`/pill/<sale_id>`)

###  Services
- CRUD operations for services
- Assign employee to each service

###  Order Lines + Staff Assignment
- Breakdown of sale into cars/services
- Assign staff to each order line with role

---

##  View Example

 **`/order-totals`** displays sale totals using a live SQL view  
 **`/analytics/appointments`** shows top reserved purposes and peak months  

---

##  Setup Instructions

1. Make sure MySQL is running and create a `Cars` database
2. Import `SQL.txt` into MySQL (includes schema + data)
3. Run Flask app:

```bash
pip install flask mysql-connector-python
python app.py
