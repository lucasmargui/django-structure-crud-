<H1 align="center">Development in Django</H1>

<p align="center">🚀 Development of a CRUD structure for future references</p>

## Resources Used
- Visual Studio 2015
- SQL Server Management Studio (SSMS):
- Python 
- Django

# Initial environment setup

Use the command python -m pip install Django to install Django via pip, Python's package manager.

## Creating the project

<details>
<summary>Click to show details about </summary>

#### Create a Django Project:

Create a new Django project with the command django-admin startproject CrudDjango. This will generate a basic directory and file structure for your project.

```
django-admin startproject CrudDjango
```

#### Create a Module:

A Django app is a self-contained module within a Django project that is designed to perform a specific function. Each app can handle a different aspect of the web application, such as user authentication, blog posts, or a shopping cart. Apps in Django are reusable and can be included in multiple projects.

Run the command python manage.py startapp Home to create a new app named "Home". This will generate a directory with the necessary files for the app.


```
python manage.py startapp Home
```
```
python manage.py startapp Material
```


![image](https://github.com/user-attachments/assets/bd75f72f-3f9f-460b-9dbc-a8703662ab8b)

#### Add the App to INSTALLED_APPS:

Open the settings.py file and add 'Home' to the INSTALLED_APPS list. This step is essential for Django to recognize and apply any changes made within the "Home" app.

![image](https://github.com/user-attachments/assets/61bae140-6d92-4d8f-96db-f4acfaad40c6)


#### Run the Development Server:

Navigate to the project directory and start the development server with the command python manage.py runserver. This will start a local server, allowing you to view your project in a web browser.

```
python manage.py runserver
```


</details>


## Database Connection

<details>
<summary>Click to show details about </summary>

#### Install mssql-django:

To use Microsoft SQL Server with Django, install the mssql-django package using the command: pip install mssql-django.

```
pip install mssql-django.
```

#### Open the settings.py File:

Locate and open the settings.py file, which is typically found in the main directory of your Django project. The project structure might look something like this:

![image](https://github.com/user-attachments/assets/109a5f43-0019-4e74-98e6-7d7d33b982f1)


</details>

# Project Documentation

## Create Models

<details>
<summary>Click to show details about </summary>

In Django, models are the heart of your web application’s data structure. They define the structure of your database, encapsulating essential fields and behaviors of the data you want to store. Each model class typically maps to a single database table, where class attributes represent the columns of the table.

#### Model Material

This Django code defines a model class named Material, which represents a database table where each instance of the class corresponds to a row in that table.

![image](https://github.com/user-attachments/assets/d02a6b8e-f828-4cf7-9122-2e544c1b57c2)

#### Forms based Model Material

This Django code defines a form class called MaterialForm, which is a subclass of forms.ModelForm. This form is specifically designed to work with the Material model, allowing users to create or update Material instances through a web form.

In short, it creates a skeleton of how the model form will be represented on the screen if you directly use {{ form.as_p }}

![image](https://github.com/user-attachments/assets/8e46d51b-a4b0-4df8-9ddc-d53b389cb2b1)


![image](https://github.com/user-attachments/assets/3c15c47c-49ab-4203-9c66-fa16529e6ef2)


</details>

## Migrations

<details>
<summary>Click to show details about </summary>

Creating and applying migrations in Django involves two key commands:

![image](https://github.com/user-attachments/assets/e07c7c27-3cee-40ca-98b1-6f77feac8df2)


#### makemigrations: 

```
python manage.py makemigrations
```

This command generates migration files based on the changes you've made to your models. Migrations are a way to record changes to your database schema, such as creating tables, adding fields, or modifying existing ones. Running makemigrations tells Django to look at your models and create the necessary migration scripts to reflect any changes.

#### migrate:

```
python manage.py migrate
```

This command applies the migration files to your database, executing the necessary SQL commands to update your database schema. Running migrate ensures that your database is synchronized with the current state of your models, applying all pending migrations in the correct order.

![image](https://github.com/user-attachments/assets/f9592e14-cbea-4a4c-8242-9b23249ef506)



</details>

## Template Inheritance

<details>
<summary>Click to show details about </summary>


#### Config Templates

Make sure the configuration for the template directories is correct. Typically there should be something like this

![image](https://github.com/user-attachments/assets/e50186d4-95a3-48e4-9277-0dc0b414964f)

#### Layout (Master Page):

Create a base template file: Typically, this file is called base.html and is located in your application's templates folder or project's templates directory.

![image](https://github.com/user-attachments/assets/83b535ee-baa6-4396-9232-88093580df1d)

###### Base.html

![image](https://github.com/user-attachments/assets/13e08718-7b78-4711-a006-49cc80f0ec1b)


#### Rendering Content

Create other templates that extend the base template: In each of your individual templates, you use the {% extends %} tag to inherit the base.html structure and define the specific content with the {% block %} tag

![image](https://github.com/user-attachments/assets/3335f32a-31f9-476b-a763-bfd64678a5ea)

![image](https://github.com/user-attachments/assets/6eb8a96d-7956-4b2e-b87f-ad2439ab9438)


</details>

## Controller

<details>
<summary>Click to show details about </summary>

#### Creating a Controller:

### Actions

#### Index():

#### Details(ByVal id As Integer?):

#### Create():

#### Create(ByVal materialMovel As MaterialMovel):

#### Edit(ByVal id As Integer?):

#### Edit(ByVal materialMovel As MaterialMovel):

#### Delete(ByVal id As Integer?):

#### DeleteConfirmed(ByVal id As Integer):

</details>

## Routes

<details>
<summary>Click to show details about </summary>

</details>

## Views

<details>
<summary>Click to show details about </summary>


</details>



![image](https://github.com/user-attachments/assets/17e52a87-e329-4e1a-a772-0d98eaba4985)

![image](https://github.com/user-attachments/assets/cc25463b-fd75-4d12-a4b8-105ab16d332d)

![image](https://github.com/user-attachments/assets/41e39ef6-09f9-408a-a7f8-574783549d9c)

![image](https://github.com/user-attachments/assets/62738a6b-cb1d-4f85-ad39-af5037f7c2b8)

