# Haven Real Estate Management System

A Django and SQLite property listing app with account registration, property search and management, contact inquiries, and a staff dashboard.

## Run locally

```powershell
python -m pip install -r requirements.txt
python manage.py migrate
python manage.py seed_demo_properties
python manage.py createsuperuser
python manage.py runserver
```

The seed command adds six fictional, repeatable sample listings for local search previews. Open `http://127.0.0.1:8000/`. The staff dashboard is available after signing in with a staff account. Django's built-in management interface is at `/django-admin/`.

Property photos are stored under `media/` during development. Bootstrap and the display fonts are loaded from their CDNs; property photography on the landing page uses Unsplash image URLs.

## Main routes

- `/` home page
- `/properties/` searchable property directory
- `/properties/add/` authenticated property listing form
- `/dashboard/` member dashboard or staff dashboard
- `/register/`, `/login/`, `/profile/`
- `/about/`, `/contact/`
- `/django-admin/` Django admin