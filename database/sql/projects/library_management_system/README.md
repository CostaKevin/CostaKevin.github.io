# 📚 Library Management System (LMS)

## 🧾 Project Overview

This project demonstrates a complete relational database design and SQL querying solution for a **Library Management System**. It includes schema creation, data insertion, and both basic and advanced queries. The goal is to showcase skills in database modeling, normalization, and SQL query writing.

---

## 🗃️ Database Schema

The system consists of the following relational tables:

| Table        | Description                            |
|--------------|----------------------------------------|
| authors      | Stores author information              |
| books        | Contains book details                  |
| members      | Holds data on registered library users |
| loans        | Tracks book borrow and return activity |
| fines        | Records fines associated with overdue loans |
| book_authors  | Junction table for books and authors   |

### 📌 Entity Relationships

- One **Author** → Many **Books**
- One **Book** → Many **Authors**
- Many-to-Many relationship handled via **BookAuthors**
- One **Book** → Many **Loans**
- One **Member** → Many **Loans**
- One **Loan** → Zero or One **Fine**

---

## 🧱 Tables and Fields

```sql
authors(AuthorID, Name, Country)
books(BookID, Title, Genre, PublishedYear)
members(MemberID, Name, JoinDate, Email)
loans(LoanID, BookID, MemberID, LoanDate, ReturnDate)
fines(fine_id, Loan_id, amount, paid)
book_authors(book_id, author_id)
```

- `BookAuthors` is a junction table to support the many-to-many relationship between Books and Authors.

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
lms-sql-project/
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
- Add UI integration via web or Python app

---

## 🧠 Design Reflection

In this version, I’ve included a dedicated `Fines` table to manage overdue penalties separately from the `Loans` table. This separation allows for cleaner data organization and better scalability. In future improvements, I plan to expand this table to support more detailed tracking — such as timestamps for when fines were issued and paid, user who processed the fine, fine reason codes, and even audit logs for payment history. These changes will make the system more robust and ready for production-scale environments.

---

## 👨‍💻 Author
**Kevin Costa**  
Data Scientist | Machine Learning Researcher | Python Developer | Scientific Computing

📫 dacosta.kevin.mota@gmail.com

🌐 https://www.linkedin.com/in/costakevinn/
