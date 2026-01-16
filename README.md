#CS50 Birthdays
A lightweight web application that allows users to keep track of birthdays. This project demonstrates the integration of a Python Flask backend with a SQLite database and a dynamic HTML/CSS frontend.

## Features
View Birthdays: Displays a clean, organized table of everyone’s birthday stored in the database.

Add New Entries: A simple form to input a name, month, and day.

Persistent Storage: Uses a SQL database to ensure data remains saved even after the server restarts.

Validation: Basic logic to ensure inputs are handled correctly before being stored.

## Tech Stack
Backend: Python & Flask

Database: SQLite3

Frontend: HTML5, CSS3 (via Bootstrap 5), and Jinja2 templating.

## Project Structure
Plaintext
birthdays/
├── app.py           # Flask application logic and SQL queries
├── birthdays.db     # SQLite database containing the birthdays table
├── static/          # CSS styles and UI enhancements
└── templates/       # HTML files (index.html)
## Database Schema
The project uses a single table named birthdays within the birthdays.db file.

Column	Type	Description
id	INTEGER	Primary key (auto-incrementing)
name	TEXT	The name of the person
month	INTEGER	Birth month (1-12)
day	INTEGER	Birth day (1-31)
## Getting Started
1. Prerequisites

You need Python 3 and the cs50 library installed.

Bash
pip install flask cs50
2. Running the App

Navigate to your project folder and start the Flask development server:

Bash
flask run
3. Usage

Open the URL provided by Flask (usually http://127.0.0.1:5000).

Enter a friend's name and birthday in the form at the top of the page.

Click Submit to see the list update instantly.

## Implementation Details
The core of this project involves handling two types of HTTP requests:

GET: The app selects all rows from the birthdays table and renders them in the HTML template.

POST: The app retrieves form data (name, month, day) and executes an INSERT INTO SQL command to add the data to the database.

## Acknowledgments
CS50x: Provided by Harvard University.

Bootstrap: For the responsive UI components.
