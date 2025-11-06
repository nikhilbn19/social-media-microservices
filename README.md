#  Microservices-Based Social Media Platform

A scalable **social media platform** built with **Node.js**, **Express.js**, **MongoDB**, **Redis**, and **RabbitMQ**, designed with a **microservices architecture** for modularity, scalability, and fault tolerance.

---

##  Overview

This project demonstrates a distributed microservices-based architecture for a social media platform.
It includes independent services for **Identity**, **Post**, **Media**, and **Search**, all connected via REST APIs and routed through an **API Gateway** acting as a reverse proxy.

---

##  Architecture

**Services:**

* **API Gateway:** Routes requests to the respective microservices and handles authentication.
* **Identity Service:** Handles user registration, login, and authentication.
* **Post Service:** Manages user posts and interactions.
* **Media Service:** Uploads and manages media files linked to posts.
* **Search Service:** Enables efficient search for posts and users.

**Inter-Service Communication:**

* REST APIs for synchronous communication
* **RabbitMQ** for asynchronous message queuing
* **Redis** for caching and rate limiting

---

##  Security & Performance

* **JWT Authentication** for secure user sessions
* **Argon2** for password hashing
* **Helmet**, **CORS**, and **express-rate-limit** for API security
* **Redis** caching for faster read operations and API rate control
* **Winston** for structured backend logging

---

##  Database

* **MongoDB** with **Mongoose ORM** for schema validation and database interaction
* Collections include:

  * `users`
  * `posts`
  * `media`
  * `searchIndex`

---

##  Media Storage

* Integrated **Cloudinary** for scalable media storage and optimized delivery.

---

##  Tech Stack

| Layer                      | Technology                       |
| -------------------------- | -------------------------------- |
| **Backend**                | Node.js, Express.js              |
| **Database**               | MongoDB, Redis                   |
| **Authentication**         | JWT, Argon2                      |
| **Asynchronous Messaging** | RabbitMQ                         |
| **Media Handling**         | Cloudinary                       |
| **Logging**                | Winston                          |
| **Security**               | Helmet, CORS, express-rate-limit |
| **Validation**             | Joi                              |

---

##  Setup & Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/nikhilbn19/social-media-microservices.git
   cd social-media-microservices
   ```

2. **Install dependencies for all services**

   ```bash
   npm install
   ```

3. **Set up environment variables**
   Each service has a `.env` file containing:

   ```
   PORT=
   MONGO_URI=
   JWT_SECRET=
   CLOUDINARY_API_KEY=
   REDIS_URL=
   RABBITMQ_URL=
   ```

4. **Start all services**

   ```bash
   npm run dev
   ```

---

##  Future Enhancements

* Add **notification service** using WebSockets or Kafka
* Implement **friend/follow system**
* Add **analytics service** for engagement insights

---

