# UI Testing with Selenium Python & Pytest BDD - Page Object Model

## Overview
This project provides an example for testing a UI with Selenium WebDriver, written in Python, using the Page Object Model design pattern and driven via BDD feature files through Pytest BDD. 


## Web Application Under Test
The website that is being tested by this framework is “Repository Search”, that uses Repository APIs to make search when a given keyword is passed into the field

Following functionality has been tested, focusing on the following pages:
* [home/repository-list](http://localhost:3000/) page


### Tech stack
As this is a Python project, build and dependency management is handled by Pipenv, so there is a `Pipfile` (and associated `.lock` file) defining the versions of the dependencies:
* Python v3.8
* Selenium v4.1.5
* Pytest v7.1.2
* Pytest BDD v5.0.0
* Webdriver-Manager v3.5.4
* Pytest-html v3.1.1

Follow below steps to setup this project (Can be developed & run in PyCharm environment too)

* Install pipenv. Example: pip install pipenv
* Install Pipfile, install all the library dependencies and create environment. Example: pipenv install Pipfile
* Activate environment. Example: pipenv shell



### Supported Browsers
The `conftest.py` module uses the Webdriver-Manager dependency to manage the various browser drivers. The `browser` Pytest fixture returns the relevant WebDriver instance for the chosen browser, with support for:
* Chrome - the default option
* Firefox


### Running tests
* Run the web application locally by:  
  - npm install && npm start
* Run the entire suite by running the command: 
  - pytest
* To run a specific suite (e.g.repo_list_home_page, smoke etc) 
  - pytest -m repo_list_home_page 
  - pytest -m smoke
* To generate the report file for a run
  - pytest -m smoke --html=report.html (report_file_name.html)
* To override the default browser set in config.json
  - pytest -m regression --html=report.html --browser=Firefox



#### Test Reports
Test reports can be generated locally in the repository by passing the option --html=report.html to pytest utility. This file will be generated in the project root directory by default


