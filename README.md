# ADBU_CourseMaterialHub

A web platform for Assam Don Bosco University where students and teachers
can upload, browse, and download course resources like lecture notes,
slides, and documents — organized by course and subject.

# Features

- Student and Admin accounts
- Upload resources (PDF, PPT, DOC, images)
- Browse resources by Course and Subject
- Search resources by title
- Preview files directly in browser
- Download files
- Dark and Light mode
- Mobile responsive with slide-in menu



## Tech Stack

1. Frontend
- HTML, CSS, Vanilla JavaScript

2. Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- bcrypt for password hashing
- Multer + Cloudinary for file uploads


3. Project Structure

project/
│
├── frontend/
│   ├── index.html
│   ├── styles.css
│   └── app.js
│
├── backend/
│   ├── server.js
│   ├── config/
│   │   ├── db.js
│   │   └── cloudinary.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Course.js
│   │   ├── Subject.js
│   │   └── Resource.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── courseRoutes.js
│   │   ├── subjectRoutes.js
│   │   └── resourceRoutes.js
│   └── middleware/
│       └── authMiddleware.js
│
└── README.md

## Getting Started

### Prerequisites
- Node.js installed
- MongoDB Atlas account
- Cloudinary account

### Installation

1. Clone the repository
   bash
   git clone https://github.com/ariesha123/ADBU_CourseMaterialHub.git
   cd ADBU_CourseMaterialHub


2. Install dependencies
   bash
   cd backend
   npm install


3. Create a `.env` file inside the backend folder

   MONGO_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   CLOUDINARY_NAME=your_cloudinary_name
   CLOUDINARY_KEY=your_cloudinary_api_key
   CLOUDINARY_SECRET=your_cloudinary_api_secret


4. Start the backend server
   bash
   node server.js


5. Open `frontend/index.html` in your browser




## API Endpoints

### Auth
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/auth/register | Register a new user |
| POST | /api/auth/login | Login and get token |
| POST | /api/auth/logout | Logout |
| POST | /api/auth/forgot-password | Send reset email |
| POST | /api/auth/reset-password/:token | Reset password |

### Courses
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/courses | Get all courses |
| POST | /api/courses | Create course (admin only) |
| DELETE | /api/courses/:id | Delete course (admin only) |

### Subjects
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/subjects | Get all subjects |
| GET | /api/subjects/course/:id | Get subjects by course |
| POST | /api/subjects | Create subject (admin only) |
| DELETE | /api/subjects/:id | Delete subject (admin only) |

### Resources
| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/resources | Get all resources |
| GET | /api/resources/search?keyword= | Search resources |
| GET | /api/resources/subject/:id | Get resources by subject |
| GET | /api/resources/:id | Get single resource |
| POST | /api/resources/upload | Upload resource (auth required) |
| DELETE | /api/resources/:id | Delete resource |
## Developer

Built by Ariesha R Marak — https://github.com/ariesha123
Video demonstartion: https://youtu.be/4XO0fyiP7N8
