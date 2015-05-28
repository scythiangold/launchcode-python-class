# Problem Set 4 - Django

## Introduction
This exercise assumes that you know some basics about Django and Python, and that you've completed either the jQuery or Angular edition of the [LaunchCode Javascript Class](https://github.com/chrisbay/launchcode-javascript-class).

We'll create a simple Django app that allows a to-do list to be persisted.

## Getting ready
You should familiarize yourself with Python and Django basics. This project assumes that you're using Python 3.2 or later and Django 1.8

For practicing Python, you can dive into the [LaunchCode Python Class]() (*Note: this is still a work in progress), or hack away the [Treehouse Python Basics course](http://teamtreehouse.com/library/python-basics) (for ReBootU students, you'll find Treehouse login info in Blackboard).

For setting up your Django project, the official Django site tutorial is a great reference:
* [Writing your first Django app, part 1](https://docs.djangoproject.com/en/1.8/intro/tutorial01/): project setup and models (you can skip the API) section
* [Writing your first Django app, part 3](https://docs.djangoproject.com/en/1.8/intro/tutorial03/): URL routing, views, and template rendering

You'll need some more details on Django, so be sure to check out the References section.

## What to do
1. Set up a basic Django project in PyCharm.
2. Create an app: `python manage.py startapp [appname]`
3. Set up your `urls.py` file at the project level, and the app level
4. Create a `templates/[appname]` folder in your app directory, and add an `index.html` template. Place your task list markup in this template.
5. Add a `static` folder at the top level of your project, and drop in your CSS and JS (including Bootstrap and jQuery or Angular). Modify your template to properly include the static files.
6. Add a request handler in your `views.py` for your app that simply renders the `index.html` template. Be sure that you have a route set up to this view function. Fire up your app and test.
7. Create a `Task` model class in your `models.py` file in your app. It should store any fields that you've associated with your task in the front end (e.g. text, completion status, due date, etc). Remember that Django model classes should *not* have constructors in most situations. You'll use model queries to create and access class instances.
8. Your app front-end will interact with the back-end via AJAX, so add view functions for any actions that should update your model (create, update/complete, delete, etc). For now, these functions can simply return an empty [`JsonResponse`](https://docs.djangoproject.com/en/1.8/ref/request-response/#jsonresponse-objects) 
9. Connect your front-end event handlers to your back-end using [jQuery's `.post()` method](http://api.jquery.com/jquery.post/) 
10. Fill out your view handlers to properly update the model when an incoming request is received.

You can also reference the project code in the [example task list project repository](https://github.com/chrisbay/get-it-done-django) as a reference.

## References
* [Python 3.4 language reference](https://docs.python.org/3/reference/)
* [Writing your first Django app](https://docs.djangoproject.com/en/1.8/intro/tutorial01/)
* [Django request and response objects](https://docs.djangoproject.com/en/1.8/ref/request-response/) (includes JsonResponse object)
* [jQuery `.post()` reference](http://api.jquery.com/jquery.post/)
* [Using Django models](https://docs.djangoproject.com/en/1.8/topics/db/models/) (setting up your classes, persistence, and persistence relationships)
* [Django model queries](https://docs.djangoproject.com/en/1.8/topics/db/queries/) (creating, accessing, and updating your model data)
* [Django template tags](https://docs.djangoproject.com/en/1.8/ref/templates/builtins/)