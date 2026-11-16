# The Grand Library - Technology Stack

## 1. Introduction

This document describes the technologies, frameworks, and tools selected for The Grand Library.

The application will use a separate frontend and backend, with PostgreSQL as its database.

## 2. Frontend Technologies

| Technology | Purpose |
|---|---|
| Next.js | Frontend application framework |
| React | Building reusable user interface components |
| TypeScript | Adding static typing to JavaScript |
| Tailwind CSS | Styling and responsive layouts |

### Frontend Responsibilities

The frontend will handle:

- Displaying the website and user interfaces.
- Allowing visitors to browse and search for books.
- Providing registration and login screens.
- Displaying member dashboards.
- Managing reading lists and reading progress.
- Displaying book details, reviews, and ratings.
- Communicating with the backend REST API.

## 3. Backend Technologies

| Technology | Purpose |
|---|---|
| Java | Backend programming language |
| Spring Boot | Building the backend application |
| Spring Web | Creating REST API endpoints |
| Spring Data JPA | Database access and repository operations |
| Hibernate | Object-relational mapping |
| Spring Security | Authentication and authorization |
| Jakarta Bean Validation | Validating incoming data |

### Backend Responsibilities

The backend will handle:

- Business logic and application rules.
- User authentication and authorization.
- Book and author management.
- Borrowing and reservation operations.
- Reading progress and reviews.
- Community features.
- Database communication.
- Data validation and error handling.

## 4. Database

**Technology:** PostgreSQL

PostgreSQL will store the application's information, including:

- User accounts and roles.
- Books, authors, and categories.
- Physical book copies and digital editions.
- Borrowing and reservation records.
- Reading lists and progress.
- Reviews and ratings.
- Book clubs and challenges.
- Notifications.

The backend will communicate with PostgreSQL through Spring Data JPA and Hibernate.

## 5. External Integration

**Service:** Open Library API

The Open Library API will provide external book information, such as:

- Book titles.
- Authors.
- ISBN information.
- Publication details.
- Book cover information.

Administrators will also be able to add and manage book information directly through the platform.

## 6. Development and Testing Tools

| Tool | Purpose |
|---|---|
| Visual Studio Code | Frontend development and project management |
| NetBeans | Java development |
| PostgreSQL | Database management |
| pgAdmin | Graphical database administration |
| Postman | REST API testing |
| Git | Version control |
| GitHub | Remote repository and project hosting |

## 7. Application Architecture

The Grand Library will follow a modular monolithic architecture.

The frontend and backend will be separate applications.

The frontend will send HTTP requests to the backend REST API. The backend will process requests, apply business rules, communicate with the database, and return responses.

### High-Level Architecture

```text
             USER
               |
               v
       NEXT.JS FRONTEND
       React + TypeScript
               |
               | HTTP / REST API
               v
       SPRING BOOT BACKEND
               |
       ---------------------
       |         |         |
     Auth      Books   Borrowing
       |         |         |
       ---------------------
               |
               v
          POSTGRESQL
               |
               v
          DATABASE