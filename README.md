# Basic User Authentication Using Flask

User authentication is important for protecting sensitive information and resources from unauthorized access. It helsp ensure that only authorized users can access and make changes to data, and helps prevent unauthorized users from gaining access to sensitive information.

## Libraries

- <ins>Flask</ins> is a simple, easy-to-use microframework for Python that helps you build scalable and secure web applications.
- <ins>Flask-Login</ins> provides user session management for Flask. It handles the common tasks of logging in, logging out, and remembering users' sessions over extended periods of time.
- <ins>Flask-Bcrypt</ins> is a Flask extension that provides bcrypt hashing utilities for your application.
- <ins>Flask-WTF</ins> is a simple integration of Flask and WTForms that helps you create forms in Flask.
- <ins>Flask-Migrate</ins> is an extension that handles SQLAlchemy database migrations for Flask applications using Alembic. The database operations are made available through the Flask command-line interface.
- <ins>Flask-Testing</ins> extension provides unit testing utilities for Flask.
- <ins>Python Decouple</ins> helps you use environment variables in your Python Project.

## File Structure

```
Basic-Authentication-Flask
|   .env
|   config.py
|   manage.py
|   README.md
|   requirements.txt
|   
+---src
|   |   __init__.py
|   |   
|   +---accounts
|   |       forms.py
|   |       models.py
|   |       views.py
|   |       __init__.py
|   |       
|   +---core
|   |       views.py
|   |       __init__.py
|   |       
|   +---static
|   |       styles.css
|   |       
|   \---templates
|       |   navigation.html
|       |   _base.html
|       |   
|       +---accounts
|       |       login.html
|       |       register.html
|       |       
|       +---core
|       |       index.html
|       |       
|       \---errors
|               401.html
|               404.html
|               500.html
|               
\---tests
        base_test.py
        test_forms.py
        test_models.py
        test_routes.py
        __init__.py
```

## Running the Flask App for the First Time

1. Clone the Repository using the following command:
``` bash
git clone https://github.com/aniru-dh21/Basic-Authentication-Flask.git
```

2. Install the Python Packages using the following command:
``` bash
pip install -r requirements.txt
```

3. Now that application is ready (without the tests), you can first migrate the database, and then run the app.

4. To initialize the database (create a migration repository), use the command:
``` bash
flask db init
```

5. To migrate the database changes, use the command:
``` bash
flask db migrate
```

6. To apply the migrations, use the command:
``` bash
flask db upgrade
```

7. Since this is the first time we're running our app, you'll need to run all the above commands. Later, whenever we make changes to the database, you'll just need to run the last two command.

8. After that, we can run application using the command:
``` bash
python manage.py run
```

## Testing the Flask App and Creating the Admin user
