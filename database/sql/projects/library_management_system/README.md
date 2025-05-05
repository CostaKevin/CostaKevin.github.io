# 📚 Library Management System (LMS)

## 🧾 Project Overview

This project demonstrates a complete relational database design and SQL querying solution for a **Library Management System**. It includes schema creation, data insertion, and both basic and advanced queries. The goal is to showcase skills in database modeling, normalization, and SQL query writing.

---

## 🗃️ Database Schema

The system consists of the following relational tables:

| Table     | Description                            |
|-----------|----------------------------------------|
| Authors   | Stores author information              |
| Books     | Contains book details                  |
| Members   | Holds data on registered library users |
| Loans     | Tracks book borrow and return activity |
| Fines     | Records fines associated with overdue loans |

### 📌 Entity Relationships

- One **Author** → Many **Books**
- One **Book** → Many **Loans**
- One **Member** → Many **Loans**
- One **Loan** → Zero or One **Fine**

---

## 🧱 Tables and Fields

```sql
authors(author_id, name, country)
books(book_id, title, author_id, genre, published_year)
members(member_id, name, status, email)
loans(loan_id, book_id, member_id, loan_date, return_date)
fines(fine_id, loan_id, amount, paid)
```

---

## 📥 Sample Data

Each table contains a set of meaningful sample entries to simulate real-world operations. The `INSERT INTO` scripts are included in the `/sql` folder.

---

## 🔍 Sample SQL Queries

### ✅ Basic Queries

- List all books and their authors
- View active (unreturned) loans
- Display all registered members

### 📊 Advanced Queries

- Top 3 most borrowed books
- Calculate total fines per member
- List members who borrowed books from multiple genres

---

## 🛠️ Tools Used

- SQL (Microsoft SQL Server Management Studio)
- ERD diagram tool (MySQL Workbench)
- Text editor (VS Code)

---

## 📈 Learning Objectives

- Practice **relational database design** and normalization
- Demonstrate **SQL proficiency** (SELECT, JOINs, GROUP BY, etc.)
- Understand **real-world relationships** in systems
- Apply **data modeling and schema creation**

---

## 📁 Project Structure

```
library_management_system/
├── README.md
├── sql/
│   ├── schema.sql
│   ├── insert_data.sql
│   └── queries.sql
├── diagrams/
│   └── erd.png
└── screenshots/
    └── sample_query_results.png
```

---

## 🧠 Future Improvements

- Add triggers for automatic fine calculation
- Create stored procedures for issuing and returning books
- Introduce user roles (admin, member)

---

## 👨‍💻 Author

**Kevin Costa**  
Data Scientist | Machine Learning Researcher | Python Developer | Scientific Computing

📫 dacosta.kevin.mota@gmail.com  
🌐 https://www.linkedin.com/in/costakevinn/
