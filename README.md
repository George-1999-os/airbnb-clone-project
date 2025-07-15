## Database Design 

This section outlines the core database structure for the Airbnb Clone project.

### Users
- **id**: unique identifier (primary key)
- **name**: full name of the user
- **email**: unique email address
- **password_hash**: encrypted password
- **created_at**: timestamp when the user account was created

> One user can have multiple properties and make multiple bookings.


### Properties
- **id**: unique identifier (primary key)
- **owner_id**: foreign key to Users table
- **title**: name/title of the property
- **location**: property address
- **price_per_night**: cost per night

> A user can own many properties. Each property can have multiple bookings and reviews.


### Bookings
- **id**: unique identifier (primary key)
- **user_id**: foreign key to Users table
- **property_id**: foreign key to Properties table
- **start_date**: check-in date
- **end_date**: check-out date

> A booking belongs to a user and a property.


###  Reviews
- **id**: unique identifier (primary key)
- **user_id**: foreign key to Users table
- **property_id**: foreign key to Properties table
- **rating**: numerical score (e.g., 15)
- **comment**: written feedback

> A user can review multiple properties. Each property can have many reviews.


### Payments
- **id**: unique identifier (primary key)
- **booking_id**: foreign key to Bookings table
- **amount**: total amount paid
- **payment_method**: e.g., card, PayPal
- **status**: completed, pending, failed

> Each payment is tied to one booking.
