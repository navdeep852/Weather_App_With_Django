# Weather_App_With_Django
This repository implements a weather app that uses Open Weather API and Django as a backend framework and deployment using heroku.

Important Links
Deployment using Heroku
Open Weather API
MDN Docs
Summary Workflow
The following is a basic workflow that you can use as a quick reference for developing a Django Project.

Setup
Within a new directory, create and activate a virtualenv.
Install Django.
Create your project:
 django-admin.py startproject  
Create a new app:
 python manage.py startapp  
Add your app to the INSTALLED_APPS tuple.
Add Basic URLs and Views
Map your Project’s urls.py file to the new app.
In your App directory, create a urls.py file to define your App’s URLs.
Add views, associated with the URLs, in your App’s views.py; make sure they return a HttpResponse object. Depending on the situation, you may also need to query the model (database) to get the required data back requested by the end user.
Templates and Static Files
Create a templates and static directory within your project root.
Update settings.py to include the paths to your templates.
Add a template (HTML file) to the templates directory. Within that file, you can include the static file with -
{% load static %}
and
 {% static "filename" %} 
. Also, you may need to pass in data requested by the user.
Update the views.py file as necessary.
Models and Databases
Update the database engine to settings.py (if necessary, as it defaults to SQLite).
Create and apply a new migration.
Create a super user.
Add an admin.py file in each App that you want access to in the Admin.
Create your models for each App.
Create and apply a new migration. (Do this whenever you make any change to a model).
Forms
Create a forms.py file at the App to define form-related classes; define your ModelForm classes here.
Add or update a view for handling the form logic - e.g., displaying the form, saving the form data, alerting the user about validation errors, etc.
Add or update a template to display the form.
Add a urlpattern in the App’s urls.py file for the new view.
User Registration
Create a UserForm
Add a view for creating a new user.
Add a template to display the form.
Add a urlpattern for the new view.
User Login
Add a view for handling user credentials.
Create a template to display a login form.
Add a urlpattern for the new view.
Setup the template structure
Find the common parts of each page (i.e., header, sidebar, footer).
Add these parts to a base template
Create specific. templates that inherent from the base template.
Heroku Hosting
Copy the project seperately
Go to 'Getting Started on Heroku with Python'
Create an Heroku account
install pipenv
Install git ( check git --version)
Install Heroku CLI
Login heroku
Create a virtual enviroment
Run manage.py not gonna run - pip freeze nothing installing
Check which version django,requests you have and install it
Run manage.py and then stop it
Go to django heroku
Create a Procfile and
Install django-heroku
Add stuff to settings.py file
Install guincorn
pip freeze > requirements.txt
heroku create (to create an app on heroku)
git status git commands (git push heroku master)
Open up the website
Admin panel not working. heroku run bash. Migrations
