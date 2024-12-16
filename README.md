# CS50w Capstone Project

## Overview

This project is a Django-based web application that allows users to participate in polls. It is structured using Django's MVC (Model-View-Controller) framework and incorporates modularized code and templates for flexibility and scalability. The project demonstrates a complete web application lifecycle, including user interaction, data handling, and dynamic content rendering.

---

## Distinctiveness and Complexity

### Why This Project Satisfies the Requirements

1. **Distinctiveness:**
   - Unlike simple CRUD applications, this project integrates multiple Django apps (`polls` and `pages`) to create a cohesive system. It uses templates, URL routing, and views to provide a comprehensive user experience.
   - Features include user interaction for creating, voting on, and viewing poll results, which go beyond basic functionality and require integrating models, forms, and template inheritance.

2. **Complexity:**
   - Implements custom views and URL patterns for dynamic routing.
   - Uses Django’s ORM for database operations, migrations for schema management, and modular apps for separation of concerns.
   - Incorporates reusable templates for DRY (Don’t Repeat Yourself) principles.
   - Includes navigation via partial templates (e.g., `_navbar.html`).

### File Breakdown

- **`pollmania/`** (Project settings and configurations):
  - `settings.py`: Configuration for the Django project.
  - `urls.py`: URL routing for the project.
  - `wsgi.py` and `asgi.py`: Deployment configurations.

- **`polls/`** (Main app for handling polls):
  - `models.py`: Defines the database schema for polls and choices.
  - `views.py`: Contains logic for displaying polls, voting, and showing results.
  - `urls.py`: Routes specific to the `polls` app.
  - `admin.py`: Registers models for the admin interface.

- **`pages/`** (Additional app for static pages):
  - `views.py`: Logic for rendering static pages like the homepage.
  - `urls.py`: Routes specific to the `pages` app.

- **Templates**:
  - `base.html`: A shared base template for consistent styling.
  - `partials/_navbar.html`: Reusable navigation bar.
  - `polls/index.html`, `polls/detail.html`, `polls/results.html`: Templates specific to polls.

- **Database**:
  - `db.sqlite3`: SQLite database file storing application data.

### How to Run the Application

1. **Install Dependencies**:
   - Ensure Python and pipenv are installed.
   - Run the following command to install dependencies:
     ```bash
     pipenv install
     ```

2. **Apply Migrations**:
   - Set up the database schema by running:
     ```bash
     python manage.py migrate
     ```

3. **Start the Development Server**:
   - Run the Django development server:
     ```bash
     python manage.py runserver
     ```
   - Access the application at `http://127.0.0.1:8000/`.

4. **Navigate the Application**:
   - Visit `/polls/` to view polls, vote, and see results.
   - Visit `/` for the homepage or other static pages.

### Additional Information

- This project is configured with modular apps to ensure scalability.
- Template inheritance is used to maintain a consistent design.
- Follow Django best practices, including separate migrations and reusable components.

---

## Requirements

A `requirements.txt` file is auto-generated using Pipenv. Ensure you install dependencies using:
```bash
pipenv install
```

If you prefer `requirements.txt`, you can generate it using:
```bash
pipenv lock -r > requirements.txt
```

---

## Conclusion

This project demonstrates a well-structured Django application that integrates distinct features and showcases both frontend and backend skills. By following the provided instructions, you can deploy and explore the functionalities with ease.

