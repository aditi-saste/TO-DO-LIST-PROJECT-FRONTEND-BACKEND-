# To-Do List Application

A simple To-Do List application built with Express.js and vanilla JavaScript. This application allows users to add, edit, delete, and mark tasks as done. Tasks are managed in a LIFO (Last In, First Out) structure.

## Features

- Add tasks with a date and description
- Edit existing tasks
- Delete tasks
- Mark tasks as done
- Search tasks by date

## Technologies Used

- Node.js
- Express.js
- HTML5
- CSS3
- JavaScript (ES6)

## Getting Started

### Prerequisites

Ensure you have the following installed on your machine:

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)

### Installation

1. **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/to-do-list-app.git
    cd to-do-list-app
    ```

2. **Install dependencies:**

    ```bash
    npm install
    ```

3. **Run the application:**

    ```bash
    node server.js
    ```

    By default, the application will be running on `http://localhost:3000`.

## Project Structure

"to-do-list-app/"
"├── public/"
"│ ├── index.html"
"│ ├── style.css"
"│ └── script.js"
"├── server.js"
"├── package.json"
"└── README.md"

**public/**: Contains static files (HTML, CSS, JavaScript)
- **server.js**: Express server setup
- **package.json**: Project metadata and dependencies
- **README.md**: Project documentation

## API Endpoints

### Get All Tasks

- **URL:** `/tasks`
- **Method:** `GET`
- **Response:**
    ```json
    [
        {
            "id": "task-id",
            "date": "2023-12-31",
            "entry": "Task description",
            "done": false
        }
    ]
    ```

### Add a New Task

- **URL:** `/task`
- **Method:** `POST`
- **Body:**
    ```json
    {
        "taskDate": "2023-12-31",
        "taskEntry": "New task"
    }
    ```
- **Response:**
    ```json
    {
        "id": "new-task-id",
        "date": "2023-12-31",
        "entry": "New task",
        "done": false
    }
    ```

### Delete a Task

- **URL:** `/task/:id`
- **Method:** `DELETE`

### Edit a Task

- **URL:** `/task/:id`
- **Method:** `PUT`
- **Body:**
    ```json
    {
        "entry": "Updated task description"
    }
    ```
### Mark Task as Done

- **URL:** `/task/done/:id`
- **Method:** `PUT`
