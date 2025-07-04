# React Job Portal

A full-stack MERN (MongoDB, Express, React, Node.js) job portal application that allows job seekers to find and apply for jobs, and employers to post and manage job listings. The project features secure authentication, file uploads, and a modern, responsive UI.

---

## Features

### For Job Seekers
- Register and login securely
- Browse and search for jobs
- View job details
- Apply for jobs with resume upload (Cloudinary integration)
- Track your applications

### For Employers
- Register and login securely
- Post new job listings
- Edit and delete your jobs
- View applications for your jobs

### General
- JWT-based authentication and role-based access
- MongoDB Atlas for database
- Cloudinary for file uploads
- Responsive React frontend (Vite)
- Error handling and validation

---

## Project Structure

```
react-job-portal-main/
├── backend/
│   ├── app.js
│   ├── server.js
│   ├── package.json
│   ├── .env
│   ├── controllers/
│   ├── database/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   └── utils/
└── frontend/
    ├── src/
    ├── public/
    ├── package.json
    └── vite.config.js
```

---

## Getting Started

### Prerequisites
- Node.js (v16+ recommended)
- npm
- MongoDB Atlas account
- Cloudinary account

### 1. Clone the Repository
```bash
git clone <repo-url>
cd react-job-portal-main
```

### 2. Backend Setup
```bash
cd backend
npm install
```

#### Configure Environment Variables
Create a `.env` file in the `backend/` directory:
```env
PORT=4000
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
FRONTEND_URL=http://localhost:5173
DB_URL=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret
JWT_EXPIRE=7d
COOKIE_EXPIRE=7
NODE_ENV=development
```

- Get Cloudinary keys from your [Cloudinary dashboard](https://cloudinary.com/)
- Get MongoDB connection string from [MongoDB Atlas](https://cloud.mongodb.com/)
- Generate a JWT secret using `node -e "console.log(require('crypto').randomBytes(64).toString('hex'))"`

#### Start Backend Server
```bash
npm run dev
# or
node server.js
```

---

### 3. Frontend Setup
```bash
cd ../frontend
npm install
```

#### Start Frontend Server
```bash
npm run dev
```

- The app will be available at [http://localhost:5173](http://localhost:5173)

---

## Usage
- Register as a job seeker or employer
- Employers can post, edit, and delete jobs
- Job seekers can browse jobs and apply with a resume
- Both can manage their profiles and applications

---

## Technologies Used
- **Frontend:** React, Vite, React Router, Axios, React Icons
- **Backend:** Node.js, Express, MongoDB, Mongoose, JWT, Cloudinary, bcrypt
- **Other:** dotenv, express-fileupload, cookie-parser, cors

---

## Security Notes
- Never commit your `.env` file or secrets to version control
- Use strong, unique JWT secrets and database passwords
- Restrict MongoDB Atlas access to trusted IPs

---

## License
This project is licensed under the MIT License.

---

## Author
- [Your Name]

---

## Screenshots
_Add screenshots of the app here_

---

## Deployment

You can deploy this project to popular cloud platforms. Here are some recommended options:

### Backend (Node.js/Express)
- [Render](https://render.com/)
- [Heroku](https://heroku.com/)
- [Railway](https://railway.app/)
- [Vercel (Serverless)](https://vercel.com/)

### Frontend (React/Vite)
- [Vercel](https://vercel.com/)
- [Netlify](https://netlify.com/)
- [Render (Static Sites)](https://render.com/)

#### Deployment Steps (Example: Vercel for Frontend)
1. Push your code to GitHub.
2. Go to [Vercel](https://vercel.com/) and import your frontend repo.
3. Set the build command to `npm run build` and output directory to `dist`.
4. Add any required environment variables.
5. Deploy and get your live URL!

#### Deployment Steps (Example: Render for Backend)
1. Push your backend code to GitHub.
2. Go to [Render](https://render.com/) and create a new Web Service.
3. Connect your repo and set the start command to `npm start` or `node server.js`.
4. Add your environment variables from `.env`.
5. Deploy and get your backend API URL.

---

## Contact
For questions or support, open an issue or contact the maintainer.
