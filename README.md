# Project Title: REST CRUD API with Exception Handling (not finished)

This project is a RESTful CRUD (Create, Read, Update, Delete) API built with Java and Spring Boot. It uses Maven as a build tool. The main focus of this project is on handling exceptions and providing a robust REST API.

## Project Structure

The project is structured into different packages:

- `com.example.restcrud.entity`: Contains the `Student` entity class.
- `com.example.restcrud.exception`: Contains custom exception classes like `StudentNotFoundException`.
- `com.example.restcrud.rest`: Contains REST controller classes like `DemoRestController` and `StudentRestController`.

## Exception Handling

![image](https://github.com/baderbenlhachemi/restcrud/assets/88034249/91d682ee-ef93-4732-ab7e-01903568e6fd)

The application has an exception handler that catches and handles `StudentNotFoundException`. It returns a `StudentErrorResponse` with details about the error. The `StudentNotFoundException` is thrown when a student with a given ID does not exist in the system.

![image](https://github.com/baderbenlhachemi/restcrud/assets/88034249/185051cb-2a5e-43b4-b519-be797b51c743)

In addition to `StudentNotFoundException`, the application also has a catch-all exception handler that catches any other exceptions that might occur during the execution of the application. This ensures that all exceptions are properly handled and meaningful error messages are returned to the client.

## API Endpoints

- `GET /api/students`: Returns a list of all students.
- `GET /api/student/{studentId}`: Returns a student with the given ID. If the student does not exist, a `StudentNotFoundException` is thrown.

## Error Responses

When an exception is thrown, the application returns a `StudentErrorResponse` object. This object contains the following fields:

- `status`: The HTTP status code.
- `message`: A detailed error message.
- `timeStamp`: The time when the error occurred.

This ensures that the client receives a detailed and meaningful error message, which can be used to debug and fix the issue.
