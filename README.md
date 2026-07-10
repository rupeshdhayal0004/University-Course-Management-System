# University-Course-Management-System-UCMS-
University Course Management System

A DBMS course project implementing a course registration and analytics system for a university, built in four phases: database design, a Flask REST API backend, and a Streamlit analytics dashboard.

Project Structure

University_course_Project/
├── database/
│   └── university.db              # SQLite database file
├── phase2_database_design/
│   ├── schema.sql                 # Table definitions + seed data
│   └── create_database.py         # Script to build the DB from schema.sql
├── phase3_backend_flask/
│   ├── app.py                     # Flask REST API
│   └── database.py                # DB connection helper
└── phase4_analytics_streamlit/
    ├── dashboard.py                # Streamlit dashboard entry point
    ├── add_student.py              # Student registration UI
    ├── view_students.py            # View/browse students
    ├── teachers.py                 # Teacher management
    └── analytics.py                # Analytics & reports

Database Schema

The database has three core tables:

students — roll number (PK), name, department

courses — course id (PK), code, name, department, semester, type (core/elective), credits

student_courses — join table linking students to their registered courses

teachers / teacher_courses — teacher records and their course assignments

Tech Stack

Database: SQLite

Backend: Flask (Python REST API)

Frontend/Analytics: Streamlit

Getting Started

1. Clone the repo

git clone <your-repo-url>
cd University_course_Project

2. Install dependencies

pip install flask streamlit pandas

3. Build the database (if needed)

cd phase2_database_design
python create_database.py

4. Run the Flask backend

cd phase3_backend_flask
python app.py

5. Run the Streamlit dashboard

cd phase4_analytics_streamlit
streamlit run dashboard.py

API Endpoints (Flask)

Method

Endpoint

Description

GET

/courses/<dept>/<semester>

Get core & elective courses for a department/semester

POST

/register_student

Register a student and enroll them in courses (with credit-limit validation)

GET

/students

List all registered students



Author

Built as a DBMS course project.

Author

Built as a DBMS course project.
