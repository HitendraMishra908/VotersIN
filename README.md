[github.com/HitendraMishra908](https://github.com/HitendraMishra908)

VotersIN – MERN Stack Secure Voting Platform

VotersIN is a full-stack voting application built using the MERN stack.
It provides secure OTP authentication (via Gmail), Aadhar verification, room-code based voting access, and an admin dashboard to manage voting rooms, candidates, and results.

Download Links

Project ZIP: https://drive.google.com/file/d/1iGvLjSoWTJP37sKc3KT5pHykNwtMj1v5/view?usp=sharing

Technologies Used

Frontend: React.js, JavaScript
Backend: Node.js, Express.js
Database: MongoDB
Authentication: JSON Web Tokens (JWT)
Email Service: Nodemailer (Gmail OTP)
UI: Yellow & Orange theme

Key Features

OTP login using Gmail (via Nodemailer)

Hashed OTP + JWT-based authentication

Aadhar verification to prevent duplicate voting

Room-code based access validation

One-user one-vote system

Admin dashboard for room creation and candidate management

Real-time vote results

Protected REST APIs with middleware validation

Clean React UI with yellow/orange theme

Easy setup and configuration

Installation & Setup Guide
1. Install Required Software

Before starting, install:

Node.js (v14 or higher)

MongoDB

Gmail account with App Password enabled

2. Download and Extract the Project

Download the ZIP from the drive link above

Extract it to your system

3. Install Dependencies

Open terminal inside the project folder:

Backend:
cd server
npm install

Frontend:
cd client
npm install

4. Environment Variables Setup

Create a file named .env inside the server/ folder and add:

MONGO_URI=your_mongo_connection_string
PORT=5000
EMAIL_USER=your_email_here
EMAIL_PASS=your_gmail_app_password_here
JWT_SECRET=your_jwt_secret_key_here


Note: .env file is not included for security reasons.
Use .env.example as reference if provided.

5. Generate Gmail App Password

Open Google Account

Go to Security

Enable 2-Step Verification

Open App Passwords

Select Mail

Generate password

Use this 16-digit password as EMAIL_PASS

6. Start MongoDB

Open a new terminal and run:

mongod


Keep this terminal running.

7. Start the Application
Backend:
cd server
npm run dev

Frontend:
cd client
npm start

8. Access the Website

Open browser:

http://localhost:3000

Project Flow Overview
User:

Enters Aadhar + phone number

Receives OTP via Gmail

Logs in using OTP

Enters room code

Votes once (locked afterwards)

Redirected to Thank-You page

Admin:

Logs into admin dashboard

Creates rooms

Adds candidates

Views live results

Troubleshooting
OTP Issues

Ensure App Password is used

Check EMAIL_USER and EMAIL_PASS

Verify Gmail 2FA is ON

MongoDB Not Connecting

Check if mongod is running

Verify your MONGO_URI

Port Already in Use

Change port in .env:

PORT=5001

NPM Errors

Delete:

node_modules
package-lock.json


Then reinstall:

npm install

Project Information

Project Name: VotersIN
Version: 1.0.0
Tech Stack: MERN
UI Theme: Yellow / Orange
OTP Delivery: Gmail (Nodemailer)

Support

Check logs in terminal

Verify API routes

Review .env configuration

Ensure MongoDB is running
