# Backend Guide

## Introduction

Welcome to the backend of the MERN Book Store App. This application serves as the server-side component of a book store, handling API requests, managing database operations, and serving as the backbone for the frontend application. 

## Techstack

The backend of this application utilizes the following technologies:<br>
<center><img src="https://go-skill-icons.vercel.app/api/icons?i=javascript,typescript,nodejs,express,mongodb,mongoose" /></center><br>

- **Node.js**: A JavaScript runtime built on Chrome's V8 JavaScript engine.<br>
- **Express**: A minimal and flexible Node.js web application framework.
- **MongoDB**: A NoSQL database for storing book and user data.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js.
- **JWT (JSON Web Token)**: A standard for creating access tokens for secure user authentication.
- **Dotenv**: A zero-dependency module that loads environment variables from a `.env` file into `process.env`.

## Code Workflow

The backend code is structured as follows:

1. **Entry Point**: `index.js` is the main entry point of the application. It sets up the Express server, connects to the MongoDB database, and defines the API routes.

2. **Configuration**: `config.js` holds the configuration settings such as database connection strings.

3. **Models**: The `models` directory contains Mongoose schemas and models, which define the structure of the data stored in MongoDB.

4. **Routes**: The `routes` directory includes all the route definitions and handlers for different API endpoints.

5. **Dependencies**: `package.json` and `package-lock.json` manage the project's dependencies.

## Setup

To set up and run the backend of the MERN Book Store App, follow these steps:

1. **Clone the Repository**: Clone the repository to your local machine.

   ```bash
   git clone <repository-url>
   cd backend
   ```

2. **Install Dependencies**: Install the required dependencies using npm.

   ```bash
   npm install
   ```

3. **Configure Environment Variables**: Create a `.env` file in the root directory and add the necessary environment variables. Refer to `config.js` for the required variables.

   ```env
   MONGO_URI=your_mongodb_connection_string
   PORT=your_preferred_port
   JWT_SECRET=your_jwt_secret
   ```

4. **Run the Server**: Start the Express server.

   ```bash
   npm start
   ```

   The server should now be running on the specified port.

## Errors and Solutions

Here are some common errors you might encounter during setup and their solutions:

| Error                       | Reason                                           | Solution                                                                                                                                                       |
|-----------------------------|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MongoDB Connection Error**| Failed to connect to MongoDB                     | Check your MongoDB server status and verify the `MONGO_URI` in the `.env` file.                                                                                |
| **Port Already in Use**     | Specified port is already in use                 | Change the `PORT` value in the `.env` file to a different port number.                                                                                         |
| **Missing Dependencies**    | Required modules are not installed               | Run `npm install` to install all required dependencies.                                                                                                        |
| **JWT Secret Not Set**      | Missing JWT_SECRET in environment variables      | Ensure that the `.env` file contains a `JWT_SECRET` variable.                                                                                                  |
| **CORS Policy Error**       | Cross-origin requests are blocked                | Install and configure the `cors` middleware in your Express app. Add `const cors = require('cors'); app.use(cors());` to your `index.js` file.                 |
| **SyntaxError: Unexpected token** | JSON parsing error                            | Verify that the request payloads sent to the server are properly formatted JSON.                                                                               |
| **ValidationError**         | Mongoose schema validation failed                | Check the data being sent to the server and ensure it adheres to the schema defined in the Mongoose models.                                                    |
| **Cannot find module 'xyz'**| Missing module or incorrect import path          | Verify the module is installed and the import path is correct. If the module is not installed, run `npm install <module_name>`.                                 |
| **UnhandledPromiseRejectionWarning** | Uncaught promise rejection                      | Ensure that all promises are properly handled using `.then()` and `.catch()` or async/await with try/catch blocks.                                             |
| **DeprecationWarning**      | Use of deprecated Node.js features               | Update the code to use the recommended API. Refer to the official documentation for the latest practices and update the dependencies.                           |

