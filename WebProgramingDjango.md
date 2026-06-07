** WEB PROGRAMMING USING DJANGO FRAMEWORK **

1. Installing Django

   > pip install django

2. Creating a Django Project

   > python -m django startproject <project-name>

3. Running the server
   > cd DjangoProj
   > python manage.py runserver

- Django applications are independent modules of the Django project

4. Creating a Django application

   > python manage.py startapp app_name

- The response of a view function should always be a HTTPResponse imported from django.http module
- For logical separation of code, html files can be placed within 'template' folder and static files such as css, js, images under 'static' folder

- {% load static %}: provides access to all static files inside static folder

- render(): used to return .html file, request object as argument and renders required template as response

- All the user-defined model classes must inherit the base class 'Model' from django.db.models

5. Performing Database Migrations

   # generates corresponding SQL commands for all changes done in 'models.py' module

   > python manage.py makemigrations

   # execute generated commands in database

   > python manage.py migrate

6. Passing data to template
   - data from view is passed to template as optional argument in render() : context parameter
