## Technology Stack

This project utilizes a variety of modern technologies to build a scalable and efficient web application. Each technology plays a specific role in the system:

### 🐍 Django
A high-level Python web framework used to develop the backend of the application. Django provides a robust structure for building secure and maintainable RESTful APIs quickly and efficiently.

### 🐘 PostgreSQL
An advanced open-source relational database system used to store structured data such as user profiles, property listings, bookings, and reviews. It offers reliability, strong performance, and powerful querying capabilities.

### 🔍 GraphQL
A query language for APIs that allows the frontend to request exactly the data it needs. GraphQL helps improve performance and flexibility in communication between the frontend and backend.

### 🐙 Git & GitHub
Git is a version control system used to track code changes, while GitHub is the platform used for hosting the repository and collaborating as a team.

### 🐳 Docker
A containerization tool used to package the application and its dependencies, ensuring consistent environments across development, testing, and production.

### 🚀 Heroku / AWS
Cloud platforms used to deploy the application and make it accessible online. They provide hosting infrastructure, database integration, and scalability options.

### 🧪 Pytest / Postman
Used for testing the backend services. Pytest enables automated testing of Django components, and Postman is used for testing API endpoints manually.

## Database Design

The database for this project is designed using **PostgreSQL** to store and manage structured data efficiently. Below is an overview of the main entities and their relationships.

### 🧱 Entities and Their Purpose

- **User**
  - Stores user information such as name, email, password (hashed), and role.
  
- **Property**
  - Represents a listed apartment or house with details like title, location, description, price, and host (linked to a User).
  
- **Booking**
  - Tracks reservation details, including user who booked, property booked, dates, and total price.
  
- **Review**
  - Contains user-generated reviews and ratings for a property.

- **Image**
  - Stores image URLs or paths associated with a property.

### 🔗 Relationships

- One **User** can own multiple **Properties**
- One **User** can make multiple **Bookings**
- One **Booking** is linked to one **Property**
- One **Property** can have multiple **Reviews**
- One **Property** can have multiple **Images**

### 🗂️ Tools Used

- **PostgreSQL** – Relational database engine  
- **Django ORM** – To define models and handle database queries in Python  
- **ERD (Entity-Relationship Diagram)** – [Include an image or link if you have one]



