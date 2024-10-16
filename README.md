# SignUpFeatureTask6

This project is a Signup feature implementation, part of the APDS7311 course. The project includes a fully functional frontend signup form integrated with backend services and a MongoDB database. 

The project focuses on secure data transmission, storage, and appropriate security practices for user authentication.

---

## Table of Contents

- [Technologies Used](#technologies-used)
- [Features](#features)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Running the Project](#running-the-project)
- [Important Security Features](#important-security-features)

---

## Technologies Used

**Frontend:**
- React.js
- Tailwind CSS (For styling)
- Axios (For API calls)
- ESLint (For code linting)

**Backend:**
- Node.js with Express.js (API services)
- MongoDB (Database)
- JWT (For user authentication)

**Other Tools:**
- GitHub Actions (CI/CD)
- Docker (optional for deployment)
  
---

## Features

- **User Signup**: Users can create accounts by entering their name, surname, email, username, and password.
- **Form Validation**: Form input is validated on the client side to ensure required fields are not left blank.
- **Backend Services**: Secure API services handle user registration and authentication.
- **Database Integration**: MongoDB is used to securely store user data.
- **Security**: The project includes strong password hashing, JSON Web Tokens (JWT) for authentication, and HTTPS for secure data transmission.

---

## Project Structure

```bash
├── frontend
│   ├── src
│   │   ├── components
│   │   │   ├── SignupForm.js # Signup form component
│   │   └── App.js            # Main app component
│   └── public
│       └── index.html
├── backend
│   ├── controllers
│   │   └── userController.js  # Logic for user signup API
│   ├── routes
│   │   └── userRoutes.js      # API routes for user signup
│   ├── models
│   │   └── User.js            # MongoDB User model
│   └── app.js                # Main backend entry point
├── package.json
└── README.md
````

**Setup Instructions**
1. Clone the repository
To get started with the project, clone the repository:

```bash

Copy code

git clone 


https://github.com/thekayd/SignUpFeatureTask6.git
```

cd SignUpFeatureTask6

**2. Install Dependencies**

For the frontend:

```bash
Copy code
cd frontend
npm install
```
For the backend:

```bash
Copy code
cd backend
npm install
```
**3. Configure Environment Variables**
For the backend, create a .env file in the backend directory and add the following environment variables:

```makefile
Copy code
PORT=5000
MONGODB_URI=your_mongo_uri
JWT_SECRET=your_secret_key
```

Replace your_mongo_uri with your actual MongoDB connection string and your_secret_key with a strong secret key for JWT.

**4. Running the Application**

start the backend:

```bash
Copy code
cd backend
npm start
```
The backend should be running on http://localhost:5000.

Start the frontend:

```bash
Copy code
cd frontend
npm start
```
The frontend should be running on http://localhost:3000.

**Running the Project**

1. Backend:
To run the backend server, navigate to the backend folder and use:

```bash
Copy code
npm start
```
This will launch the Express server and connect to MongoDB.

2. Frontend:
To run the frontend locally, use the following command in the frontend folder:

```bash
Copy code
npm start
```

This will launch the React development server and open the app in your browser.



**Important Security Features**

Password Hashing: User passwords are hashed using bcrypt before being stored in the database for better security.

JWT Authentication: After signup, users are issued a JWT token that can be used for subsequent authenticated requests.

Input Validation: The form ensures that required fields are filled in correctly on the frontend. Additionally, backend validation checks are also in place to handle malicious inputs.

Secure Data Transmission: HTTPS should be used in production for secure data transmission.

**Future Enhancements**
Email Verification: Implement an email verification feature to confirm user email addresses before allowing login.

Rate Limiting: Introduce rate limiting on the signup and login endpoints to prevent abuse.

Forgot Password: Add functionality for users to reset their passwords securely.

```
##License

This project is licensed under the MIT License.
```



