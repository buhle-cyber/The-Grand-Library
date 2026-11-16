# The Grand Library - System Requirements

## 1. Introduction

This document defines the functional and non-functional requirements of the The Grand Library.

## 2. Functional Requirements

Functional requirements describe what the system must do.

### 2.1 User Authentication and Accounts

- FR-001: The system must allow users to register for an account.
- FR-002: The system must allow registered users to log in and log out.
- FR-003: The system must support different user roles, including Member and Administrator.
- FR-004: Users must be able to manage their profile information.
- FR-005: The system must restrict protected features based on user permissions.

### 2.2 Book Catalogue

- FR-006: Visotrs must be able to browse the book catalogue.
- FR-007: Users must be able to search for books by title, author, ISBN, and keywords.
- FR-008: Users must be able to filter books by category, language, publication year, rating, and availability.
- FR-009: Users must be able to sort search results.
- FR-010: Users must be able to view detailed book information.
- FR-011: Administrators must be able to add, update, and archive catalogue entries.
- FR-012: The system must support importing book information from the Open Library API.

### 2.3 Book Management

- FR-013: The system must support multiple physical copies of the same book. 
- FR-014: Administrators must be able to manage physical book copies. 
- FR-015: The system must support digital editions of books.
- FR-016: Administrators must be able to manage digital editions and their access permissions. 

### 2.4 Borrowing and Reservations

- FR-017: Members must be able to request physical books for borrowing.
- FR-018: Administrators must be able to approve borrowing requests and assign available copies.
- FR-019: The system must record borrowing dates and due dates.
- FR-020: Administrators must be able to reserve books that are unavailable.
- FR-021: Members must be able to rserve books that are unavailable.
- FR-022: The system must manage reservation queues.
- FR-023: The system must support digital borrowing with access expiry rules. 

### 2.5 Reading Activities

- FR-024: Members must be able to save books to their personal lists.
- FR-025: Members must be able to create and manage reading lists.
- FR-026: Members must be able to track their reading progress.
- FR-027: Members must be able to read eligible digital books.
- FR-028: Members must be able to rate and review books.
- FR-029: Members must be able to edit their existing reviews.

### 2.6 Community Features

- FR-030: Members must be able to join book clubs.
- FR-031: Members must be able to participate in reading challenges.
- FR-032: The system must support public book club events.
- FR-033: The system must support badges and reading achievements.

### 2.7 Notifications

- FR-034: The system must provide in-app notifications.
- FR-035: Members must receives notifications about borrowing requests, due dates, reservations, and relevant activities.

### 2.8 Administration

- FR-036: Administrators must have access to an administration dashboard.
- FR-037: Administrators must be able to manage members. 
- FR-038: Administrators must be able to manage borrowing and reservation records.
- FR-039: Administrators must be able to manage book clubs, challenges, and events.
- FR-040: Administrators must be able to view library statistics. 

## 3. Non-Functional Requirements

Non-functional requirements describe how well the system must operate.

### 3.1 Security

- NFR-001: Passwords must be securely hashed and never stored as plain text. 
- NFR-002: Protected API endpoints must require authentication.
- NFR-003: Users must only access information and actions permitted by their roles.
- NFR-004: Digital book files must only be accessible to users with the required permissions.

### 3.2 Performance
- NFR-005: The system should return normal catalogue search results within a reasonabe response time.
- NFR-006: The system should support pagination for large catalogue results. 
- NFR-007: Database queries should be designed to avoid unecessary processing. 

### 3.3 Usability

- NFR-008: The interface must be responsive across desktop, tablet, and mobile devices.
- NFR-009: Navigation must be clear and consistent.
- NFR-010: The system must provide understandable validation and error messages. 

### 3.4 Reliablity and Data Integrity

- NFR-011: The system must validate data before saving it.
- NFR-012: The system must prevent invalid borrowing and reservation operations. 
- NFR-013: Important database operations must maintain data consistency.
-NFR-014: The system should handle unexpected errors without exposing sensitive information. 

### 3.5 Maintainability

- NFR-015: The backend must follow a modular architecture.
- NFR-016: The codebase must use consistent naming and coding conventions.
- NFR-017: Important functionality must have automated tests.
- NFR-018: Project documentation must be maintained as the system develops.

### 3.6 Compatibility

- NFR-019: The application must support modern web browsers.
- NFR-020: The frontend and backend must communicate through documented REST API endpoints.

## 4. User Roles

| Role | Description |
|---|---|
| Visitor | Can browse publicly available library information. |
| Member | Can access personal reading and borrowing features. |
| Administrator | Can manage library operations and system content. |

## 5. Requirements Priority

Development will follow these priorities:

- **High:** Essential features required for the initial working platform.
- **Medium:** Important features added after the core platform is working.
- **Low:** Additional enhancements that can be introduced later.

