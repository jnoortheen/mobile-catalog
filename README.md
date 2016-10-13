Mobile Catalogue
================
Single page web app to store and retrieve Mobile Information with Google OAuth2 User Authentication.

Technologies
------------
1.  Python
2.  Flask
5.  AngularJS
6.  Bootstrap3
3.  SQLAlchemy

How To Run
----------
1. Clone this repository
2. Install the required modules using the following command
    ```````````````````````````````
    pip install -r requirements.txt
    ```````````````````````````````
3. change working directory to be the folder that contains app.py
4. run this to use flask cli commands
    ```````````````````````
    export FLASK_APP=app.py
    ```````````````````````
5. Initialise database and its tables using
    `````````````
    flask initdb
    `````````````
6. start the application server by
    `````````````
    python app.py
    `````````````

JSON API Endpoints
------------------
1.  To get all categories and their items
    ```````````````````````````````
    http://localhost:5000/?json=all
    ```````````````````````````````
2.  To get only items under a category
    `````````````````````````````````````````````````````````````
    http://localhost:5000/?json=category&category={category_name}
    `````````````````````````````````````````````````````````````

Features:
--------
1.  Using OAuth2 based user syste to manage site contents
2.  Secured cookie usage
3.  Single Page app using AngualrJS

Notes while deploying:
----------------------
-   Any database engine can be used for the apllication backend if they are supported by SQLAlchemy and the respective db engine driver is installed. 
-   Update the SQLALCHEMY_DATABASE_URI variable in the app.py to use correct connection URI to the database.
-   Update the authorised URI section in the Google Credentials and then update the client_secrets.json file.