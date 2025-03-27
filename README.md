# JWT Authentication System

## Overview

This project is a secure authentication system using JSON Web Tokens (JWT). It allows users to log in and access a protected dashboard only if they have a valid token.

## Features

- User authentication with JWT
- Secure login system
- Middleware-based token verification
- Protected dashboard route
- Express.js backend for API handling
- Custom error handling

## Tech Stack

- **Backend:** Node.js, Express.js
- **Authentication:** JWT (JSON Web Token)
- **Dependencies:**
  - dotenv (^8.2.0)
  - express (^4.17.1)
  - express-async-errors (^3.1.1)
  - http-status-codes (^2.1.4)
  - jsonwebtoken (^8.5.1)

## Project Structure

````
project-folder/
│── node_modules/            # Installed dependencies
│── src/
│   ├── middleware/
│   │   ├── auth.js                # JWT authentication middleware
│   │   ├── errorHandlerMiddleware.js # Handles application errors
│   │   ├── notFound.js             # Handles 404 errors
│   ├── errors/
│   │   ├── BadRequest.js          # Handles bad request errors
│   │   ├── CustomAPIError.js      # Base class for custom API errors
│   │   ├── UnauthenticatedError.js # Handles authentication errors
│   │   ├── index.js               # Centralized error exports
│   ├── routes/
│   │   ├── authRoutes.js          # Authentication routes
│   ├── controllers/
│   │   ├── authController.js      # Login and authentication logic
│   ├── app.js                     # Main application file
│── .env                            # Environment variables
│── .gitignore                      # Git ignore file
│── package.json                    # Project metadata and dependencies
│── package-lock.json               # Locked versions of dependencies
│── README.md                        # Documentation

````


## Installation

1. Clone the repository:
   ```bash
   git clone <https://github.com/bhanuudhay/SimpleJWT>
   cd <SimpleJWT>
2. Install dependencies:
   ```bash
   npm install
3. Create a .env file in the root directory and add the following environment variables:
   ```
   PORT=5000
   JWT_SECRET=your_secret_key
4. Start the server:
   ```bash
   npm start

# API Endpoints

- **POST / login** - Authenticates the user and returns a JWT token.

-  **GET / dashboard**   - Protected route, accessible only with a valid token.

# Usage

- Send a POST request to /login with valid credentials.

- Receive a JWT token upon successful login.

- Include the token in the Authorization header when accessing the /dashboard route.

 **Created By Bhanu Udhay Singh**

