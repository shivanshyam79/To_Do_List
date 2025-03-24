# Ex03 To-Do List using JavaScript
## Date: 24/03/2025

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
index.html
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>To-Do List</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>My To-Do List</h1>
    </header>
    <main>
        <div class="container">
            <h2>To-Do List</h2>
            <div class="input-area">
                <input type="text" id="taskInput" placeholder="Enter a task">
                <button id="addTask">Add Task</button>
            </div>
            <ul class="task-list">
                <li>Shyam R - 212223040200 <button class="delete-btn">X</button></li>
                <li>Activity-2 MWAD <button class="delete-btn">X</button></li>
                <li>Assignment-4 WEB <button class="delete-btn">X</button></li>
            </ul>
        </div>
    </main>
    <footer>
        <p>&copy; Shyam R  -  212223040200</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```
style.css
```

body {
    font-family: Arial, sans-serif;
    margin: 0;
    background-color: #f4f4f4;
    color: #333;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

header {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1em 0;
}

main {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
}

.container {
    background-color: #fff;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 400px;
    max-width: 100%;
}

.container h2 {
    text-align: center;
    margin-bottom: 20px;
}

.input-area {
    display: flex;
    margin-bottom: 15px;
}

.input-area input[type="text"] {
    flex: 1;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.input-area button {
    background-color: #4CAF50;
    color: white;
    border: none;
    padding: 10px 15px;
    border-radius: 4px;
    cursor: pointer;
    margin-left: 5px;
}

.task-list {
    list-style: none;
    padding: 0;
}

.task-list li {
    background-color: #f9f9f9;
    padding: 10px;
    border-bottom: 1px solid #eee;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.task-list li:last-child {
    border-bottom: none;
}

.delete-btn {
    background-color: #f44336;
    color: white;
    border: none;
    padding: 5px 10px;
    border-radius: 4px;
    cursor: pointer;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 1em 0;
    margin-top: auto;
}
```
scrpit.js
```
document.addEventListener('DOMContentLoaded', function() {
    const taskInput = document.getElementById('taskInput');
    const addTaskButton = document.getElementById('addTask');
    const taskList = document.querySelector('.task-list');

    addTaskButton.addEventListener('click', function() {
        const taskText = taskInput.value.trim();
        if (taskText !== '') {
            addTaskToList(taskText);
            taskInput.value = '';
        }
    });

    taskInput.addEventListener('keypress', function(event) {
        if (event.key === 'Enter') {
            addTaskButton.click();
        }
    });

    function addTaskToList(taskText) {
        const listItem = document.createElement('li');
        listItem.innerHTML = `
            ${taskText}
            <button class="delete-btn">X</button>
        `;
        taskList.appendChild(listItem);

        const deleteButton = listItem.querySelector('.delete-btn');
        deleteButton.addEventListener('click', function() {
            listItem.remove();
        });
    }
});
```
## OUTPUT
![Screenshot 2025-03-24 152126](https://github.com/user-attachments/assets/709b4be8-1a8f-4683-a92c-4cdaf1593145)


## RESULT
The program for creating To-do list using JavaScript is executed successfully.
