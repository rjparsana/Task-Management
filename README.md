# Task Management API

## Overview
This is a role-based task management API built with Node.js, Express, and MongoDB. Admin users can manage all tasks and users, while regular users can only manage their own tasks.

## Features
- User Authentication (Registration, Login)
- Role-Based Access Control (Admin vs User)
- Task Creation, Update, Deletion, and Viewing
- JWT Authentication

## Technologies
- Node.js
- Express
- MongoDB (Mongoose)
- JWT for authentication
- Bcrypt for password hashing

## API Endpoints

### Authentication
- **POST /api/auth/register**: Register a new user.
- **POST /api/auth/login**: Log in and get a JWT token.

### Task Management
- **POST /api/tasks**: Create a new task (User).
- **GET /api/tasks/mytasks**: Get tasks of the logged-in user (User).
- **PUT /api/tasks/:id**: Update a task (User).
- **DELETE /api/tasks/:id**: Delete a task (User).
- **GET /api/tasks**: Get all tasks (Admin only).

## Authorization
Each request to the protected routes must include a valid JWT token in the `Authorization` header:

