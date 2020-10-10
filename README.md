

## Virtual environment for Flask using python3

[Installing python on Windows OS](https://www.python.org/downloads/)

A Virtual Environment is a python environment, that is an isolated working copy of Python which allows you to work on a specific project without affecting other projects
So basically it is a tool that enables multiple side-by-side installations of Python, one for each project.


### Step1: Install virtual environment

1. The Python installers for Windows include pip

    `py -m pip --version`

    pip is up-to-date by running:
    
    `py -m pip install --upgrade pip`
    
2. On Windows, virtualenv is provided by your package manager

    `pip install virtualenv`
    
### Step 2: Create an environment

1. Create a project folder and a venv folder within:

    `mkdir <Folder Name>`

2. Start virtual environment

    `virtualenvl <env_folder_name>`

    e.g.
    `virtualenvl portfolio_env`


3. Activate virtual environment

    `\pathto\env\Scripts\activate`

    Example:
    
    `C:\Users\'Username'\venv\Scripts\activate.bat`

4. PowerShell Execution.

    - *Note:* You must set the PowerShell Execution Policy from Restricted to RemoteSigned or Unrestricted to allow local PowerShell scripts to run:(if you use power shell).
    
    `set-executionpolicy remotesigned`

5. Deactivate virtual environment

    `deactivate`


6. For freeze your requirements which used:

    `pip freeze > requirements.txt`


7. For installing  the requirements freeze file:

    `pip install -r requirements.txt`

8. Install same packages of system in virtual environment:

    `virtualenv --system-site-packages <virtname>`

### Step 3: Install Flask
 Within the activated environment, use the following command to install Flask:

    pip install Flask

### Step 4: Create a applcation
Build the most simplest hello world application.

#### Follow these steps:

1. As, you are already present in the myproject folder. Create a file `hello.py' and write the below code.
    * Import the Flask class. An instance of this class will be our WSGI application.
    
        `from flask import Flask`
    
    * Next we create an instance of this class. The first argument is the name of the application’s module or package. If you are using a single module (as in this example), you should use __ name __ because depending on if it’s started as application or imported as module the name will be different ('main' versus the actual import name). This is needed so that Flask knows where to look for templates, static files, and so on.
    
        `app = Flask(__ name __)`
    
    * We then use the route() decorator to tell Flask what URL should trigger our function.The function is given a name which is also used to generate URLs for that particular function, and returns the message we want to display in the user’s browser.
    
        ```
        @app.route("/")
        def hello():
            return "Hello, World!"
        ```
    
    Make sure to not call your application flask.py because this would conflict with Flask itself.
    
    
    To run the application you can either use the flask command or python’s -m switch with Flask. Before you can do that you need to tell your terminal the application to work with by exporting the FLASK_APP environment variable:
    
        
        from flask import Flask

        app = Flask(__name__)

        @app.route("/")
        def hello():
            return "Hello, World!"
        

2. Start the server

        Python <File Name>.py
    
### Step 3: Reference links

0. Python virtual environment & simplest flask hello world application more reference links.
    * Packaging Python: https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/
    * Flask Palletsprojects: https://flask.palletsprojects.com/en/1.1.x/installation/
    * Liquidweb: https://www.liquidweb.com/kb/how-to-setup-a-python-virtual-environment-on-windows-10/
    * Timmyreilly: https://timmyreilly.azurewebsites.net/python-flask-windows-development-environment-setup/
    * Flask Palletsprojects: https://flask.palletsprojects.com/en/1.0.x/
    * Flask Palletsprojects: https://flask.palletsprojects.com/en/1.0.x/quickstart/


---
  
Debian and most other distributions include a python-pip package, if you want to use the Linux distribution-provided versions of pip see Installing pip/setuptools/wheel with Linux Package Managers.
