# TSM_WebAPI:Web API service using C#

Overview[~]
The Task Management API is a web-based application developed using ASP.NET Core that enables users to manage their tasks. It offers API endpoints for performing CRUD operations: creating, retrieving, updating, and deleting tasks. The API supports filtering tasks by status, due date, and pagination. An in-memory database is used to store task data, and Swagger/OpenAPI is integrated for seamless testing and documentation.

Features[~]
Create, Read, Update, Delete (CRUD): Manage tasks with full CRUD functionality.
Filters: Filter tasks by status (Pending, In Progress, Completed) and due date.
Pagination: Support for paginated task listings.
Swagger Documentation: Provides interactive API documentation for easy exploration and testing.
In-Memory Database: Uses an in-memory database for task storage.

Techstack[~]
ASP.NET Core 8: Framework used for building the API.
Entity Framework Core: ORM for interacting with the in-memory database.
Swagger: For API documentation and testing.
NUnit: Unit testing framework for testing the API endpoints.
Playwright: Used for end-to-end testing of the web interface .

------------------------------------------------------------------------------------------------------------------------------------------

Setup & Installation[~]
To set up the project locally:

Clone the repository:
#git clone https://github.com/yourusername/TaskManagementAPI.git

Navigate to the project directory:
#cd TaskManagementAPI

Install dependencies:
#dotnet restore

Run the project:
#dotnet run

------------------------------------------------------------------------------------------------------------------------------------------

API Endpoints[~]

GET /tasks--
Description: Fetch a list of all tasks.
Query Parameters:
status: Filter tasks by status .
dueDate: Filter tasks by due date .
page: Page number for pagination .
pageSize: Number of items per page .

POST /tasks--
Description: Create a new task.
Request Body:
json
Copy code
{
  "title": "Task Title",
  "status": "Pending",
  "dueDate": "2024-12-31T00:00:00Z"
}

PUT /tasks/{id}--
Description: Update an existing task.
Request Body: Same as POST request body.
Parameters: id of the task to update.

DELETE /tasks/{id}--
Description: Delete a task.
Parameters: id of the task to delete.
