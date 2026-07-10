# University Course Management System

A full-stack **Database Management System (DBMS)** project that provides a complete solution for managing university course registration, student records, teacher assignments, and analytics.

The project is developed in four phases, covering database design, backend API development, and an interactive analytics dashboard.

---

## Features

* Student registration
* Course management
* Teacher management
* Course enrollment
* Credit limit validation
* Department and semester-wise course listing
* Interactive analytics dashboard
* RESTful API using Flask

---

## Tech Stack

| Technology | Purpose            |
| ---------- | ------------------ |
| SQLite     | Database           |
| Flask      | Backend REST API   |
| Streamlit  | Frontend Dashboard |
| Pandas     | Data Analysis      |

---

## Project Structure

```text
University_course_Project/
│
├── database/
│   └── university.db
│
├── phase2_database_design/
│   ├── schema.sql
│   └── create_database.py
│
├── phase3_backend_flask/
│   ├── app.py
│   └── database.py
│
└── phase4_analytics_streamlit/
    ├── dashboard.py
    ├── add_student.py
    ├── view_students.py
    ├── teachers.py
    └── analytics.py
```

---

## Database Schema

### Students

* Roll Number *(Primary Key)*
* Name
* Department

### Courses

* Course ID *(Primary Key)*
* Course Code
* Course Name
* Department
* Semester
* Course Type *(Core/Elective)*
* Credits

### Student Courses

Maps students to the courses they are enrolled in.

### Teachers

Stores teacher information.

### Teacher Courses

Maps teachers to the courses they teach.

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/University_course_Project.git
cd University_course_Project
```

### 2. Install Dependencies

```bash
pip install flask streamlit pandas
```

### 3. Create the Database

```bash
cd phase2_database_design
python create_database.py
```

### 4. Start the Flask Server

```bash
cd phase3_backend_flask
python app.py
```

### 5. Launch the Streamlit Dashboard

```bash
cd phase4_analytics_streamlit
streamlit run dashboard.py
```

---

## API Endpoints

| Method | Endpoint                           | Description                              |
| ------ | ---------------------------------- | ---------------------------------------- |
| GET    | `/courses/<department>/<semester>` | Retrieve available courses               |
| POST   | `/register_student`                | Register a student and enroll in courses |
| GET    | `/students`                        | Retrieve all registered students         |

---

## Project Workflow

```
SQLite Database
        │
        ▼
Flask REST API
        │
        ▼
Streamlit Dashboard
        │
        ▼
Analytics & Reports
```

---

## Future Enhancements

* User authentication
* Admin dashboard
* Student login portal
* Attendance management
* Grade management
* Email notifications
* Data visualization with charts
* Export reports to PDF and Excel

---

## Author

Developed as a **Database Management System (DBMS)** course project to demonstrate full-stack database application development using **SQLite**, **Flask**, and **Streamlit**.
