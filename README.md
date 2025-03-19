# Practicode3

## Overview
This project consists of two main components:
1. **TodoApi** - A .NET Core Web API for managing a to-do list.
2. **Client** - A front-end client built with JavaScript (React).

## Project Structure
```
Practicode3.sln
client/
    package.json
    build/
    public/
    src/
TodoApi/
    appsettings.Development.json
    appsettings.json
    Dockerfile
    Item.cs
    Program.cs
    TodoApi.csproj
    ToDoDbContext.cs
    Properties/
```

## Prerequisites
- [.NET SDK 8.0](https://dotnet.microsoft.com/download)
- [Node.js](https://nodejs.org/) (for the client)
- Docker (optional, for containerization)

## How to Run

### Backend (TodoApi)
1. Navigate to the `TodoApi` directory:
   ```sh
   cd TodoApi
   ```
2. Run the application:
   ```sh
   dotnet run
   ```
3. The API will be available at `http://localhost:5073`.

### Frontend (Client)
1. Navigate to the `client` directory:
   ```sh
   cd client
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the development server:
   ```sh
   npm start
   ```
4. The client will be available at `http://localhost:3000`.

## Docker Support
To run the project using Docker:
1. Build the Docker image:
   ```sh
   docker build -t todoapi .
   ```
2. Run the container:
   ```sh
   docker run -p 5073:5073 todoapi
   ```

## Technologies Used
- **Backend**: .NET Core 8.0, Entity Framework Core
- **Frontend**: React.js
- **Database**: SQLite (or other, based on configuration)
- **Containerization**: Docker

## License
This project is licensed under the MIT License.

## Author
Developed by chana ben yosef.