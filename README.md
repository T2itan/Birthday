# CS50 Birthdays

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
├── app.py           # Python backend; handles routing and SQL logic
├── birthdays.db     # SQLite database; stores name, month, and day data
├── static/          # Contains static assets like styles.css
│   └── styles.css   # Custom CSS for the frontend design
└── templates/       # Jinja2 templates for the user interface
    └── index.html   # The main (and only) page for the application
    ### Key File Responsibilities

app.py: The "brain" of the project. It configures the Flask application and provides the routes for GET (viewing birthdays) and POST (saving new birthdays).

birthdays.db: A relational database. This is where your data persists so that your birthdays aren't lost when you close the browser.

templates/index.html: Contains the HTML structure and uses Jinja2 syntax (like {% for ... %}) to dynamically generate the table rows from the database.

static/styles.css: Used to override default Bootstrap styles or add custom flair to your "Add Birthday" form.
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
