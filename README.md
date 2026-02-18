# Complete Local Development Setup Guide for Pollster-app (for Linux)

## Step 1: Install Python
- If Python is not already installed, install it.
- To verify installation, type `python` in your shell.

## Step 2: Create a Virtual Environment to Clone and Install Requirements
- Create a new virtual environment:

```bash
$ python3 -m venv ~/.virtualenvs/djangodev
```
- The path specifies where the environment will be saved on your computer.
- Activate the virtual environment:

```bash
$ source ~/.virtualenvs/djangodev/bin/activate
```
- If the `source` command is unavailable, use a dot instead:

```bash
$ . ~/.virtualenvs/djangodev/bin/activate
```
- The name of the currently activated virtual environment appears on the command line for easy tracking.

## Step 3: Clone the Repository
```bash
git clone https://github.com/discreetso/Pollster-app.git
dd Pollster-app
```

## Step 4: Install Dependencies
- With the virtual environment activated, install all required packages:
```bash
$ pip install -r requirements.txt
```
- This installs dependencies including:
  - Django 6.0.2 — Web framework
  - django-debug-toolbar — Debugging tool
  - gunicorn — Production WSGI server
  - psycopg — PostgreSQL database adapter
  - whitenoise — Static file handling
  - And other required packages.

## Step 5: Database Setup 
- Ensure PostgreSQL is installed and running.
- Run migrations:
```bash
$ python manage.py migrate
```
 
## Step 6: Run Development Server 
```bash 
$ python manage.py runserver 
```
- Visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.
