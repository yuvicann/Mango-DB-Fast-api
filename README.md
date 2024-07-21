# MongoDB-FastApi
Implemented CRUD operations with MongoDB and FastApi


Objective:
The objective of this assignment is to develop a complete application that performs CRUD
(Create, Read, Update, Delete) operations on a MongoDB database using Python. You will
implement wrapper functions for each CRUD operation and integrate these functions with the
FastAPI framework to expose these operations as RESTful APIs.
Requirements:
1. Set Up MongoDB Database:
○ Install and configure MongoDB.
○ Create a database and collection for the assignment.
2. Implement CRUD Wrapper Functions:
○ Create a Python module to connect to the MongoDB database.
○ Implement wrapper functions for Create, Read, Update, and Delete operations.
3. Develop RESTful APIs with FastAPI:
○ Install FastAPI and Uvicorn.
○ Create a FastAPI application that exposes the CRUD operations as RESTful
APIs.
○ Integrate the CRUD wrapper functions with the FastAPI endpoints.
4. Test the Application:
○ Test the CRUD operations through the FastAPI endpoints using a tool like
Postman or curl.

Steps to SetUp and Run the App:-

Step1:-  Install MongoDB and Mongo Compass as Gui for MongoDB for database usuage.
Step2:-  Create a School database containing table studens which has field as given below
        CREATE TABLE students (
            name VARCHAR(100) NOT NULL,
            age INT NOT NULL,
            grade VARCHAR(10) NOT NULL
        );

Step3:- Insert some data to check whether we are able to fetch it using query.
Step4:- Implement utility function for connecting to a database and executing the query.
Step5:- Implement CRUD function to create update read and delete student.
Step6:- Implement Endpoint for each operations having different usuage.
Step7:- To run the application in IDE go to the terminal containing the file and apply below command to the
        app will run as a localhost connected to DB.
        Command:- uvicorn main:app --reload
Step8:- Install Postman as a tool to run the endpoints and check whether we are able to implement CRUD operations and url and body
        for the request are as follows:-
        GET ALL API:- 
            URL:- http://localhost:8000/students/
        GET BY ID API:- 
            URL:- http://localhost:8000/students/6693a18b06b5651680b9dfed
        POST API:- 
            URL:- http://localhost:8000/students/
            BODY:- {
                        "name": "Name",
                        "age": 22,
                        "grade": "A"
                    }
        PUT API:-
            URL:- http://localhost:8000/students/6693a18b06b5651680b9dfed
            BODY:- {
                        "name": "Name 1 ",
                        "age": 22,
                        "grade": "B+"
                    }
        DELETE API:-
            URL:- http://localhost:8000/students/6693a18b06b5651680b9dfed
