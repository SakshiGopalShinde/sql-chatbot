AI-Assisted SQL Database Chat Assistant
Overview

This project is an AI-assisted SQL chat application that allows users to interact with a relational database using plain English instead of writing SQL manually.

The main goal of the project is to make database querying easier for non-technical users while still keeping SQL at the core of the system. Every user question is converted into a real SQL query, executed on a MySQL database, and the results are presented in a readable format along with optional visualizations.

This project demonstrates practical usage of:

SQL and relational databases

Backend development with Python and Flask

Natural language to SQL conversion

Data analysis and visualization

What the Project Does

The system allows users to:

Ask questions in plain English

Automatically generate valid SQL queries

Execute those queries on a MySQL database

View results as tables

Generate charts like bar graphs, pie charts, line plots, and histograms when requested

The focus of the project is not just AI, but how AI is used to drive SQL-based data analysis.

How It Works (High Level)

The user enters a question in natural language.

The backend sends the question to an LLM configured for SQL generation.

The model generates a SQL SELECT query based on the database schema.

The query is executed using SQLAlchemy.

Results are loaded into a Pandas DataFrame.

The response is returned as:

The generated SQL query

A short human-readable summary

A table of results

A chart (if requested)

Example

User question:
“Show total donations by state as a pie chart”

Generated SQL:

SELECT state, SUM(amount) AS total_donations
FROM donations
GROUP BY state;


Output:

Tabular result of states and donation totals

Pie chart showing contribution distribution

Summary explaining what the query represents

SQL Focus of the Project

Although the interface is conversational, the system is strongly SQL-driven.

The project makes real use of:

SELECT queries

GROUP BY, ORDER BY

Aggregation functions (SUM, COUNT, AVG)

Filtering and data summarization

Every answer shown to the user is backed by an actual SQL query executed on the database.

This makes the project relevant for:

Data analyst roles

Backend roles involving databases

SQL-heavy interview discussions

Tech Stack
Backend

Python

Flask

SQLAlchemy

PyMySQL

Pandas

Database

MySQL

AI / NLP

LangChain (SQLDatabase utilities)

OpenRouter LLM API

Natural language to SQL generation

Visualization

Matplotlib

Plotly (conceptual support)

Frontend

HTML

CSS

JavaScript (Fetch API)

***Project Directory Structure
SQL-CHATBOT/
│
├── app.py                  # Main Flask application entry point
├── requirements.txt        # Python dependencies
├── render.yaml             # Deployment config (Render)
├── .env                    # Environment variables (NOT committed)
├── .gitignore              # Git ignore rules
│
├── templates/
│   └── index.html          # Frontend chat UI
│
├── static/
│   └── charts/             # Generated chart images (optional persistence)
│
├── utils/
│   ├── __pycache__/        # Python cache (ignored)
│   ├── db.py               # Database connection & SQLAlchemy setup
│   ├── llm.py              # LLM / OpenRouter configuration
│   ├── sql_generator.py    # Natural language → SQL generation logic
│   ├── sql_agent.py        # LangChain SQL agent orchestration
│   ├── charts.py           # Chart generation (matplotlib / plotly)
│   └── answer_formatter.py # Formats SQL results into readable responses
│
├── data/
│   ├── donation_data.csv   # Sample dataset
│   └── csv_to_sql.py       # Script to load CSV data into MySQL
│
└── README.md               # Project documentation

<img width="1833" height="925" alt="image" src="https://github.com/user-attachments/assets/708d0258-e729-4fc0-b1a5-73c6b2588f96" />
<img width="1714" height="956" alt="image" src="https://github.com/user-attachments/assets/94b9c099-a435-460c-948d-f365e4212b91" />
<img width="982" height="852" alt="image" src="https://github.com/user-attachments/assets/1414afba-c902-43a9-bb62-51b9ccd1a9cb" />
<img width="775" height="804" alt="image" src="https://github.com/user-attachments/assets/8ffa5f8e-8ea5-4b80-9eb7-bfaae8f1a21b" />


Why This Project Is Useful

Shows real SQL usage, not mock data

Demonstrates how AI can be used practically with databases

Makes data accessible to non-technical users

Combines backend, SQL, and data visualization in one project

Easy to explain in interviews and easy to extend

Possible Improvements

Support for multiple databases (PostgreSQL, SQLite)

User authentication

Query history and exports

Better SQL explanations for learning purposes

Deployment on a cloud platform

Author

Sakshi Gopal Shinde
Computer Engineering Student

Satara, Maharashtra
Email: sakshishinde0808@gmail.com

LinkedIn: https://tinyurl.com/ykhnd9d7
