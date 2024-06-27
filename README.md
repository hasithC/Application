### README.md
#### Project Overview
This project is a Task Management Application that allows users to perform CRUD operations on tasks. It consists of a front-end built with React.js and a back-end API built with Node.js and Express.js. MongoDB is used as the database to store task information.
#### Prerequisites
Before you begin, ensure you have the following installed on your machine:
- Node.js (v14.0.0 or higher)
- npm (Node Package Manager)
- MongoDB (make sure it's running locally or have a MongoDB Atlas account for cloud deployment)
#### Installation
1. **Clone the repository**
   ```
   git clone https://github.com/your-username/task-management-app.git
   cd task-management-app
   ```
2. **Install dependencies**
   - **Front-end** (React):
     ```
     cd frontend
     npm install
     ```
   
   - **Back-end** (Node.js & Express):
     ```
     cd backend
     npm install
     ```

3. **Set up environment variables**
   - Create a `.env` file in the `backend` directory and add the following:
     ```
     PORT=5000
     MONGODB_URI=mongodb://localhost:27017/task-manager
     ```
     Adjust `MONGODB_URI` if your MongoDB instance is running on a different port or if you're using MongoDB Atlas.

4. **Database Setup**
   - Make sure MongoDB is running. If not, start MongoDB by running `mongod` in a terminal window.

5. **Run the application**
   - **Front-end** (React):
     ```
     cd frontend
     npm start
     ```
     This will start the React development server on `http://localhost:3000`.

   - **Back-end** (Node.js & Express):
     ```
     cd backend
     npm start
     ```
     This will start the Node.js server on `http://localhost:5000`.

6. **Accessing the application**
   - Open your web browser and go to `http://localhost:3000` to access the Task Management Application.

#### API Endpoints
- **GET all tasks**: `GET http://localhost:5000/api/tasks`
- **POST a new task**: `POST http://localhost:5000/api/tasks`
  - Body: `{ "title": "Task Title", "description": "Task Description", "dueDate": "YYYY-MM-DD" }`
- **GET a single task by ID**: `GET http://localhost:5000/api/tasks/:id`
- **PUT update a task by ID**: `PUT http://localhost:5000/api/tasks/:id`
  - Body: `{ "title": "Updated Title", "description": "Updated Description", "dueDate": "YYYY-MM-DD" }`
- **DELETE a task by ID**: `DELETE http://localhost:5000/api/tasks/:id`

#### Additional Notes
- Ensure MongoDB is configured correctly and running before starting the application.
- Adjust MongoDB connection settings in `.env` file if necessary.
