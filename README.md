# Framework-of-SocialMedia
Creating a basic social media site with task assignment functionality is a complex project that involves front-end and back-end development. 

**Front-end (HTML, CSS, JavaScript)**

Below is a basic structure for the social media site's front-end:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Social Media Site</title>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
<body>
    <header>
        <h1>Social Media Site</h1>
    </header>
    <div class="content">
        <div class="users">
            <h2>Users</h2>
            <ul id="user-list">
                <!-- User list will be dynamically populated -->
            </ul>
        </div>
        <div class="chat">
            <h2>Chat</h2>
            <div id="chat-messages">
                <!-- Chat messages will be displayed here -->
            </div>
            <input type="text" id="message-input" placeholder="Type your message">
            <button id="send-button">Send</button>
        </div>
        <div class="tasks">
            <h2>Tasks</h2>
            <ul id="task-list">
                <!-- Task list will be dynamically populated -->
            </ul>
            <input type="text" id="task-input" placeholder="Assign a task">
            <button id="assign-task-button">Assign Task</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```

Next, I created the CSS (styles.css) to style the page. We can customize the styles to our liking.

The JavaScript (script.js) is used to handle user interactions:

```javascript
// Front-end JavaScript
document.addEventListener("DOMContentLoaded", function() {
    const userList = document.getElementById("user-list");
    const chatMessages = document.getElementById("chat-messages");
    const messageInput = document.getElementById("message-input");
    const sendButton = document.getElementById("send-button");
    const taskList = document.getElementById("task-list");
    const taskInput = document.getElementById("task-input");
    const assignTaskButton = document.getElementById("assign-task-button");

    // Function to send a chat message
    function sendMessage() {
        const message = messageInput.value;
        if (message.trim() !== "") {
            // Send the message to the server (not shown in this example).
            // Append the message to the chatMessages element for display.
            chatMessages.innerHTML += `<div class="message">You: ${message}</div>`;
            messageInput.value = "";
        }
    }

    sendButton.addEventListener("click", sendMessage);

    // Function to assign a task
    function assignTask() {
        const task = taskInput.value;
        if (task.trim() !== "") {
            // Send the task to the server (not shown in this example).
            // Append the task to the taskList element for display.
            taskList.innerHTML += `<li>${task}</li>`;
            taskInput.value = "";
        }
    }

    assignTaskButton.addEventListener("click", assignTask);

    // You'll need additional code to fetch and display users, messages, and tasks dynamically.
});
```

**Back-end (Node.js with Express.js)**

For the back-end, you would set up a server using Node.js and Express.js to handle user data, messages, and tasks. We will need to implement endpoints for fetching and sending this data, handle user authentication, and more.
