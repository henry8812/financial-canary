# Investment Planning Application

## Introduction

This repository contains the source code and documentation for an investment planning application. The application allows users to visualize real-time behavior of stock values, manage their portfolio, and make informed decisions about their investments.

## Functional Requirements

### Use Cases

#### 1. User Registration
- **Actors:** User
- **Description:** The user registers in the application by providing personal information.

#### 2. Login
- **Actors:** User
- **Description:** The user logs into the application using their credentials.

#### 3. Stock Selection
- **Actors:** User
- **Description:** The user selects the stocks they want to include in their portfolio.

#### 4. Real-time Graph Visualization
- **Actors:** User
- **Description:** The user views a real-time graph showing the evolution of selected stock values.

#### 5. Portfolio Management
- **Actors:** User
- **Description:** The user manages their portfolio, adding or removing stocks, and viewing details about their investments.

### Detailed Functional Requirements

#### 1. Integration with Polygon.io
The application must integrate with the Polygon.io API to obtain real-time data of stock values.

#### 2. Automatic Graph Update
The graph in the user interface must update automatically as new data is obtained from the API.

#### 3. User Management
The application must allow users to register, log in, and manage their accounts.

#### 4. Stock Selection
Users must be able to select the stocks they want to include in their portfolio from a list provided by the application.

#### 5. Portfolio Management
Users must be able to add, remove, and view details of stocks in their portfolio.

## Non-functional Requirements

### 1. Performance
The application must have an acceptable response time, and real-time graph updates must be fast and efficient.

### 2. Usability
The user interface must be intuitive and easy to use, even for users with no financial experience.

### 3. Security
User data and transactions must be secure. The application must implement security measures, such as secure authentication.

### 4. Availability
The application must be available for access at all times, ensuring minimal downtime.

## User Management with MongoDB

### 1. User Collection Structure
```javascript
{
  _id: ObjectId,
  name: String,
  email: String,
  password: String,  // Stored securely using hashing and salt
  portfolio: [String],  // List of stocks in the user's portfolio
}

## User Management with MongoDB

### 2. Authentication Procedures

The application will use the `useraccounts:core` package from Meteor.js to manage user registration, login, and logout.

#### User Registration

- Users can register by providing their name, email, and a secure password.
- Passwords will be stored securely using hashing and salt techniques.

#### User Login

- Registered users can log into the application using their email and password.
- The application will authenticate the user against the stored credentials.

#### User Logout

- Users can log out of their accounts securely.

#### Password Recovery

- Users who forget their passwords can request a password reset.
- The application will send a secure password reset link to the user's registered email.

### 3. User Privileges

- Authenticated users can select stocks, manage their portfolio, and view real-time graphs.
- Administrator users (if implemented) will have additional privileges for system management.

## Conclusions

This repository outlines the requirements for the development of the investment planning application. The application is expected to provide users with an efficient and secure tool to make informed decisions about their investments.
