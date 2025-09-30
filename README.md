# Source Start Course Selling Website Backend

Welcome to the Source Start Course Selling Website Backend repository! We're excited to have you as a potential contributor to our course selling platform backend built with Node.js, Express, and MongoDB.

## Table of Contents

- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [API Endpoints](#api-endpoints)
- [How to Contribute](#how-to-contribute)
- [Features to Implement](#features-to-implement)


## Introduction

This repository contains the backend API for a course selling platform (similar to Udemy) built with Node.js, Express.js, and MongoDB. The platform supports both user and admin functionalities including course creation, purchasing, user authentication, and course management. As part of "Source Start," an open source event organized by CSI SPIT, we invite developers, backend enthusiasts, and API learners to contribute to this project by adding new features, improving security, enhancing database design, or optimizing the codebase.

## Getting Started

To get started with the project, follow these steps:

1. **Fork the Repository:** Click the "Fork" button on the top right corner of this repository to create a copy in your GitHub account.

2. **Clone Your Fork:** Clone your fork of the repository to your local machine using `git clone`.

   ```bash
   git clone https://github.com/your-username/CourseSellingWebsiteBackend.git
   ```

3. **Install Dependencies:** Navigate to the project directory and install the required dependencies.

   ```bash
   cd CourseSellingWebsiteBackend
   npm install
   ```

4. **Set Up Environment Variables:** Create a `.env` file in the root directory and add your environment variables:

   ```bash
   MONGO_URL=your_mongodb_connection_string
   JWT_SECRET_USER=your_jwt_secret_for_users
   JWT_SECRET_ADMIN=your_jwt_secret_for_admins
   ```

5. **Start the Development Server:** Start the server in development mode.

   ```bash
   npm run dev
   # OR
   npm start
   ```

6. **Test the API:** Visit [http://localhost:3000](http://localhost:3000) in your browser or use tools like Postman to test the API endpoints.

## Project Structure

The project is structured as follows:

- `index.js`: Main server file with Express app configuration and route mounting
- `db.js`: Database connection and schema definitions using Mongoose
- `package.json`: Node.js project configuration and dependencies
- `routes/`: Directory containing API route handlers
  - `user.js`: User-related routes (signup, login, purchases)
  - `admin.js`: Admin-related routes (signup, login, course management)
  - `courses.js`: Course-related routes (view all courses)
- `middlewares/`: Directory containing middleware functions
  - `userMiddleware.js`: JWT authentication middleware for users
  - `adminMiddleware.js`: JWT authentication middleware for admins
  - `middleware.js`: Common middleware functions
- `.env`: Environment variables (create this file)
- `README.md`: This README file

## API Endpoints

### User Routes (`/user`)
- `POST /user/signup` - Register a new user
- `POST /user/login` - Login user and receive JWT token
- `POST /user/course/purchase` - Purchase a course (protected)
- `GET /user/purchases` - View all purchased courses (protected)

### Admin Routes (`/admin`)
- `POST /admin/signup` - Register a new admin
- `POST /admin/login` - Login admin and receive JWT token
- `POST /admin/create-course` - Create a new course (protected)
- `PUT /admin/update-course` - Update an existing course (protected)
- `GET /admin/created-courses` - View all courses created by admin (protected)
- `DELETE /admin/delete-course` - Delete a course (protected)

### Course Routes (`/`)
- `GET /courses` - View all available courses (public)

**Note:** Protected routes require `Authorization: Bearer <token>` header.

## How to Contribute

We welcome and encourage contributions from the community to make this project better. To contribute:

1. **Create a New Branch:** Create a new branch for your contribution.

   ```bash
   git checkout -b feature/my-contribution
   ```

2. **Make Changes:** Work on your contribution, make changes, and add new features.

3. **Test Your Changes:** Test your changes thoroughly to ensure they work as expected and don't break existing functionality.

4. **Commit Changes:** Commit your changes with a descriptive commit message.

   ```bash
   git commit -m "Add feature: Description of your contribution"
   ```

5. **Push Changes:** Push your changes to your fork on GitHub.

   ```bash
   git push origin feature/my-contribution
   ```

6. **Create a Pull Request:** Create a pull request (PR) from your fork to this repository. Describe your changes and the purpose of the PR.

We will review your PR and merge it if it meets the project's standards.

## Features to Implement

Here are some ideas for contributions:

- **Input Validation:** Enhance Zod schemas for better data validation
- **Email Verification:** Add email verification system for user registration
- **Password Reset:** Implement forgot password functionality
- **Course Categories:** Add category system for better course organization
- **Search & Filter:** Implement course search and filtering capabilities
- **Rating System:** Add course rating and review functionality
- **Payment Integration:** Integrate with payment gateways (Stripe, Razorpay)
- **File Upload:** Add functionality to upload course materials and videos
- **Notifications:** Implement email/SMS notifications for purchases
- **Analytics:** Add admin dashboard with sales and user analytics
- **Cache Implementation:** Add Redis caching for better performance
- **API Documentation:** Create comprehensive API documentation with Swagger
- **Rate Limiting:** Implement rate limiting to prevent API abuse
- **Logging System:** Add structured logging with Winston or similar
- **Unit Tests:** Add comprehensive test coverage with Jest

---

Thank you for participating in "Source Start" organized by CSI SPIT! We look forward to your contributions to help make this course selling platform more robust and feature-rich. Whether you're a beginner learning backend development or an experienced developer, there's something for everyone to contribute. Happy coding! 🚀💻
