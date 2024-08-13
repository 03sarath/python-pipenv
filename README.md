# Simple Flask App with Pipenv

This guide will help you create a simple Flask application using Pipenv for dependency management and virtual environments.

## Prerequisites

- Python installed on your system
- `pip` (Python package manager) installed

## Step 1: Install Pipenv

First, install Pipenv using pip:

```
pip install pipenv
```

## Step 2: Create a Project Directory
Create a directory for your new Flask project and navigate into it:

```
mkdir flask_app
cd flask_app

```

## Step 3: Initialize the Project with Pipenv
Run the following command to create a new virtual environment and a `Pipfile`:

```
pipenv install

```
## Step 4: Install Flask
Use Pipenv to install Flask:
```
pipenv install flask

```
This will add Flask to your `Pipfile` and ensure it's included in your virtual environment.

## Step 5: Create a Simple Flask App
Create a Python script named `app.py` in your project directory:
```
# app.py

from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "Hello, Flask!"

if __name__ == "__main__":
    app.run(debug=True)

```
This script sets up a simple Flask application with one route that returns "Hello, Flask!".

## Step 6: Run Your Flask App
To run your Flask application, use the following command within the Pipenv-managed virtual environment:

```
pipenv run python app.py

```
Open your web browser and go to `http://127.0.0.1:5000/` to see your app in action.

## Step 7: Activate the Virtual Environment (Optional)
If you want to work interactively within the virtual environment, activate it with:
```
pipenv shell

```
Then you can run your app simply with:

```
python app.py

```
## Step 8: Deactivate the Virtual Environment
When you're done, exit the virtual environment with:

```
exit

```