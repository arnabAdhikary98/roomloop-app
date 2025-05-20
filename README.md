# RoomLoop - Micro-Meetup Platform

![RoomLoop Desktop View](assets/room_loop_homepage.png)
![RoomLoop Mobile View](assets/room_loop_mobile.png)

[![CI](https://github.com/yourusername/roomloop-app/actions/workflows/ci.yml/badge.svg)](https://github.com/yourusername/roomloop-app/actions/workflows/ci.yml)
[![Deploy](https://github.com/yourusername/roomloop-app/actions/workflows/deploy.yml/badge.svg)](https://github.com/yourusername/roomloop-app/actions/workflows/deploy.yml)

## Live Demo
Visit the live application at: [RoomLoop](https://room-loop-ten.vercel.app/)

## Overview

RoomLoop is a modern web application designed to facilitate micro-meetups and focused discussions. It enables users to create and join time-bounded virtual rooms for meaningful collaborations and connections. The platform automatically manages room lifecycles, transitioning them from scheduled to live to closed states based on predefined timeframes.

### Key Features

- **Smart Room Management**: Create rooms with specific topics, time slots, and tags
- **Real-time Communication**: Engage in live discussions with text messages and emoji reactions
- **Intelligent Scheduling**: Automatic room status transitions based on timeframes
- **User Authentication**: Secure sign-up and sign-in functionality
- **Responsive Design**: Seamless experience across desktop and mobile devices

## Tech Stack

### Frontend
- **Framework**: Next.js 14 (React)
- **Styling**: TailwindCSS
- **State Management**: React Context API
- **UI Components**: Custom components with TailwindCSS
- **Type Safety**: TypeScript

### Backend
- **Runtime**: Node.js
- **API Routes**: Next.js API Routes
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: NextAuth.js
- **API Documentation**: Swagger/OpenAPI

### DevOps & Tools
- **Version Control**: Git
- **CI/CD**: GitHub Actions
- **Deployment**: Vercel
- **Code Quality**: ESLint, Prettier
- **Testing**: Jest

## Getting Started

### Prerequisites

- Node.js 18+ and npm
- MongoDB database (local or Atlas)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/roomloop-app.git
   cd roomloop-app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env.local` file in the root directory with the following variables:
   ```
   # MongoDB Connection String
   MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/roomloop?retryWrites=true&w=majority

   # NextAuth Configuration
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=your-secret-key-for-jwt-encryption
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

### MongoDB Setup

1. Create a free MongoDB Atlas account at [mongodb.com/cloud/atlas](https://mongodb.com/cloud/atlas)
2. Create a new cluster
3. Create a database user with read/write permissions
4. Add your IP address to the network access list
5. Get your connection string and replace the placeholder in `.env.local`

## CI/CD Pipeline

This project uses GitHub Actions for continuous integration and deployment:

### CI Workflow

The CI workflow runs on every push to main and pull requests:
- Linting with ESLint
- Type checking with TypeScript
- Building the application

### Test Workflow

The test workflow runs on every push to main and pull requests:
- Sets up MongoDB for testing
- Verifies database connection
- Runs tests (when added)

### CD Workflow

The CD workflow automatically deploys to Vercel on pushes to the main branch:
- Builds the application
- Deploys to Vercel production environment

### Setting up CI/CD

1. Fork or push this repository to your GitHub account
2. Set up a Vercel account and connect it to your repository
3. Add the following secrets to your GitHub repository:
   - `VERCEL_TOKEN`: Your Vercel API token
4. The CI/CD pipeline will automatically run on push to the main branch

## Deployment

### Deploying to Vercel

1. Push your code to a GitHub repository
2. Sign up for a [Vercel](https://vercel.com) account
3. Import your repository
4. Add the environment variables from `.env.local` to your Vercel project
5. Deploy!

## Project Structure

- `/src/app`: Next.js App Router components and pages
- `/src/app/api`: API routes for backend functionality
- `/src/app/lib`: Utility functions and database connection
- `/src/app/models`: Mongoose models for database schema
- `/src/app/components`: Reusable React components

## License

This project is licensed under the MIT License.
