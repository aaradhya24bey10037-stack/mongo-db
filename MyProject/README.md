# Job Application Tracker API

A backend-only Job Application Tracker built using **Node.js, Express.js, and MongoDB**. The application allows users to manage, track, search, and analyze job and internship applications through REST APIs. All operations are performed using **Postman**, **Swagger UI**, and console outputs without any frontend interface.

---

## Project Overview

Managing multiple job applications manually can be difficult. This project provides a centralized backend system where users can store and monitor application details such as company name, job role, salary, location, and application status.

The project demonstrates MongoDB CRUD operations, Aggregation Pipelines, REST API development, Swagger documentation, and database seeding.

---

## Features

### Application Management

* Create a new job application
* View all applications
* View application by ID
* Update application details
* Delete applications

### Search & Filtering

* Search applications by company name
* Filter applications by application status

### Analytics Dashboard APIs

* Total applications count
* Status-wise application statistics
* Company-wise application statistics
* Average salary analytics
* Monthly application trends

### Additional Features

* MongoDB database integration
* Seed data generation
* Swagger API documentation
* Environment-based configuration
* RESTful architecture

---

## Tech Stack

| Technology | Purpose               |
| ---------- | --------------------- |
| Node.js    | Runtime Environment   |
| Express.js | Backend Framework     |
| MongoDB    | Database              |
| Mongoose   | ODM                   |
| Swagger UI | API Documentation     |
| Postman    | API Testing           |
| dotenv     | Environment Variables |
| Nodemon    | Development Server    |

---

## Project Structure

```text
job-application-tracker/
│
├── config/
│   └── db.js
│
├── controllers/
│   ├── applicationController.js
│   └── analyticsController.js
│
├── models/
│   └── Application.js
│
├── routes/
│   ├── applicationRoutes.js
│   └── analyticsRoutes.js
│
├── seed/
│   └── seed.js
│
├── swagger/
│   └── swagger.js
│
├── .env
├── app.js
├── server.js
├── package.json
└── README.md
```

---

## Database Schema

### Application

```json
{
  "companyName": "Google",
  "jobRole": "Software Engineer Intern",
  "location": "Bangalore",
  "salary": 45000,
  "status": "Applied",
  "applicationDate": "2026-06-20"
}
```

### Available Status Values

```text
Applied
Shortlisted
Interview Scheduled
Rejected
Selected
```

---

## Installation

### Clone Repository

```bash
git clone <repository-url>
cd job-application-tracker
```

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file:

```env
PORT=8000
MONGO_URI=mongodb://127.0.0.1:27017/jobApplicationTracker
```

### Start MongoDB

Ensure MongoDB is running locally.

### Start Development Server

```bash
npm run dev
```

### Start Production Server

```bash
npm start
```

---

## API Endpoints

### Application APIs

#### Create Application

```http
POST /api/applications
```

#### Get All Applications

```http
GET /api/applications
```

#### Get Application By ID

```http
GET /api/applications/:id
```

#### Update Application

```http
PUT /api/applications/:id
```

#### Delete Application

```http
DELETE /api/applications/:id
```

---

### Search APIs

#### Search By Company

```http
GET /api/applications/search?company=Google
```

#### Filter By Status

```http
GET /api/applications/status/Applied
```

---

### Analytics APIs

#### Total Applications

```http
GET /api/analytics/total
```

#### Status Statistics

```http
GET /api/analytics/status-stats
```

#### Company Statistics

```http
GET /api/analytics/company-stats
```

#### Average Salary

```http
GET /api/analytics/average-salary
```

#### Monthly Trends

```http
GET /api/analytics/monthly-trends
```

---

## Seed Database

Populate the database with sample records:

```bash
npm run seed
```

The script generates:

* 50 Sample Applications
* Multiple Companies
* Different Application Statuses
* Random Salary Data

---

## Swagger Documentation

After starting the server, access:

```text
http://localhost:8000/api-docs
```

Swagger UI provides interactive API documentation and endpoint testing.

---

## MongoDB Concepts Demonstrated

* CRUD Operations
* Schema Design
* Data Validation
* Indexing
* Aggregation Pipelines
* Filtering
* Searching
* Sorting
* Database Seeding

---

## Sample Workflow

1. Start MongoDB Server
2. Run Backend Application
3. Seed Sample Data
4. Test APIs using Postman
5. View API Documentation using Swagger
6. Perform CRUD Operations
7. Generate Analytics Reports

---

## Future Enhancements

* User Authentication (JWT)
* Role-Based Access Control
* Email Notifications
* Resume Upload Support
* Company Management Module
* Dashboard Frontend
* Export Reports to PDF/Excel
* Advanced Search and Filters

---

## Learning Outcomes

This project demonstrates practical backend development using Node.js and MongoDB, including REST API design, database modeling, aggregation queries, API documentation, and testing workflows commonly used in real-world software development.

---

## Author

Aradhya Sohani

B.Tech Computer Science Engineering with Specialization in E-Commerce
