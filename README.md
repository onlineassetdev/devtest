# Junior Developer Coding Test

## Table of Contents
- [Overview](#overview)
- [Technical Stack](#technical-stack)
- [Project Setup](#project-setup)
- [Database Schema](#database-schema)
- [API Implementation](#api-implementation)
- [Frontend Implementation](#frontend-implementation)
- [Database Seeding](#database-seeding)
- [Styling & Responsiveness](#styling--responsiveness)
- [Bonus Points](#bonus-points)
- [Submission Requirements](#submission-requirements)
- [Evaluation Criteria](#evaluation-criteria)
- [Timeline and Points](#timeline-and-points)
- [Resources](#resources)

## Overview
This coding test is designed to assess your skills in full-stack web development using modern technologies. You'll be building a dashboard application with user and product management capabilities.

## Technical Stack
- **Frontend**: Vue 3 with Composition API
- **UI Components**: TailwindCSS
- **Database**: PostgreSQL
- **Backend**: Node.js (with Express)
- **API Client**: Axios or Fetch API
- **ORM**: Optional

## Project Setup
1. Initialize a new Vue 3 project using Vite.
2. Install and configure TailwindCSS for styling in the project.
3. Set up a Node.js backend (Express.js) with PostgreSQL as the database.
4. Configure a `.env` file with necessary environment variables for the PostgreSQL connection.

## Database Schema
Create a simple database schema with the following tables:

### Users Table
| Field | Type | Constraints |
|-------|------|-------------|
| id | Auto-increment | Primary key |
| name | string | - |
| email | string | Unique |
| created_at | timestamp | Defaults to now |
| updated_at | timestamp | Defaults to now, auto-updated |

### Products Table
| Field | Type | Constraints |
|-------|------|-------------|
| id | Auto-increment | Primary key |
| name | string | - |
| price | decimal | - |
| category | string | - |
| created_at | timestamp | - |
| updated_at | timestamp | - |

> **Note**: No need to set up complex relationships (i.e., foreign keys). For simplicity, focus on these two tables.

## API Implementation
Create the following API endpoints using Express.js:

### User Endpoints
- `GET /api/users` - Get a list of all users
- `POST /api/users` - Create a new user (request body should include name, email)

### Product Endpoints
- `GET /api/products` - Get a list of all products
- `POST /api/products` - Create a new product (request body should include name, price, category)

Make sure to handle basic error responses (e.g., user already exists, validation errors).
You can use Sequelize, Knex.js, or raw SQL queries with pg to interact with the PostgreSQL database.

## Frontend Implementation
Create a simple dashboard with the following pages:

### Users Management Page
- Display a list of users with their id, name, and email.
- Allow adding new users via a form (name, email).

### Products Management Page
- Display a list of products with id, name, price, and category.
- Allow adding new products via a form (name, price, category).

For styling, use TailwindCSS to make it clean and responsive.
Use Axios or Fetch API to connect to the API endpoints and display the data. Handle loading states and errors properly.

## Database Seeding
Create a seeding script to populate the users and products tables with at least 5 sample users and 5 sample products.

**Example Users:**
- John Doe
- Jane Smith
- Bob Johnson
- Alice Williams
- Charlie Brown

**Example Products:**
- Laptop
- Phone
- Tablet
- Headphones
- Keyboard

This will allow you to test the data displayed in your frontend pages.

## Styling & Responsiveness
- Use TailwindCSS to ensure that the dashboard is responsive on both mobile and desktop screens.
- Ensure basic UI accessibility (use proper aria-labels and semantic HTML where applicable).

## Bonus Points (Optional)
If you finish early or want to challenge yourself, you can add:
- Search functionality for users and products on their respective pages.
- Simple form validation (e.g., ensuring the email is valid, price is a number).
- Pagination for the user and product lists (just a basic implementation).
- Basic error handling (e.g., form errors, API errors).
- Deployment: Deploy the app to a platform like Vercel, Netlify, or Render.

## Submission Requirements
- GitHub repository with your solution.
- README with:
  - Setup instructions (how to run the project locally).
  - A short explanation of the technologies used.
  - Include screenshots of the working application in the README.
- (Optional) Deploy the project to a hosting platform.

## Evaluation Criteria
- **Code organization**: Proper use of Vue 3, Express, and TailwindCSS.
- **Database interaction**: Clear and understandable database setup with API interaction.
- **UI/UX design**: Clean, responsive, and accessible design.
- **Functionality**: Proper CRUD operations, error handling, and state management.
- **Bonus**: Any additional features or polish will be considered.ign.

## Timeline and Points
You should aim to complete this task within 3 days. However, take the time you need to produce quality code.
Bonus:
- Any additional features or polish will be considered.
- Functionality: Proper CRUD operations, error handling, and state management.

## Resources
- [Vue 3 Documentation](https://vuejs.org/)
- [Tailwind CSS Documentation](https://tailwindcss.com/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)