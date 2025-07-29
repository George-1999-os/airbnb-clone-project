# Airbnb Clone Project

## Overview
This is a simplified clone of the Airbnb platform, developed as part of the ALX Software Engineering program. It includes features like user authentication, property listing and booking, and admin functionalities.

### Project Goals
- Develop a functional web-based clone of Airbnb.
- Learn full-stack development using Django and PostgreSQL.
- Implement CI/CD, secure APIs, and database design best practices.

---

## Technology Stack

| Technology     | Purpose |
|----------------|---------|
| **Django**     | Backend web framework to manage the server-side logic. |
| **PostgreSQL** | Relational database for storing users, properties, bookings, etc. |
| **GraphQL**    | API query language for flexible client-server interactions. |
| **Docker**     | Containerization of the app for consistent deployment. |
| **GitHub Actions** | Automate testing and deployment in CI/CD pipeline. |

---

## Team Roles

| Team Member         | Role |
|---------------------|------|
| George Ibuchi       | Backend Developer |
| Jane Doe            | Frontend Developer |
| John Smith          | Database Administrator |
| Alice Johnson       | DevOps Engineer |
| Bob Williams        | Project Manager |

---

## Database Design

### Entities & Fields

1. **User**
   - user_id (PK)
   - name
   - email
   - password

2. **Property**
   - property_id (PK)
   - title
   - location
   - price_per_night
   - owner_id (FK to User)

3. **Booking**
   - booking_id (PK)
   - user_id (FK to User)
   - property_id (FK to Property)
   - check_in_date
   - check_out_date

4. **Review**
   - review_id (PK)
   - user_id (FK to User)
   - property_id (FK to Property)
   - rating
   - comment

5. **Payment**
   - payment_id (PK)
   - user_id (FK to User)
   - booking_id (FK to Booking)
   - amount
   - payment_date

### Relationships
- A user can book multiple properties.
- A property can have many bookings and reviews.
- A booking belongs to one user and one property.
- A payment is made by a user for a booking.

---

## Feature Breakdown

- User Registration and Login
- Property Listings with Filters
- Booking System with Date Selection
- Payment Simulation
- Review and Rating System
- Admin Dashboard for Managing Listings

---

## API Security

- **Authentication**: JWT tokens used for login and session management.
- **Authorization**: Role-based access (admin vs regular user).
- **Rate Limiting**: Prevent API abuse by throttling.
- **Data Validation**: Input validation to protect against SQL injection and XSS.

---

## CI/CD Pipeline

### What is CI/CD?
CI/CD stands for Continuous Integration and Continuous Deployment. It automates testing, building, and deploying of code, leading to faster development cycles and fewer bugs in production.

### Tools Used
- **GitHub Actions**: Automatically run tests and linting on each pull request.
- **Docker**: Ensures code runs consistently across different environments.
- **Heroku (or Render)**: For automatic deployment of the application (optional).

---

## Conclusion
This project showcases skills in full-stack development, database design, DevOps practices, and teamwork. It's a foundational step toward building scalable, secure web applications.
