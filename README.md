# Voting Application

This is a backend application for a voting system where users can vote for candidates. It provides functionalities for user authentication, candidate management, and voting.

## Features

- User sign up and login with Aadhar Card Number and password
- User can view the list of candidates
- User can vote for a candidate (only once)
- Admin can manage candidates (add, update, delete)
- Admin cannot vote

## Technologies Used

- Node.js
- Express.js
- MongoDB
- JSON Web Tokens (JWT) for authentication


# API Endpoints

## Authentication

### Sign Up
- `POST user/signup`: Sign up a user(body should contain details of user)

### Login
- `POST user/login`: Login a user(body should contain aadharCardNumber and password of user)

## Candidates

### Get Candidates
- `GET /candidate`: Get the list of candidates

### Add Candidate
- `POST /candidate`: Add a new candidate (Admin only)

### Update Candidate
- `PUT /candidate/:id`: Update a candidate by ID (Admin only)

### Delete Candidate
- `DELETE /candidate/:id`: Delete a candidate by ID (Admin only)

## Voting

### Get Vote Count
- `GET /candidate/vote/counts`: Get the count of votes for each candidate

### Vote for Candidate
- `POST /candidate/vote/:id`: Vote for a candidate (User only)

## User Profile

### Get Profile
- `GET /user/profile`: Get user profile information

### Change Password
- `PUT /user/profile/password`: Change user password(body should contain currentPassword and newPassword of user)

## include MONGODB_URL_LOCAL=(clusterlink) JWT_SECRET=your-very-secret-key in .env
