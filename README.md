

## Python3 Virtual Environment For Windows 10

[Installing python on different OS](https://www.python.org/downloads/)

A Virtual Environment is a python environment, that is an isolated working copy of Python which allows you to work on a specific project without affecting other projects
So basically it is a tool that enables multiple side-by-side installations of Python, one for each project.


### Creating virtual environment

0. The Python installers for Windows include pip

    `py -m pip --version`

    pip is up-to-date by running:
    
    `py -m pip install --upgrade pip`


### Install virtual environment

1. Start virtual environment

    `virtualenvl <env_folder_name>`

    e.g.
    `virtualenvl portfolio_env`


2. Activate virtual environment

    `\pathto\env\Scripts\activate`

    Example:
    
    `C:\Users\'Username'\venv\Scripts\activate.bat`

3. PowerShell Execution.

    - *Note:* You must set the PowerShell Execution Policy from Restricted to RemoteSigned or Unrestricted to allow local PowerShell scripts to run:(if you use power shell).
    
    `set-executionpolicy remotesigned`

4. Deactivate virtual environment

    `deactivate`


5. For freeze your requirements which used:

    `pip freeze > requirements.txt`


6. For installing  the requirements freeze file:

    `pip install -r requirements.txt`

7. Install same packages of system in virtual environment:

    `virtualenv --system-site-packages <virtname>`


8. Python virtual environment more reference links.
    * Packaging Python: https://docs.nextcloud.com/server/stable/developer_manual/
    * Flask Palletsprojects: https://flask.palletsprojects.com/en/1.1.x/installation/
    * Liquidweb: https://www.liquidweb.com/kb/how-to-setup-a-python-virtual-environment-on-windows-10/

---
  
Debian and most other distributions include a python-pip package, if you want to use the Linux distribution-provided versions of pip see Installing pip/setuptools/wheel with Linux Package Managers.
