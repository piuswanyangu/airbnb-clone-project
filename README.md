# 🏠 Airbnb Clone Project (Backend)

##  Overview
This is the **backend** for my Airbnb Clone project — a platform that allows users to list, book, and review properties, just like Airbnb.  
I built it with a focus on scalability, clean architecture, and secure API design.

###  Goals
- Build a RESTful backend using **Django**.
- Design a relational database with **PostgreSQL**.
- Expose data efficiently through **GraphQL APIs**.
- Implement strong authentication and security measures.

---

##  Team Roles
Although I’m handling the backend, this project structure includes these roles:

- **Backend Developer (me):** Builds APIs, handles authentication, and manages business logic.  
- **Database Admin:** Designs and maintains data relationships.  
- **DevOps Engineer:** Manages CI/CD and deployments.  
- **QA Engineer:** Tests backend endpoints for bugs and performance.

---

##  Technology Stack
| Tech | Role |
|------|------|
| **Django** | Main backend framework |
| **PostgreSQL** | Database for structured data |
| **GraphQL** | API query language |
| **Docker** | For consistent deployments |
| **GitHub Actions** | CI/CD automation |

---

##  Database Design
**Key Entities**
- **Users:** id, username, email, password, role  
- **Properties:** id, title, location, price, owner_id  
- **Bookings:** id, user_id, property_id, start_date, end_date  
- **Reviews:** id, user_id, property_id, rating, comment  
- **Payments:** id, booking_id, amount, status, transaction_date  

**Relationships:**  
A user can own many properties, a booking links a user to a property, and each booking can have one payment and multiple reviews.

---

## ⚙️ Features
- **User Management:** Signup, login, and role control (host or guest).  
- **Property Management:** Create and manage property listings.  
- **Booking System:** Reserve available listings.  
- **Review System:** Add feedback after stays.  
- **Payment Handling:** Manage secure transactions.  

---

## API Security
I ill implement:
- **Token Authentication** for verified sessions.  
- **Role-Based Authorization** to protect endpoints.  
- **Rate Limiting & Data Validation** to prevent misuse.  
- **HTTPS** for secure data transfer.  

Security is key to protecting user data and maintaining trust.

---

##  CI/CD Pipeline
I use **GitHub Actions** for testing and deployment automation, and **Docker** for containerization.  
This ensures faster delivery, fewer bugs, and consistent production builds.

---

##  Setup
To run locally:
```bash
git clone https://github.com/piuswanyangu/airbnb-clone-project.git
cd airbnb-clone-project
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
