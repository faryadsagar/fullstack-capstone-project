---
name: research authentication in React and Express
about: this task involves researching methods to set up authentication in both React
  and Express.
title: ''
labels: new
assignees: ''

---

**As a** product manager  
**I need** a user authentication system  
**So that** users can securely log in and access their personalized content.

## Details and Assumptions
- The system should support email/password login as well as OAuth for social logins (e.g., Google, Facebook).
- The authentication flow should be simple and intuitive, with error messages displayed clearly.
- Sensitive data like passwords should be securely hashed and stored using a strong hashing algorithm.
- User sessions should be managed using JWT tokens or similar secure methods to prevent session hijacking.
- Failed login attempts should be limited to 3 to prevent brute-force attacks.

## Acceptance Criteria

**Given** a user navigates to the login page,  
**When** they enter their correct credentials and click "Login",  
**Then** they are authenticated and redirected to the homepage.

**Given** a user enters incorrect credentials,  
**When** they click "Login",  
**Then** an error message "Invalid email or password" is shown.

**Given** a user successfully logs in using Google OAuth,  
**When** the login is successful,  
**Then** they are redirected to the homepage and their user profile is created if it doesn't already exist.

**Given** a user enters incorrect credentials 3 times in a row,  
**When** they attempt to log in again,  
**Then** their account is temporarily locked for 10 minutes with a message saying "Too many login attempts, please try again later."
