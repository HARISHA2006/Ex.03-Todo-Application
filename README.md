# Ex03 To-Do List using JavaScript
## Date:03.10.2025

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

# Index.html

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Stylish To-Do App</title>
  <link rel="stylesheet" href="index.css">
</head>
<body>
  <div class="todo-container">
    <h1>✨ My Tasks ✨</h1>
    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Add a new task...">
      <button onclick="addTask()">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>

  <script src="index.js"></script>
</body>
</html>


```
# Index.js
````
function addTask() {
  const input = document.getElementById("taskInput");
  const taskText = input.value.trim();
  if (!taskText) return;

  const li = document.createElement("li");
  li.innerHTML = `
    <span onclick="toggleComplete(this)">${taskText}</span>
    <button onclick="deleteTask(this)">Delete</button>
  `;
  document.getElementById("taskList").appendChild(li);
  input.value = "";
}

function deleteTask(button) {
  button.parentElement.remove();
}

function toggleComplete(span) {
  span.parentElement.classList.toggle("completed");
}

  

````
# Index.css
```
/* Background & container */
body {
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #89f7fe, #66a6ff);
  display: flex;
  justify-content: center;
  align-items: flex-start;
  min-height: 100vh;
  padding-top: 60px;
}

.todo-container {
  background: rgba(255, 255, 255, 0.15);
  backdrop-filter: blur(15px);
  padding: 30px;
  border-radius: 20px;
  width: 90%;
  max-width: 450px;
  box-shadow: 0 8px 32px rgba(0,0,0,0.2);
  border: 1px solid rgba(255, 255, 255, 0.3);
}

/* Header */
h1 {
  text-align: center;
  margin-bottom: 25px;
  color: #fff;
  text-shadow: 1px 1px 5px rgba(0,0,0,0.2);
}

/* Input section */
.input-section {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

input[type="text"] {
  flex: 1;
  padding: 12px;
  border-radius: 10px;
  border: none;
  outline: none;
  font-size: 16px;
  box-shadow: inset 0 0 6px rgba(0,0,0,0.1);
}

button {
  padding: 12px 20px;
  border-radius: 10px;
  border: none;
  cursor: pointer;
  font-weight: bold;
  background: linear-gradient(45deg, #ff6ec4, #7873f5);
  color: white;
  transition: transform 0.2s, box-shadow 0.2s;
}

button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 15px rgba(0,0,0,0.2);
}

/* Task list */
ul {
  list-style: none;
  padding: 0;
}

li {
  background: rgba(255,255,255,0.25);
  backdrop-filter: blur(5px);
  margin-bottom: 12px;
  padding: 12px;
  border-radius: 15px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #222; /* Dark font for task text */
  font-weight: 500;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  transition: transform 0.1s;
}

li:hover {
  transform: scale(1.02);
}

li.completed {
  text-decoration: line-through;
  color: #777; /* Gray for completed tasks */
}

li button {
  background: #ff4b5c;
  padding: 6px 12px;
  border-radius: 10px;
  font-weight: bold;
  border: none;
  cursor: pointer;
  transition: background 0.2s, transform 0.2s;
}

li button:hover {
  background: #ff1e2e;
  transform: scale(1.05);
}


```

## OUTPUT


<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/f707cba6-eb47-4a71-aa49-cdb669aeca6a" />

<img width="1919" height="1078" alt="image" src="https://github.com/user-attachments/assets/4df93fb8-b2c0-493c-af19-228e5f116854" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.
