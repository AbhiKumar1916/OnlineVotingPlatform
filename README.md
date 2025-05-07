# Smart Voting Platform

A secure online voting platform with face recognition and OTP verification.

## Features

- Voter registration with age verification
- Face recognition for voter authentication
- OTP verification via phone number
- Admin dashboard for candidate management
- Real-time vote counting
- Secure voting system

## Prerequisites

- Node.js (v14 or higher)
- MongoDB
- Twilio Account (for OTP)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd EVMPlatForm
```

2. Install backend dependencies:
```bash
cd backend
npm install
```

3. Install frontend dependencies:
```bash
cd ../frontend
npm install
```

4. Download face recognition models:
```bash
cd scripts
node downloadModels.js
```

5. Set up environment variables:
Create a `.env` file in the backend directory with the following:
```
PORT=5000
MONGODB_URI=mongodb://localhost:27017/voting-platform
JWT_SECRET=your_jwt_secret_key_here
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number
```

## Running the Application

1. Start MongoDB:
```bash
mongod
```

2. Start the backend server:
```bash
cd backend
npm run dev
```

3. Start the frontend development server:
```bash
cd frontend
npm run dev
```

The application will be available at:
- Frontend: http://localhost:5173
- Backend: http://localhost:5000

## Usage

### Admin
1. Login to admin dashboard using admin credentials
2. Manage candidates (add/remove)
3. View election results
4. Reset votes if needed

### Voters
1. Register with personal details and face capture
2. Verify phone number via OTP
3. Login with credentials
4. Complete face verification
5. Cast vote for preferred candidate

## Security Features

- Face recognition for voter verification
- OTP verification for registration
- JWT-based authentication
- Age verification (18+ only)
- One vote per voter
- Secure password hashing

## Tech Stack

- Frontend: React.js with Vite
- Backend: Node.js with Express.js
- Database: MongoDB
- Face Recognition: Python
- UI Framework: Material-UI
- Authentication: JWT
- OTP Service: Nodemailer
