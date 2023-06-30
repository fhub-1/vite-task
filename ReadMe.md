# Task Management App

This is a Task Management App built using React, TypeScript, and TailwindCSS. It allows users to create, edit, and manage tasks, helping them stay organized and boost productivity.

## Features

- Create new tasks by providing a title, description, due date, and priority.
- Edit existing tasks to update their details.
- Display a list of tasks with their respective information.
- Delete tasks that are no longer needed.

## Tech Stack

- React: A JavaScript library for building user interfaces.
- TypeScript: A typed superset of JavaScript that provides static typing.
- TailwindCSS: A utility-first CSS framework for designing responsive and customizable UI components.

## Project Structure

- `src/App.tsx`: The main entry point of the application. It renders the task management interface and handles the state of tasks.
- `src/components/Form.tsx`: A reusable form component for creating and editing tasks.
- `src/types.ts`: Contains TypeScript type definitions used in the project.

## Getting Started

To run the project locally, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/task-management-app.git`
2. Navigate to the project directory: `cd task-management-app`
3. Install dependencies: `npm install`
4. Start the development server: `npm start`
5. Open your browser and visit: `http://localhost:3000`

## App.tsx

The `App.tsx` file is the main entry point of the application. It renders the task management interface and handles the state of tasks. Here's a breakdown of its key components:

- `import React, { useState } from "react";`: Imports the necessary modules and hooks from React.
- `import Form from "./Form";`: Imports the `Form` component used for creating and editing tasks.
- `interface Task { ... }`: Defines the `Task` interface to represent the structure of a task object.
- `const App: React.FC = () => { ... }`: Defines the main component of the application.
- `const [tasks, setTasks] = useState<Task[]>([]);`: Uses the `useState` hook to manage the state of tasks.
- `const handleTaskSubmit = (...) => { ... }`: Handles the submission of tasks, allowing for creation or editing of tasks based on the `editTask` state.
- `const handleEditTask = (...) => { ... }`: Handles the editing of a specific task.
- `const handleDeleteTask = (...) => { ... }`: Handles the deletion of a task.
- The `return` statement renders the task management interface with conditional rendering based on the `editTask` state and a list of tasks.

## Form.tsx

The `Form.tsx` file is a reusable form component for creating and editing tasks. Here's a breakdown of its key components:

- `import React, { useState, useEffect } from "react";`: Imports the necessary modules and hooks from React.
- `interface TaskFormProps { ... }`: Defines the props interface for the `TaskForm` component.
- `const TaskForm: React.FC<TaskFormProps> = ({ ... }) => { ... }`: Defines the main component of the form.
- `const [title, setTitle] = useState(initialTitle);`: Uses the `useState` hook to manage the state of the title input field.
- `const [description, setDescription] = useState(initialDescription);`: Uses the `useState` hook to manage the state of the description input field.
- `const [dueDate, setDueDate] = useState(initialDueDate);`: Uses the `useState` hook to manage the state of the due date input field.
- `const [priority, setPriority] = useState(initialPriority);`: Uses the `useState` hook to manage the state of the priority select field.
- `useEffect(() => { ... }, [initialTitle, initialDescription, initialDueDate, initialPriority]);`: Sets the initial values for the form fields when the component mounts or when the initial values change.
- `const handleSubmit = (e: React.FormEvent) => { ... }`: Handles the form submission, calling the `onSubmit` function with the input values and resetting the form fields.
- The `return` statement renders the form with input fields for title, description, due date, and priority, along with a submit button.


Feel free to explore the code and make any necessary modifications to suit your requirements.

## Contributing

Contributions are welcome! If you have any ideas for improvements or bug fixes, please submit a pull request. Make sure to follow the existing coding style and add appropriate tests.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
