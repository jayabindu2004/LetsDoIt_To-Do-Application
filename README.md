# LetsDoIt_To-Do-Application
A full-stack to-do list application built with Node.js, Express.js, and PostgreSQL, featuring a dynamic and responsive user interface. The application allows users to add, edit, and delete tasks, with all data stored persistently in a PostgreSQL database.

## Features
**Add New Task**: Users can add new tasks to the list.<br>
**Edit Task**: Users can edit the title of existing tasks directly within the list.<br>
**Delete Task**: Users can delete tasks by checking a checkbox next to each item.<br>
**Persistent Storage**: Tasks are stored in a PostgreSQL database, ensuring data is preserved across sessions.<br>

## Technologies Used
**Backend**: Node.js, Express.js, PostgreSQL, pg (node-postgres)<br>
**Frontend**: HTML5, CSS3, JavaScript, EJS (Embedded JavaScript Templates)<br>
**Tools and Libraries**: Body-Parser, Path, URL<br>

## Installation
### Clone the repository:
```
git clone https://github.com/jayabindu2004/LetsDoIt_To-Do-Application.git
```
### Navigate to the project directory:
```
cd todo-list-app
```
### Install dependencies:
```
npm install
```
### Set up the PostgreSQL database using pgAdmin:

* Open pgAdmin and connect to your PostgreSQL server.
* Create a new database named to-do-list:
** Right-click on the Databases section and select Create > Database....
* Name the database to-do-list and click Save.
* Create a table named items:
** Open the Query Tool in pgAdmin.
** Run the following SQL query:
```
CREATE TABLE items (
    id SERIAL PRIMARY KEY,
    title VARCHAR(255) NOT NULL
);
```
* Configure database connection in index.js:
```
const db = new pg.Client({
  user: "postgres",
  host: "localhost",
  database: "to-do-list",
  password: "your-password",
  port: 5432,
});
```
## Start the application:
```
npm start
```
Open your browser and navigate to http://localhost:3000 to see the application in action.

## Usage
* **Add Task**: Enter a task in the input field and click the "+" button.<br>
* **Edit Task**: Click the pencil icon next to a task, modify the text, and click the check icon to save changes.<br>
* **Delete Task**: Check the checkbox next to a task to delete it.<br>
