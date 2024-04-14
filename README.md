Setup Instructions
Clone the repository:

git clone <repository-url>
Install dependencies:

npm install
Start the server:

node app.js
Usage Instructions
API Endpoints
User Registration:

Endpoint: POST /register
Request Body:
{
  "username": "example_user",
  "password": "password123"
}
Response:
{
  "message": "User registered successfully",
  "token": "example_jwt_token"
}
User Login:

Endpoint: POST /login
Request Body:
{
  "username": "example_user",
  "password": "password123"
}
Response:
{
  "message": "Login successful",
  "token": "example_jwt_token"
}
Profile Management:

Endpoint: GET /profile
Headers: Authorization: Bearer example_jwt_token
Response:
{
  "userId": 1,
  "username": "example_user"
}
Diary Entry Creation:

Endpoint: POST /diary
Headers: Authorization: Bearer example_jwt_token
Request Body:
{
  "title": "Trip to Paris",
  "description": "Visited Eiffel Tower",
  "date": "2024-04-10",
  "location": "Paris, France",
  "photos": ["url1", "url2"]
}
Response:
{
  "message": "Diary entry created successfully",
  "entryId": 1
}
Diary Entry Retrieval:

Endpoint: GET /diary/:id
Headers: Authorization: Bearer example_jwt_token
Response:
{
  "id": 1,
  "title": "Trip to Paris",
  "description": "Visited Eiffel Tower",
  "date": "2024-04-10",
  "location": "Paris, France",
  "photos": ["url1", "url2"]
}
Diary Entry Update:

Endpoint: PUT /diary/:id
Headers: Authorization: Bearer example_jwt_token
Request Body:
{
  "title": "Updated Title",
  "description": "Updated description"
}
Response:
{
  "message": "Diary entry updated successfully"
}
Diary Entry Deletion:

Endpoint: DELETE /diary/:id
Headers: Authorization: Bearer example_jwt_token
Response:
{
  "message": "Diary entry deleted successfully"
}
Documentation:

Endpoint: GET /documentation
Response: Detailed documentation will be provided soon.
Application of OOP Concepts
Encapsulation:
Database interactions are encapsulated within class methods of User and DiaryEntry models, ensuring that data access is abstracted away and can be easily managed and modified.
Abstraction:
User and DiaryEntry classes abstract away the complexities of managing users and diary entries, providing clean and simple interfaces for interacting with the data.
Inheritance:
Although not explicitly demonstrated in this example, inheritance can be applied to extend functionality across different types of diary entries (e.g., TravelDiaryEntry, FoodDiaryEntry).
Polymorphism:
Polymorphic behavior can be achieved by defining methods in the parent class (e.g., CRUD operations) that can be overridden in subclasses to provide custom behavior.
Deployment and Submission
The API has been deployed to Google Cloud Platform. You can access the live API for testing and evaluation at [insert_link_here].