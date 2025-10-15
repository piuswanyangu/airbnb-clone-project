# 🏠 Airbnb Clone Project (Backend)

## 📘 Overview
This is the **backend** of my Airbnb Clone project — a platform that allows users to list, book, and review properties just like Airbnb.  
I designed it with a focus on scalability, security, and clean architecture using **Django**, **PostgreSQL**, and **GraphQL**.

### 🎯 Goals
- Build a robust backend system using Django.
- Design a relational database with PostgreSQL.
- Expose efficient APIs with GraphQL.
- Implement authentication, authorization, and CI/CD pipelines.

---

## 👨‍💻 My Role
I’m responsible for developing the **backend**, which includes:
- Building APIs and managing authentication.
- Designing database schemas and relationships.
- Implementing API security measures.
- Setting up Docker and CI/CD for automation and deployment.

---

## 💻 Technology Stack
| Technology | Description |
|-------------|-------------|
| **Django** | Backend web framework for building APIs. |
| **PostgreSQL** | Relational database for structured data. |
| **GraphQL** | Query language for optimized data fetching. |
| **Docker** | Containerization for consistent environments. |
| **GitHub Actions** | CI/CD automation for testing and deployment. |

---

## 🗃️ Database Design
### **Main Entities**
- **Users:** id, username, email, password, role (guest or host)  
- **Properties:** id, title, description, location, price_per_night, owner_id  
- **Bookings:** id, property_id, user_id, start_date, end_date, total_price  
- **Reviews:** id, user_id, property_id, rating, comment  
- **Payments:** id, booking_id, amount, status, transaction_date  

**Relationships:**
- A user can own multiple properties.  
- A booking links a user to a property.  
- A booking has one payment.  
- A property can have many reviews.

---

## ⚙️ Core Features
- **User Authentication:** Signup, login, and role-based access.  
- **Property Management:** Hosts can create and manage listings.  
- **Booking System:** Guests can book and manage reservations.  
- **Reviews:** Users can rate and review properties.  
- **Payment Handling:** Secure transaction management.  
- **GraphQL API:** Simplifies data access for frontend integration.

---

## 🔒 API Security
I’ve added multiple layers of security to protect both data and users:

- **Token-based Authentication (JWT):** Ensures only logged-in users access protected routes.  
- **Role-based Authorization:** Hosts and guests have different permissions.  
- **Input Validation & Sanitization:** Prevents SQL injection and XSS attacks.  
- **Rate Limiting:** Controls API traffic and prevents DDoS attacks.  
- **HTTPS Enforcement:** Encrypts all data in transit.

Security is a top priority — it protects user data, payments, and platform integrity.

---

## 🚀 CI/CD Pipeline
I use **GitHub Actions** and **Docker** to automate testing, building, and deployment.  
This helps me deliver faster updates and maintain consistency across environments.

**Tools Used:**
- **GitHub Actions:** For automated testing and deployment.  
- **Docker:** For containerized builds.  
- **Render / AWS / Heroku:** For hosting and scaling the backend.

**Benefits:**
- Faster releases.  
- Early detection of bugs.  
- Reliable, repeatable deployments.

---

## 🗂️ Folder Structure
Here’s how I’ve organized my backend project for better scalability and readability:

airbnb-clone-project/
│
├── manage.py # Django entry point
├── requirements.txt # Project dependencies
├── Dockerfile # Docker configuration
├── .github/
│ └── workflows/
│ └── ci.yml # GitHub Actions pipeline
│
├── airbnb_backend/ # Main Django app configuration
│ ├── init.py
│ ├── settings.py # Project settings (database, installed apps, etc.)
│ ├── urls.py # API routes
│ ├── asgi.py
│ └── wsgi.py
│
├── users/ # User management app
│ ├── models.py # User model
│ ├── views.py # User views (register/login)
│ ├── serializers.py # Data serialization
│ ├── urls.py
│ └── tests.py
│
├── properties/ # Property app
│ ├── models.py
│ ├── views.py
│ ├── urls.py
│ └── serializers.py
│
├── bookings/ # Booking app
│ ├── models.py
│ ├── views.py
│ ├── urls.py
│ └── serializers.py
│
├── reviews/ # Reviews app
│ ├── models.py
│ ├── views.py
│ └── serializers.py
│
└── payments/ # Payments app
├── models.py
├── views.py
└── serializers.py
