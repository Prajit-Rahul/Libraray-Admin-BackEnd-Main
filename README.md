# Library Admin Backend

Node.js and Express backend for a library administration platform with APIs for students, admins, books, bulk imports, and analytics.

This repository pairs with the dashboard frontend in [Library-Admin-FrontEnd-Main](https://github.com/Prajit-Rahul/Library-Admin-FrontEnd-Main).

## What It Covers

- Student CRUD and bulk registration
- Admin creation and retrieval
- Book CRUD and bulk import
- Department-level student aggregation
- Genre consolidation endpoints
- Monthly book activity analytics for dashboard charts

## Tech Stack

- Node.js
- Express
- Sequelize
- PostgreSQL
- dotenv
- bcrypt
- cookie-parser
- cors

## API Surface

### Students

- `POST /register/student`
- `POST /register/students`
- `POST /update/student`
- `GET /student/:id`
- `GET /students`
- `GET /students/departments`

### Admins

- `POST /register/admin`
- `POST /register/admins`
- `GET /admin`
- `GET /admin/:id`

### Books

- `GET /books`
- `GET /book/:id`
- `POST /book`
- `PUT /book/:id`
- `DELETE /book/:id`
- `POST /register/books`
- `GET /bookMonth`

### Analytics

- `GET /genre`

## Repository Structure

- `app.js`: application entry point and route wiring
- `src/controllers`: request handlers
- `src/service`: business logic and database operations
- `src/models`: Sequelize models and associations
- `src/config/db.js`: PostgreSQL connection setup

## Environment

Database configuration is loaded from environment variables:

- `databaseName`
- `User`
- `Pass`
- `DBConfigLink`

## Running Locally

```bash
npm install
npm start
```

The server is configured to run on port `4000` for local development.

## Why This Repo Matters

This backend shows practical API design for an internal operations product: CRUD services, bulk ingestion, analytics endpoints, and relational data modeling for a real administrative workflow.
