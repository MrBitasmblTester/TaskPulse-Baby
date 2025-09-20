# TaskPulse-Baby

Description
A web-based task management app where users can add, edit, and delete tasks. The app supports user authentication with JSON Web Tokens (JWT), organizes tasks by project, and displays tasks sorted by priority. The front-end is built with React, and the back-end uses Node.js with Express.

## Tech Stack
- React
- Node.js
- Express
- JSON Web Tokens (jsonwebtoken)

## Requirements
- Authenticate users using JWT (Use jsonwebtoken in Express to sign and verify tokens)
- Implement CRUD for tasks (Use Express routers and an in-memory store or a database)
- Categorize tasks by project (Include a `projectId` field in the task object)
- Sort tasks by priority (Perform sorting in the controller or in React before rendering)

## Installation
1. Clone the repo:
   bash
   git clone https://github.com/your-username/TaskPulse-Baby.git
   cd TaskPulse-Baby
   
2. Install server dependencies:
   bash
   cd server
   npm install
   
3. Install client dependencies:
   bash
   cd ../client
   npm install
   
4. Create a `.env` file in the `server` directory with the following:
   
   PORT=5000
   JWT_SECRET=your_jwt_secret
   
5. (Optional) If using a database, add the connection URL:
   
   MONGODB_URI=mongodb://localhost:27017/taskpulse
   

## Usage
1. Start the server:
   bash
   cd server
   npm start
   
2. Start the client:
   bash
   cd client
   npm start
   
3. Open your browser to `http://localhost:3000` to access the app.
4. Register or log in, then create and manage your tasks across projects.

## Implementation Steps
1. Initialize the Node.js/Express server.
2. Set up JWT authentication routes (`/auth/register` and `/auth/login`).
3. Create Express routers and controllers for task CRUD operations.
4. Define a task model with fields: `id`, `title`, `description`, `priority`, `projectId`, and `userId`.
5. Implement in-memory data store or connect to a database.
6. Add middleware to protect task routes with JWT verification.
7. Build React client using `create-react-app`.
8. Set up API service methods for authentication and task management.
9. Create React components: Login, Register, TaskList, TaskForm, ProjectSelector.
10. Implement state management and effect hooks to fetch and display data.
11. Add sorting logic on task list by priority.
12. Test end-to-end flow: user registration, login, CRUD operations.

## API Endpoints
- POST /auth/register   Register a new user.
- POST /auth/login      Authenticate user and get JWT.
- GET /tasks            Get all tasks for the authenticated user.
- POST /tasks           Create a new task.
- GET /tasks/:id        Get a single task by ID.
- PUT /tasks/:id        Update a task by ID.
- DELETE /tasks/:id     Delete a task by ID.