# Golang and MongoDB CRUD API

This is a simple API built using The Go Programming Language and using MongoDB for database. This project have basic CRUD operations for my learning purpose. 

## Project Structure

The project consists of the following main files and directories:

- `main.go`: The entry point of the application, which sets up the HTTP server and defines the routes for user CRUD operations.
- `models/user.go`: Defines the structure of the User model.
- `controllers/user.go`: Contains the controller logic for handling user CRUD operations.

## Getting Started

1. Clone the repository to your local machine:
    ```
    git clone https://github.com/alfauzan003/mongo-golang-crud.git
    ```

2. Install the required GoLang packages:
    ```
    go mod tidy
    ```

3. Start your MongoDB server.

4. Run the application:
    ```
    go run main.go
    ```


The server will start on port 9000.

## API Endpoints

- `GET /user`: Retrieve a list of all users.
- `GET /user/:id`: Retrieve a user by ID.
- `POST /user`: Create a new user.
- `DELETE /user/:id`: Delete a user by ID.

## Usage

You can use tools like [curl](https://curl.se/) or [Postman](https://www.postman.com/) to interact with the API endpoints.

Example:

- To create a new user:
    ```bash
    curl -X POST -H "Content-Type: application/json" -d '{"name": "John Doe", "gender": "Male", "age": 30}' http://localhost:9000/user
    ```

- To retrive an user by ID
    ```
    curl http://localhost:9000/user/<user-id>
    ```

- To retrieve a list of all users:
    ```
    curl http://localhost:9000/user
    ```

- To delete a user by ID:
    ```
    curl -X DELETE http://localhost:9000/user/<user-id>
    ```

## Database COnfiguration

The application connects to a MongoDB database using the following connection string:
`mongodb://localhost:27017`

You can change the connection string in the `main.go` file if your MongoDB server is running on a different host or port.