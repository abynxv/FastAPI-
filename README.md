# CRUD-FastAPI

This project demonstrates a simple CRUD (Create, Read, Update, Delete) application using the FastAPI framework. It is designed to manage departments and employees within an organization. The project includes endpoints for creating, reading, updating, and deleting records in a SQLite database, leveraging SQLAlchemy for ORM (Object-Relational Mapping) and Pydantic for data validation.

# Setup Instructions

  -> Create a directory, open cmd in directory path  and clone CRUD-FastAPI project
  
      https://github.com/abynxv/CRUD-FastAPI.git

  -> Install Virtual environment
  
      pip install virtualenv

  -> Create virtual environment within the directory. 
  
      python -m venv venv_name  # On Windows
      python3 -m venv venv_name  # On macOS/Linux

  -> Activate virtual environmant    
  
      venv_name\Scripts\activate       # On Windows           
      source venv_name/bin/activate     # On macOS/Linux

  -> Install requirements.txt
  
      pip install -r requirements.txt

  -> Open Project in VScode
 
      code .

  -> Open terminal in vscode, navigate to project directory, Run the server and follow link

      cd fastapi_project
      uvicorn app.main:app --reload

# CRUD-FastAPI Project API Endpoints

Departments

1.Create a Department

    Endpoint    : POST /departments/
    Description : Create a new department.
    Request Body:
    {
      "name"                : "string",
      "number_of_employees" : 0
    }
    Response:
    {
      "id"                  : "integer",
      "name"                : "string",
      "number_of_employees" : "integer"
    }
2.Get a Department by ID

    Endpoint    : GET /departments/{department_id}
    Description : Retrieve a department by its ID.
    Response    :
    {
      "id"                  : "integer",
      "name"                : "string",
      "number_of_employees" : "integer"
    }

3.Get All Departments

    Endpoint    : GET /departments/
    Description : Retrieve a list of all departments.
    Parameters  :
                skip    : Integer, number of records to skip (default: 0)
                limit   : Integer, maximum number of records to return (default: 100)
    Response:
    [
    {
      "id"                 : "integer",
      "name"               : "string",
      "number_of_employees": "integer"
    }
    ]

4.Update a Department by ID

    Endpoint    : PUT /departments/{department_id}
    Description : Update an existing department by its ID.
    Request Body:
    {
      "name": "string",
      "number_of_employees": "integer"
    }
    Response    :
    {
      "id"                  : "integer",
      "name"                : "string",
      "number_of_employees" : "integer"
    }
5.Delete a Department by ID

    Endpoint    : DELETE /departments/{department_id}
    Description : Delete a department by its ID.
    Response    :
    {
      "id"                  : "integer",
      "name"                : "string",
      "number_of_employees" : "integer"
    }

Employees

1.Create an Employee

    Endpoint    : POST /employees/
    Description : Create a new employee.
    Request Body:
    {
      "name"          : "string",
      "department_id" : "integer"
    }
    Response:
    {
      "id"            : "integer",
      "name"          : "string",
      "department_id" : "integer"
    }

2.Get an Employee by ID

    Endpoint    : GET /employees/{employee_id}
    Description : Retrieve an employee by its ID.
    Response    :
    {
      "id"            : "integer",
      "name"          : "string",
      "department_id" : "integer"
    }

3.Get All Employees

    Endpoint    : GET /employees/
    Description : Retrieve a list of all employees.
    Parameters  :
                skip  : Integer, number of records to skip (default: 0)
                limit : Integer, maximum number of records to return (default: 100)
    Response````:
    [
    {
     "id": "integer",
     "name": "string",
     "department_id": "integer"
    }
    ]

4.Update an Employee by ID

    Endpoint    : PUT /employees/{employee_id}
    Description : Update an existing employee by its ID.
    Request Body:
    {
      "name"          : "string",
      "department_id" : "integer"
    }
    Response:
    {
      "id"            : "integer",
      "name"          : "string",
      "department_id" : "integer"
    }

Delete an Employee by ID

    Endpoint    : DELETE /employees/{employee_id}
    Description : Delete an employee by its ID.
    Response    :
    {
      "id": "integer",
      "name": "string",
      "department_id": "integer"
    }

