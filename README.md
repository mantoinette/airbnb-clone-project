## Database Design

The database for this project is structured to support user interactions, property listings, bookings, reviews, and payments in a scalable and relational manner. The database is managed using **PostgreSQL**, with relationships handled through Django's ORM.

### 🧍 Users
Stores information about people using the platform (guests and hosts).

**Key Fields:**
- `id`: Unique identifier
- `name`: Full name of the user
- `email`: Unique email address
- `password`: Hashed password for authentication
- `role`: Defines if the user is a host or a guest

---

### 🏠 Properties
Represents listings posted by hosts.

**Key Fields:**
- `id`: Unique identifier
- `title`: Name of the property
- `description`: Detailed description
- `location`: Address or coordinates
- `price_per_night`: Cost per night
- `owner_id`: Foreign key to Users table (host)

---

### 📅 Bookings
Tracks reservations made by guests.

**Key Fields:**
- `id`: Unique identifier
- `property_id`: Foreign key to Properties table
- `user_id`: Foreign key to Users table (guest)
- `start_date`: Check-in date
- `end_date`: Check-out date
- `total_price`: Calculated price for the stay

---

### ⭐ Reviews
Allows guests to leave feedback on properties.

**Key Fields:**
- `id`: Unique identifier
- `user_id`: Foreign key to Users table (guest)
- `property_id`: Foreign key to Properties table
- `rating`: Numeric score (e.g., 1–5)
- `comment`: Textual feedback

---

### 💳 Payments
Handles transaction records for bookings.

**Key Fields:**
- `id`: Unique identifier
- `booking_id`: Foreign key to Bookings table
- `payment_method`: e.g., Credit Card, PayPal
- `payment_status`: e.g., Completed, Failed, Pending
- `payment_date`: Timestamp of the payment

---

### 🔗 Entity Relationships

- One **User** (host) can own many **Properties**
- One **User** (guest) can make many **Bookings**
- One **Property** can have many **Bookings**
- One **Property** can have many **Reviews**
- One **Booking** is associated with one **Payment**
- One **User** can write many **Reviews**

---

