# Django Polls App

## Overview
This is a simple Polls application built using [Django](w), following the official Django documentation tutorial. It allows users to create polls with multiple-choice questions and vote on them.

## Features
- Create, edit, and delete polls through the Django admin panel
- Users can vote on polls
- Displays poll results after voting
- Built using Django's Model-View-Template (MVT) architecture
- Uses SQLite as the default database

## Installation
### Prerequisites
Ensure you have the following installed:
- Python (>=3.8)
- Git
- Virtual environment (optional but recommended)

### Setup Instructions
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/django-polls.git
   cd django-polls
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

4. Apply database migrations:
   ```sh
   python manage.py migrate
   ```

5. Create a superuser to access the admin panel:
   ```sh
   python manage.py createsuperuser
   ```
   Follow the prompts to set up the superuser credentials.

6. Run the development server:
   ```sh
   python manage.py runserver
   ```
   The app should now be accessible at `http://127.0.0.1:8000/`

## Usage
1. Access the admin panel at `http://127.0.0.1:8000/admin/` to create polls.
2. Visit `http://127.0.0.1:8000/polls/` to view and vote on polls.

## Project Structure
```
.
├── mysite/                  # Main Django project
│   ├── __pycache__/
│   ├── __init__.py          # Package file
│   ├── settings.py          # Django settings
│   ├── urls.py              # URL configurations
│   ├── wsgi.py              # WSGI entry point
│   └── asgi.py              # ASGI entry point
│
├── polls/                   # Polls application
│   ├── __pycache__/
│   ├── __init__.py          # Package file
│   ├── migrations/          # Database migrations
│   ├── templates/polls      # HTML templates
│   ├── static/polls         # Static files
│   ├── views.py             # Views for handling requests
│   ├── models.py            # Database models
│   ├── urls.py              # URL routing
│   ├── forms.py             # Forms for user input
│   └── admin.py             # Admin panel configurations
│
├── db.sqlite3               # SQLite database
├── manage.py                # Django CLI tool
└── requirements.txt         # Python dependencies 
```

## API Endpoints
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/polls/` | GET | List all available polls |
| `/polls/<poll_id>/` | GET | View details of a specific poll |
| `/polls/<poll_id>/vote/` | POST | Submit a vote for a poll |

## Deployment
To deploy the application using [Gunicorn](w) and [Nginx](w):
1. Install Gunicorn:
   ```sh
   pip install gunicorn
   ```
2. Run the app with Gunicorn:
   ```sh
   gunicorn mysite.wsgi:application --bind 0.0.0.0:8000
   ```
3. Configure Nginx as a reverse proxy (optional for production).

## Contributing
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-branch`
3. Make your changes and commit: `git commit -m "Added a new feature"`
4. Push to the branch: `git push origin feature-branch`
5. Submit a Pull Request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact
For any queries, reach out via:
- GitHub Issues
- Email: abdulmoizniazi@gmail.com

