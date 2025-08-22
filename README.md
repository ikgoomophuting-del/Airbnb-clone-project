Project Overview  
This project is an **Airbnb Clone** that I am building as part of my learning journey in software engineering. The goal is to recreate the core features of Airbnb, such as user authentication, property listings, bookings, reviews, and payments.  

By working on this project, I aim to strengthen my full-stack development skills and gain hands-on experience with real-world tools and workflows. It’s not just about coding, but also about learning how to design databases, build secure APIs, and understand the complete process of software development — from writing code to deploying an application.  

This project is also helping me get comfortable with teamwork concepts, GitHub collaboration, and industry best practices that are essential for professional software engineers. 

Team Roles  

For this Airbnb Clone project, different roles are important to ensure the application is well-structured, secure, and user-friendly. Each role has a unique responsibility, and together they form the backbone of a successful software project.  

1. Backend Developer  
Responsible for building the **logic and functionality** of the app. This includes designing APIs, handling data requests, managing user authentication, and making sure the system runs smoothly behind the scenes.  

2. Frontend Developer  
Focuses on the **user interface (UI)** and user experience. They ensure that the design is responsive, clean, and intuitive so users can easily browse properties, make bookings, and interact with the platform.  

3. Database Administrator (DBA)  
Takes care of the **database design, management, and performance**. They make sure that data (users, bookings, payments, etc.) is stored securely, relationships are well-defined, and queries run efficiently.  

4. DevOps Engineer  
Manages the **CI/CD pipeline, deployment, and server infrastructure**. Their role is to automate builds, testing, and deployments using tools like GitHub Actions and Docker, ensuring the app is reliable and scalable.  

5. QA Engineer (Tester)  
Ensures the app is **bug-free and stable** by writing test cases, running tests, and verifying features. They focus on quality control so users have a smooth experience.  

6. Project Manager  
Coordinates the project, making sure deadlines are met and that team members collaborate effectively. They track progress, communicate goals, and keep the project aligned with its objectives.  

Technology Stack  

The Airbnb Clone project uses a modern full-stack development ecosystem. Each tool and framework plays a specific role in ensuring the platform is scalable, secure, and user-friendly.  

1. Django  
A powerful **Python web framework** used to build the backend of the project. Django helps in creating RESTful APIs, managing authentication, and handling business logic efficiently.  

2. PostgreSQL  
A **relational database system** used to store structured data such as users, properties, bookings, reviews, and payments. PostgreSQL ensures data consistency, relationships, and secure storage.  

3. GraphQL  
An **API query language** that allows flexible communication between the frontend and backend. It helps clients fetch only the data they need, improving performance and reducing unnecessary data transfers.  

4. Docker  
A tool used for **containerization**, ensuring the application runs the same way in different environments (development, testing, and production). Docker makes deployment simpler and more reliable.  

5. GitHub Actions  
A **CI/CD pipeline tool** used for automating testing and deployment. It ensures new code is properly tested before merging and that deployments are smooth.  

6. HTML, CSS & JavaScript  
These are the **core frontend technologies**. They help design the user interface (UI), making the app interactive, responsive, and user-friendly.  

7. REST APIs  
Used alongside GraphQL, REST provides **standardized endpoints** for communication between different parts of the application.  


Database Design  

The database for the Airbnb Clone is designed to capture key entities and their relationships, ensuring smooth data flow and accurate representation of the booking process.  

Key Entities and Fields  

1. Users  
- **id** (Primary Key)  
- **name**  
- **email** (unique)  
- **password_hash**  
- **role** (guest or host)  

A user can be both a host (listing properties) and a guest (booking properties).  

2. Properties  
- **id** (Primary Key)  
- **user_id** (Foreign Key → Users)  
- **title**  
- **description**  
- **location**  
- **price_per_night**  

A property belongs to one host (user), but a host can have multiple properties.  

3. Bookings  
- **id** (Primary Key)  
- **user_id** (Foreign Key → Users)  
- **property_id** (Foreign Key → Properties)  
- **start_date**  
- **end_date**  
- **status** (pending, confirmed, cancelled)  

A booking links a guest (user) to a property. One property can have many bookings, but each booking belongs to one user and one property.  

4. Reviews  
- **id** (Primary Key)  
- **user_id** (Foreign Key → Users)  
- **property_id** (Foreign Key → Properties)  
- **rating** (1–5)  
- **comment**  

A review belongs to a guest (user) for a property. One property can have multiple reviews, and one user can write multiple reviews.  

5. Payments  
- **id** (Primary Key)  
- **booking_id** (Foreign Key → Bookings)  
- **amount**  
- **payment_method** (card, PayPal, etc.)  
- **status** (successful, failed, pending)  

Each payment is linked to a booking. One booking can have one or more payment attempts.

This structure ensures all critical aspects of the platform—users, listings, bookings, reviews, and payments—are properly connected for smooth application functional


 Feature Breakdown  

The Airbnb Clone project includes several core features that replicate the essential functionality of a real-world booking platform. Each feature is designed to ensure a seamless experience for both hosts and guests while maintaining scalability and security.  

1. User Management  
This feature allows users to sign up, log in, and manage their profiles securely. It supports two main roles: **guests** (who book properties) and **hosts** (who list properties). Authentication and authorization are implemented to protect user accounts and data.  

2. Property Management  
Hosts can create, update, and manage property listings with details such as title, description, location, and price per night. This feature ensures properties are accurately represented and easily searchable by guests.  

3. Booking System  
Guests can browse available properties and make bookings by selecting dates and confirming reservations. The system tracks booking status (pending, confirmed, or cancelled) to ensure proper coordination between hosts and guests.  

4. Review System  
After a stay, guests can leave ratings and comments for properties they booked. Reviews help maintain transparency, build trust, and guide future guests in making informed decisions.  

5. Payment Processing  
Payments are linked to bookings and allow users to complete transactions securely using different payment methods (e.g., credit card, PayPal). This ensures smooth financial operations while maintaining trust through secure payment handling.  

6. API Security  
Core backend APIs are protected with authentication, authorization, and rate-limiting. This prevents unauthorized access, protects sensitive user data, and ensures the reliability of the platform.  

7. CI/CD Pipeline Integration  
Automated workflows using tools like **GitHub Actions** and **Docker** streamline testing, building, and deployment. This reduces human error and ensures new features are delivered efficiently and reliably.  
