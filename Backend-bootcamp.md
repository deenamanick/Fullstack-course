# 6-Day Full Stack Development Curriculum

Backend Focus, Beginner Friendly

## Course Promise

By the end of 6 days, students will understand how the web works, build a small backend API, save data in MongoDB, add simple login security, and connect the backend to an AI-generated React frontend.

This course is designed for beginners. Keep every explanation practical, visual, and connected to one small project.

## Teaching Rule

Use this pattern every day:

1. Explain the idea in plain English.
2. Show the data flow.
3. Build one small feature.
4. Run it immediately.
5. Test it with the browser, Thunder Client, or Postman.

Avoid too much theory. Students should type, run, break, fix, and understand.

---

# Day 1: How the Web Works and UI/UX Basics

## Goal / Project Intro

Today we build a simple student profile page called **The Thoughtful Student Page**.

The goal is not just to write HTML. The goal is to understand what a website is, how users reach it, and how good design helps people use it.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Internet | A large network of connected computers |
| IP Address | The number address of a computer, like `142.250.190.78` |
| Domain | A human-friendly name like `google.com` |
| DNS | The phonebook that converts a domain into an IP address |
| Port | A door number on a computer, like `3000` or `443` |
| HTTP | The browser's language for asking for webpages |
| HTTPS | Secure HTTP |
| UI | What the user sees |
| UX | How easy and pleasant the app feels to use |

## How the Data Flows

```text
Student types google.com
        |
        v
Browser asks DNS: "What IP address is this?"
        |
        v
DNS returns an IP address
        |
        v
Browser sends an HTTPS request
        |
        v
Google server sends back HTML, CSS, and JavaScript
        |
        v
Browser displays the page
```

## How to Run

1. Create a folder named `day-1-student-page`.
2. Create two files:
   - `index.html`
   - `style.css`
3. Open `index.html` in the browser.

## The Code

### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Thoughtful Student Page</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Hello, I am Anu</h1>
    <p>A beginner learning how the web works.</p>
  </header>

  <main>
    <section>
      <h2>About Me</h2>
      <p>I enjoy learning technology step by step.</p>
    </section>

    <section>
      <h2>My Learning Goals</h2>
      <ul>
        <li>Understand websites</li>
        <li>Build simple apps</li>
        <li>Create my first backend API</li>
      </ul>
    </section>

    <nav>
      <a href="#contact">Contact Me</a>
    </nav>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: anu@example.com</p>
    </section>
  </main>
</body>
</html>
```

### `style.css`

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background: #f6f8fb;
  color: #1f2937;
  line-height: 1.6;
}

header {
  background: #0f766e;
  color: white;
  padding: 32px;
  text-align: center;
}

main {
  max-width: 760px;
  margin: 24px auto;
  padding: 0 16px;
}

section {
  background: white;
  border: 1px solid #dbe3ea;
  border-radius: 8px;
  padding: 20px;
  margin-bottom: 16px;
}

a {
  color: #0f766e;
  font-weight: bold;
}
```

## Practice

- Change the name.
- Add one more learning goal.
- Change the page color.
- Explain what happens when a browser opens the page.

## Student Checklist

- [ ] I know what an IP address is.
- [ ] I know what DNS does.
- [ ] I know that HTML is structure and CSS is style.
- [ ] I can explain why readable design matters.

---

# Day 2: Client, Server, and Consuming APIs

## Goal / Project Intro

Today we build a **Simple Joke Generator**.

The browser will ask another server for a joke. The server will send data back as JSON.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Client | The browser or app asking for data |
| Server | The computer that sends data back |
| Request | A message asking for something |
| Response | The answer from the server |
| Status Code | A number that explains what happened |
| `200` | Success |
| `404` | Not found |
| `500` | Server error |
| API | A way for apps to talk to each other |
| JSON | A simple data format used by APIs |
| `fetch()` | JavaScript command to call an API |

## How the Data Flows

```text
User clicks "Get Joke"
        |
        v
Browser runs fetch()
        |
        v
Public joke API receives request
        |
        v
API sends JSON response
        |
        v
JavaScript displays the joke on the page
```

## How to Run

1. Create a folder named `day-2-joke-generator`.
2. Create three files:
   - `index.html`
   - `style.css`
   - `script.js`
3. Open `index.html` in the browser.
4. Click the button.

## The Code

### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Joke Generator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <main>
    <h1>Simple Joke Generator</h1>
    <p id="joke">Click the button to load a joke.</p>
    <button id="jokeButton">Get Joke</button>
  </main>

  <script src="script.js"></script>
</body>
</html>
```

### `script.js`

```javascript
const jokeText = document.getElementById("joke");
const jokeButton = document.getElementById("jokeButton");

jokeButton.addEventListener("click", async () => {
  jokeText.textContent = "Loading...";

  const response = await fetch("https://official-joke-api.appspot.com/random_joke");
  const data = await response.json();

  jokeText.textContent = `${data.setup} ${data.punchline}`;
});
```

### `style.css`

```css
body {
  font-family: Arial, sans-serif;
  background: #eef2ff;
  display: grid;
  min-height: 100vh;
  place-items: center;
}

main {
  width: min(90%, 480px);
  background: white;
  border: 1px solid #c7d2fe;
  border-radius: 8px;
  padding: 24px;
  text-align: center;
}

button {
  background: #2563eb;
  border: 0;
  border-radius: 6px;
  color: white;
  cursor: pointer;
  padding: 12px 16px;
}
```

## Practice

- Open DevTools and check the Network tab.
- Find the API request.
- Look at the JSON response.
- Explain the difference between HTML and JSON.

## Student Checklist

- [ ] I can explain client and server.
- [ ] I know what an API is.
- [ ] I can read simple JSON.
- [ ] I used `fetch()` to get data.

---

# Day 3: Building Your Own Server with Express.js

## Goal / Project Intro

Today we build an **In-Memory Task API Server**.

The server will store tasks in a JavaScript array. The data will disappear when the server restarts. That is okay for today.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Node.js | Runs JavaScript outside the browser |
| npm | Tool to install JavaScript packages |
| Express.js | A small framework for building APIs |
| Route | A URL handled by the server |
| `GET` | Read data |
| `POST` | Create data |
| Middleware | Code that runs before the route |
| `app.listen(3000)` | Starts the server on port `3000` |

## How the Data Flows

```text
Thunder Client sends GET /tasks
        |
        v
Express server receives request
        |
        v
Route handler reads tasks array
        |
        v
Server sends JSON response
```

## How to Run

```bash
mkdir day-3-task-api
cd day-3-task-api
npm init -y
npm install express
node server.js
```

Then open:

```text
http://localhost:3000/tasks
```

## The Code

### `server.js`

```javascript
const express = require("express");

const app = express();
const PORT = 3000;

app.use(express.json());

let tasks = [
  { id: 1, title: "Learn Express", completed: false },
  { id: 2, title: "Test an API", completed: false }
];

app.get("/", (req, res) => {
  res.send("Task API is running");
});

app.get("/tasks", (req, res) => {
  res.json(tasks);
});

app.post("/tasks", (req, res) => {
  const newTask = {
    id: Date.now(),
    title: req.body.title,
    completed: false
  };

  tasks.push(newTask);
  res.status(201).json(newTask);
});

app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}`);
});
```

## Test Requests

### Read tasks

```text
GET http://localhost:3000/tasks
```

### Create a task

```text
POST http://localhost:3000/tasks
Content-Type: application/json

{
  "title": "Build my first backend route"
}
```

## Practice

- Add a new route: `GET /health`.
- Return `{ "status": "ok" }`.
- Restart the server and check that array data resets.

## Student Checklist

- [ ] I installed Express.
- [ ] I started a server on port `3000`.
- [ ] I created a `GET` route.
- [ ] I created a `POST` route.

---

# Day 4: Saving Data with MongoDB and Mongoose

## Goal / Project Intro

Today we build a **Database Connector**.

Yesterday's tasks disappeared after restarting the server. Today we save tasks permanently in MongoDB.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Database | A place to store app data |
| SQL | Table-based database style |
| NoSQL | Document-based database style |
| MongoDB | A NoSQL database |
| Collection | A group of documents |
| Document | One saved object |
| Mongoose | A tool that helps Node.js talk to MongoDB |
| Schema | Rules for what the data should look like |
| Model | Code used to create, read, update, and delete data |

## How the Data Flows

```text
Node script starts
        |
        v
Mongoose connects to MongoDB Atlas
        |
        v
Script creates a Task document
        |
        v
MongoDB saves it in the tasks collection
        |
        v
Script reads tasks back and prints them
```

## How to Run

```bash
mkdir day-4-database-connector
cd day-4-database-connector
npm init -y
npm install mongoose dotenv
node seed.js
```

Create a `.env` file:

```text
MONGO_URL=your_mongodb_atlas_connection_string
```

## The Code

### `Task.js`

```javascript
const mongoose = require("mongoose");

const taskSchema = new mongoose.Schema({
  title: {
    type: String,
    required: true
  },
  completed: {
    type: Boolean,
    default: false
  }
});

module.exports = mongoose.model("Task", taskSchema);
```

### `seed.js`

```javascript
require("dotenv").config();
const mongoose = require("mongoose");
const Task = require("./Task");

async function run() {
  await mongoose.connect(process.env.MONGO_URL);
  console.log("Connected to MongoDB");

  await Task.create({
    title: "Save my first task in MongoDB"
  });

  const tasks = await Task.find();
  console.log(tasks);

  await mongoose.disconnect();
}

run();
```

## Practice

- Add another task.
- Change `completed` to `true`.
- View the saved data in MongoDB Atlas.

## Student Checklist

- [ ] I know why databases are needed.
- [ ] I created a MongoDB Atlas database.
- [ ] I connected Node.js to MongoDB.
- [ ] I created and read data using Mongoose.

---

# Day 5: Full CRUD API and Security Basics

## Goal / Project Intro

Today we build a **Secured REST API**.

We connect Express to MongoDB and add:

- Create task
- Read tasks
- Update task
- Delete task
- Register user
- Login user
- Protect routes with a token

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| CRUD | Create, Read, Update, Delete |
| bcrypt | Tool to hash passwords |
| Hashing | Turning a password into a safe stored value |
| JWT | A signed token used after login |
| Protected route | A route that needs a valid token |
| Authorization header | Where the browser sends the token |

## How the Data Flows

```text
User logs in
        |
        v
Server checks email and password
        |
        v
Server returns JWT token
        |
        v
Client sends token with task requests
        |
        v
Server verifies token before allowing access
```

## How to Run

```bash
mkdir day-5-secured-api
cd day-5-secured-api
npm init -y
npm install express mongoose dotenv bcryptjs jsonwebtoken
node server.js
```

Create a `.env` file:

```text
MONGO_URL=your_mongodb_atlas_connection_string
JWT_SECRET=change_this_secret
```

## The Code

### `server.js`

```javascript
require("dotenv").config();
const express = require("express");
const mongoose = require("mongoose");
const bcrypt = require("bcryptjs");
const jwt = require("jsonwebtoken");

const app = express();
app.use(express.json());

const userSchema = new mongoose.Schema({
  email: { type: String, required: true, unique: true },
  passwordHash: { type: String, required: true }
});

const taskSchema = new mongoose.Schema({
  title: { type: String, required: true },
  completed: { type: Boolean, default: false },
  userId: { type: mongoose.Schema.Types.ObjectId, required: true }
});

const User = mongoose.model("User", userSchema);
const Task = mongoose.model("Task", taskSchema);

function authRequired(req, res, next) {
  const authHeader = req.headers.authorization;

  if (!authHeader) {
    return res.status(401).json({ message: "Token required" });
  }

  const token = authHeader.replace("Bearer ", "");
  const payload = jwt.verify(token, process.env.JWT_SECRET);

  req.userId = payload.userId;
  next();
}

app.post("/register", async (req, res) => {
  const passwordHash = await bcrypt.hash(req.body.password, 10);

  const user = await User.create({
    email: req.body.email,
    passwordHash
  });

  res.status(201).json({ id: user._id, email: user.email });
});

app.post("/login", async (req, res) => {
  const user = await User.findOne({ email: req.body.email });

  if (!user) {
    return res.status(401).json({ message: "Invalid login" });
  }

  const passwordOk = await bcrypt.compare(req.body.password, user.passwordHash);

  if (!passwordOk) {
    return res.status(401).json({ message: "Invalid login" });
  }

  const token = jwt.sign({ userId: user._id }, process.env.JWT_SECRET);
  res.json({ token });
});

app.get("/tasks", authRequired, async (req, res) => {
  const tasks = await Task.find({ userId: req.userId });
  res.json(tasks);
});

app.post("/tasks", authRequired, async (req, res) => {
  const task = await Task.create({
    title: req.body.title,
    userId: req.userId
  });

  res.status(201).json(task);
});

app.patch("/tasks/:id", authRequired, async (req, res) => {
  const task = await Task.findOneAndUpdate(
    { _id: req.params.id, userId: req.userId },
    req.body,
    { new: true }
  );

  if (!task) {
    return res.status(404).json({ message: "Task not found" });
  }

  res.json(task);
});

app.delete("/tasks/:id", authRequired, async (req, res) => {
  await Task.findOneAndDelete({ _id: req.params.id, userId: req.userId });
  res.status(204).send();
});

async function start() {
  await mongoose.connect(process.env.MONGO_URL);
  app.listen(3000, () => {
    console.log("API running at http://localhost:3000");
  });
}

start();
```

## Test Requests

### Register

```text
POST http://localhost:3000/register
Content-Type: application/json

{
  "email": "student@example.com",
  "password": "password123"
}
```

### Login

```text
POST http://localhost:3000/login
Content-Type: application/json

{
  "email": "student@example.com",
  "password": "password123"
}
```

### Create task with token

```text
POST http://localhost:3000/tasks
Authorization: Bearer paste_token_here
Content-Type: application/json

{
  "title": "Build a secure API"
}
```

## Practice

- Try calling `/tasks` without a token.
- Try logging in with the wrong password.
- Create two users and confirm each user sees only their own tasks.

## Student Checklist

- [ ] I understand CRUD.
- [ ] I hashed a password with bcrypt.
- [ ] I created a JWT after login.
- [ ] I protected task routes.
- [ ] I made sure users can only access their own tasks.

---

# Day 6: Capstone - AI-Assisted Full Stack Product

## Goal / Project Intro

Today students turn the backend into a simple full stack product.

Project idea: **Task Dashboard**

The backend is the secure API from Day 5. The frontend is generated with Lovable, then connected to the local API.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Full stack | Frontend and backend working together |
| React | A frontend library for building UI |
| AI UI builder | A tool that creates frontend code from prompts |
| Prompt | Instructions given to an AI tool |
| Integration | Connecting two parts of an app |
| Environment variable | A setting such as the API URL |

## How the Data Flows

```text
User uses React dashboard
        |
        v
Frontend sends login request
        |
        v
Backend returns token
        |
        v
Frontend stores token
        |
        v
Frontend sends task requests with token
        |
        v
Backend reads and writes MongoDB data
        |
        v
Frontend shows updated tasks
```

## Step 1: Review the Backend

Students should confirm:

- `/register` works.
- `/login` returns a token.
- `/tasks` requires a token.
- Users only see their own tasks.

## Step 2: Lovable Prompt

Copy this into Lovable:

```text
Build a simple React task dashboard for beginner students.

Pages:
- Login page
- Register page
- Dashboard page

Dashboard features:
- Show a list of tasks
- Add a new task
- Mark a task complete
- Delete a task
- Show loading and error states

API integration:
- POST /register with email and password
- POST /login with email and password
- Store the returned token
- Send Authorization: Bearer token for all /tasks requests
- GET /tasks
- POST /tasks
- PATCH /tasks/:id
- DELETE /tasks/:id

Design:
- Clean and simple
- Easy for beginners to understand
- No complex animations
- Mobile friendly
```

## Step 3: Connect the Frontend to the Backend

In the frontend project, use one API base URL:

```javascript
const API_URL = "http://localhost:3000";
```

Example login call:

```javascript
async function login(email, password) {
  const response = await fetch(`${API_URL}/login`, {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({ email, password })
  });

  const data = await response.json();
  localStorage.setItem("token", data.token);
}
```

Example protected task call:

```javascript
async function getTasks() {
  const token = localStorage.getItem("token");

  const response = await fetch(`${API_URL}/tasks`, {
    headers: {
      Authorization: `Bearer ${token}`
    }
  });

  return response.json();
}
```

## Step 4: Final Demo

Each student should show:

1. Register a new account.
2. Log in.
3. Create a task.
4. Mark the task complete.
5. Delete the task.
6. Log out.

## Student Checklist

- [ ] I connected a React frontend to my backend.
- [ ] I used a token after login.
- [ ] I can create, read, update, and delete tasks from the UI.
- [ ] I can explain the full data flow.

---

# Final Course Outcome

At the end of the course, students should be able to explain this sentence:

```text
The browser sends requests to my Express API, my API checks the user, saves or reads data from MongoDB, and sends JSON back to the frontend.
```

That one sentence is the heart of beginner full stack development.

# Instructor Notes

- Keep examples small.
- Do not teach every possible option.
- Repeat request, response, route, JSON, and database many times.
- Let students see errors early.
- Use Thunder Client or Postman every day from Day 3 onward.
- Use simple names like `Task`, `User`, `title`, and `completed`.
- Save advanced topics like refresh tokens, deployment, TypeScript, Docker, and testing for the next course.
