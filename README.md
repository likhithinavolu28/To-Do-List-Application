# 📝 To-Do List Application

A modern, responsive and user-friendly **To-Do List Application** built using the MERN Stack (MongoDB, Express.js, React.js and Node.js).

This application helps users manage their daily activities, organize tasks, track progress and improve productivity through a clean and intuitive dashboard.

---

## 🚀 Project Overview

The To-Do List Application is a full-stack web application that allows users to create accounts, securely log in and manage their personal tasks.

Users can create, view, update, delete and categorize tasks, set priorities and due dates, and monitor their productivity through an interactive dashboard.

The application uses MongoDB Atlas for persistent data storage and JWT-based authentication for secure access.

---

## 🛠️ Technology Stack

### Frontend
- HTML5 – Web page structure
- CSS3 – Styling and responsive design
- JavaScript (ES6+) – Application logic
- React.js – Frontend development
- React Router DOM – Client-side navigation
- Axios – API communication

### Backend
- Node.js – JavaScript runtime
- Express.js – Backend framework
- REST API – Frontend and backend communication
- JWT – Authentication
- bcrypt – Password hashing

### Database
- MongoDB Atlas – Cloud database
- Mongoose – MongoDB object modeling

### Development Tools
- Visual Studio Code
- Git and GitHub
- Postman
- MongoDB Atlas
- Google Antigravity

---

## ✨ Features

### 1. User Authentication
- User registration
- User login and logout
- Secure password hashing
- JWT-based authentication
- Protected routes
- Individual user task management

### 2. Dashboard
- Total tasks overview
- Completed tasks
- Pending tasks
- Overdue tasks
- Today's tasks
- Task completion percentage
- Productivity statistics

### 3. Task Management (CRUD)
- Create new tasks
- View all tasks
- Edit existing tasks
- Delete tasks
- Mark tasks as completed
- Change task status

### 4. Task Organization
- Today's tasks
- Upcoming tasks
- Completed tasks
- Pending tasks
- Overdue tasks
- Search tasks by title
- Filter tasks by priority
- Filter tasks by category

### 5. Task Details

Each task contains:
- Task title
- Task description
- Category
- Priority (Low, Medium, High)
- Due date
- Status (Pending, In Progress, Completed)
- Created date
- Updated date

### 6. User Interface
- Modern and minimal dashboard
- Responsive design
- Dark and light themes
- Sidebar navigation
- Interactive task cards
- Progress indicators
- Toast notifications
- Confirmation dialogs
- Loading indicators

---

## 📂 Project Structure

```text
To-Do List Application/
│
├── client/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── hooks/
│   │   ├── services/
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   │
│   ├── .env
│   ├── package.json
│   └── vite.config.js
│
├── server/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── tests/
│   ├── utils/
│   │
│   ├── .env
│   ├── .env.example
│   ├── server.js
│   └── package.json
│
├── .gitignore
├── package.json
└── README.md
```

---

## ⚙️ Installation and Setup

Follow these steps to run the project locally.

### Prerequisites

Install the following software:

- Node.js and npm
- Visual Studio Code
- MongoDB Atlas account
- Git

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate into the project directory:

```bash
cd "To-Do List Application"
```

### Step 2: Install Frontend Dependencies

```bash
cd client
npm install
```

### Step 3: Install Backend Dependencies

Open another terminal:

```bash
cd server
npm install
```

### Step 4: Configure Environment Variables

Create a `.env` file inside the `server` directory.

**server/.env**

```env
PORT=5000

CLIENT_ORIGIN=http://localhost:5173

MONGODB_URI=your_mongodb_atlas_connection_string

JWT_SECRET=your_secure_random_jwt_secret
```

Replace the MongoDB connection string with your actual MongoDB Atlas URI.

Create another `.env` file inside the `client` directory.

**client/.env**

```env
VITE_API_URL=http://localhost:5000/api
```

**Important:** Never upload environment files containing credentials or secrets to GitHub.

---

## ▶️ Running the Application

The frontend and backend must run simultaneously in separate terminals.

### Start Backend Server

Open Terminal 1:

```bash
cd server
npm run dev
```

Expected output:

```text
Connected to MongoDB
API listening on port 5000
```

### Start Frontend Server

Open Terminal 2:

```bash
cd client
npm run dev
```

Expected output:

```text
VITE ready

Local: http://localhost:5173/
```

### Access the Application

Frontend:

http://localhost:5173

Backend:

http://localhost:5000

Backend health check:

http://localhost:5000/api/health

---

## 🔗 API Endpoints

### Authentication APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Authenticate a user |
| GET | `/api/auth/me` | Get logged-in user details |

### Task Management APIs

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/tasks` | Create a new task |
| GET | `/api/tasks` | Get all user tasks |
| GET | `/api/tasks/:id` | Get a specific task |
| PUT | `/api/tasks/:id` | Update an existing task |
| PATCH | `/api/tasks/:id/status` | Update task status |
| DELETE | `/api/tasks/:id` | Delete a task |

All task endpoints require valid authentication.

---

## 🗄️ Database Structure

The application uses MongoDB Atlas with two main collections.

### Users Collection

| Field | Description |
|---|---|
| _id | Unique user ID |
| name | User name |
| email | User email |
| password | Hashed password |
| createdAt | Account creation date |

### Tasks Collection

| Field | Description |
|---|---|
| _id | Unique task ID |
| userId | Reference to the user |
| title | Task title |
| description | Task description |
| category | Task category |
| priority | Low, Medium or High |
| dueDate | Task deadline |
| status | Pending, In Progress or Completed |
| createdAt | Task creation date |
| updatedAt | Last updated date |

Each task is associated with its owner through the `userId` reference.

---

## 🔐 Security Features

- Password hashing using bcrypt.
- JWT-based user authentication.
- Protected API endpoints.
- Environment variable configuration.
- MongoDB credentials protection.
- Input validation.
- User-specific task authorization.
- CORS configuration.
- Secure HTTP headers using Helmet.

---

## 🧪 Testing

The following functionality should be tested before deployment:

- User registration and login.
- Authentication and logout.
- Creating new tasks.
- Updating existing tasks.
- Deleting tasks.
- Changing task status.
- Searching and filtering tasks.
- Dashboard statistics.
- MongoDB data persistence.
- Responsive design across devices.
- Unauthorized access protection.

---

## 🌐 Future Enhancements

Possible improvements for future versions:

- Task reminders and notifications.
- Calendar-based task management.
- Drag-and-drop task organization.
- Recurring tasks.
- Task sharing and collaboration.
- Email notifications.
- Productivity reports and analytics.

---

## 🎯 Learning Outcomes

This project demonstrates practical experience with:

- Full-stack web development.
- React component architecture.
- REST API development.
- Node.js and Express.js.
- MongoDB database integration.
- Authentication and authorization.
- CRUD operations.
- Frontend and backend integration.
- Responsive UI development.
- Git and GitHub version control.

---

## 👨‍💻 Author

**Likhith Inavolu**

B.Tech – Computer Science and Engineering

**Project:** To-Do List Application

**Technology:** MERN Stack

---

## 📄 License

This project is developed for educational and learning purposes.

You are welcome to explore, learn and improve the application.