# Django Authentication System

This project is a Django-based user authentication system that allows users to register, log in using either their username or email, reset their password, and view a user-specific dashboard and profile.

## Features

- **User Registration**: Users can sign up by providing a username, email, and password.
- **Login with Username/Email**: Users can log in using either their username or email.
- **Password Reset**: Users can request to reset their password via email.
- **Change Password**: Logged-in users can change their password.
- **Dashboard**: Displays a personalized greeting message to the logged-in user.
- **Profile Page**: Displays user details such as username, email, date joined.
- **Authentication-based Access Control**: Certain pages, such as the dashboard and profile, are restricted to authenticated users only.

## Prerequisites

Before running this project, make sure you have the following installed:

- Python 3.x
- Django 3.x or higher
- pip (Python package manager)

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/jindalayush326/Authentication-system.git
cd auth

###  2. Create and activate a virtual environment
It's recommended to create a virtual environment to manage dependencies.

bash
Copy code
# On macOS and Linux
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\Scripts\activate

### 3. Configure the database
Run the following commands to set up the database and create the necessary migrations:

bash
Copy code
python manage.py makemigrations
python manage.py migrate

### 4. Run the development server
Start the Django development server using the following command:

bash
Copy code
python manage.py runserver
Visit http://127.0.0.1:8000 in your web browser to view the application.

Add Backend in settings.py
Ensure that the custom authentication backend is registered in your settings.py:

python
Copy code
AUTHENTICATION_BACKENDS = [
    'authapp.backends.EmailOrUsernameModelBackend',
    'django.contrib.auth.backends.ModelBackend',
]
