# 6-Day Full Stack Development Curriculum

Backend Focus, Beginner Friendly

## Course Promise

By the end of 6 days, students will understand how the web works, build a small backend API, save data in MongoDB, add simple login security, and connect the backend to an AI-generated React frontend.

This course is designed for beginners. Keep every explanation practical, visual, and connected to one small project.

## 3-Day Node.js Learning Path

Days 3, 4, and 5 are the backend core of this course.

| Day | Node.js Level | What Students Learn |
| --- | --- | --- |
| Day 3 | Basic Node.js | Runtime, terminal, npm, modules, simple scripts, first HTTP server, first Express routes |
| Day 4 | Intermediate Node.js | Express routing, middleware, REST APIs, request body, route params, MongoDB, Mongoose |
| Day 5 | Advanced Beginner Node.js | Full CRUD, auth, password hashing, JWT, protected routes, ownership checks, safer error handling |

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

## 8-Hour Practical Plan

| Time | Activity |
| --- | --- |
| 09:30 - 10:00 | Icebreaker: What happens when we open a website? |
| 10:00 - 10:45 | Practicals 1 and 2 |
| 10:45 - 11:00 | Break |
| 11:00 - 12:15 | Practicals 3 and 4 |
| 12:15 - 01:00 | Practical 5 |
| 01:00 - 02:00 | Lunch |
| 02:00 - 03:15 | Practicals 6 and 7 |
| 03:15 - 03:30 | Break |
| 03:30 - 04:45 | Practicals 8 and 9 |
| 04:45 - 05:30 | Practical 10 and student demo |

## Day 1 Practicals

### Practical 1: Find the IP Address

Students learn that websites live on computers with addresses.

Steps:

1. Open Terminal or Command Prompt.
2. Run:

```bash
ping google.com
```

3. Write down the IP address shown.
4. Discuss: Did we type the IP address or the domain name?

Expected learning:

- `google.com` is easy for humans.
- The computer still needs an IP address.

### Practical 2: DNS Lookup

Students see DNS as the phonebook of the internet.

Steps:

1. Run:

```bash
nslookup google.com
```

2. Identify:
   - Domain name
   - IP address
   - DNS server

Expected learning:

- DNS converts a domain name into an IP address.

### Practical 3: Visit a Website and Inspect Network Requests

Students see that one webpage can load many files.

Steps:

1. Open Chrome.
2. Open DevTools.
3. Go to the Network tab.
4. Visit:

```text
https://example.com
```

5. Refresh the page.
6. Notice the request status code.

Expected learning:

- The browser sends requests.
- The server sends responses.
- `200` means success.

### Practical 4: HTTP vs HTTPS

Students understand why secure websites matter.

Steps:

1. Open a website with `https://`.
2. Click the lock icon in the browser address bar.
3. Discuss what "secure connection" means.
4. Compare:

```text
http://example.com
https://example.com
```

Expected learning:

- HTTPS protects data while it travels.
- Login pages and payment pages must use HTTPS.

### Practical 5: Create the First HTML Page

Students create the first version of the student profile page.

Steps:

1. Create a folder named `day-1-student-page`.
2. Create `index.html`.
3. Add this small starter code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My First Page</title>
</head>
<body>
  <h1>Hello, I am Anu</h1>
  <p>I am learning how websites work.</p>
</body>
</html>
```

4. Open it in the browser.

Expected learning:

- HTML gives structure to the page.
- The browser reads HTML and displays content.

### Practical 6: Add Meaningful Page Sections

Students improve the page with real content.

Steps:

1. Add an About section.
2. Add a Learning Goals section.
3. Add a Contact section.
4. Use these tags:

```html
<header>
<main>
<section>
<h1>
<h2>
<p>
<ul>
<li>
```

Expected learning:

- Good HTML is organized.
- Sections make content easier to understand.

### Practical 7: Link CSS to HTML

Students learn that HTML and CSS should be separate.

Steps:

1. Create `style.css`.
2. Link it inside `index.html`:

```html
<link rel="stylesheet" href="style.css">
```

3. Add simple body styles:

```css
body {
  font-family: Arial, sans-serif;
  background: #f6f8fb;
  color: #1f2937;
}
```

Expected learning:

- HTML is content.
- CSS is design.
- Professional projects separate structure and style.

### Practical 8: Improve Readability and UX

Students apply simple UX rules.

Steps:

1. Add spacing using `padding` and `margin`.
2. Limit content width using `max-width`.
3. Add readable line height.
4. Add card-like sections.

Use:

```css
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
```

Expected learning:

- UX is not decoration.
- UX means making the page easy to read and use.

### Practical 9: Add Navigation

Students learn basic page navigation.

Steps:

1. Add a navigation link:

```html
<nav>
  <a href="#about">About</a>
  <a href="#goals">Goals</a>
  <a href="#contact">Contact</a>
</nav>
```

2. Add matching `id` values:

```html
<section id="about">
<section id="goals">
<section id="contact">
```

3. Click each link and test it.

Expected learning:

- Links help users move around.
- Clear navigation improves UX.

### Practical 10: Final Student Page Demo

Students complete and present their page.

Requirements:

- Page has student name.
- Page has About, Goals, and Contact sections.
- Page uses a simple color palette.
- Page has readable spacing.
- Page has working navigation links.
- Student can explain how the browser loads the page.

Demo questions:

1. What is the difference between domain and IP address?
2. What does DNS do?
3. What does HTML do?
4. What does CSS do?
5. What UX improvement did you add?

## Student Checklist

- [ ] I know what an IP address is.
- [ ] I know what DNS does.
- [ ] I know that HTML is structure and CSS is style.
- [ ] I can explain why readable design matters.
- [ ] I completed 10 Day 1 practicals.
- [ ] I presented my final student page.

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
| Variable | A named box that stores data |
| Function | A reusable block of code |
| Event | Something the user does, like clicking a button |
| Array | A list of values |
| Object | Data stored as key-value pairs |
| DOM | JavaScript's way to find and change HTML elements |
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

## Mini Module: JavaScript Basics for Beginners

Before students call an API, they must understand the small JavaScript ideas used in the browser and later in Node.js.

Keep this module practical. Do not teach advanced JavaScript yet.

### JavaScript Basics Data Flow

```text
User clicks a button
        |
        v
JavaScript hears the click event
        |
        v
JavaScript runs a function
        |
        v
JavaScript changes the HTML page
```

### JavaScript Concepts Students Need

| Concept | Simple Meaning | Example |
| --- | --- | --- |
| `let` | Variable that can change | `let count = 0;` |
| `const` | Variable that should not be reassigned | `const name = "Anu";` |
| String | Text data | `"Hello"` |
| Number | Numeric data | `25` |
| Boolean | `true` or `false` | `isLoggedIn = false` |
| Function | Reusable action | `function sayHello() {}` |
| Array | List of values | `["HTML", "CSS", "JS"]` |
| Object | One item with properties | `{ name: "Anu", age: 20 }` |
| DOM | HTML page controlled by JavaScript | `document.getElementById()` |
| Event Listener | Runs code when something happens | `button.addEventListener()` |
| `async` / `await` | Waits for slow work, like API calls | `await fetch(url)` |

## JavaScript Practical 1: Variables and Output

Goal: Store simple data and print it.

Create a file named `basics.js` and run it in the browser console or with Node.js.

```javascript
const studentName = "Anu";
let age = 20;
let isLearningBackend = true;

console.log(studentName);
console.log(age);
console.log(isLearningBackend);
```

Expected learning:

- Variables store data.
- `console.log()` helps us see output while learning.

## JavaScript Practical 2: Functions

Goal: Create reusable code.

```javascript
function greetStudent(name) {
  return `Hello, ${name}. Welcome to backend development.`;
}

const message = greetStudent("Anu");
console.log(message);
```

Expected learning:

- A function takes input.
- A function can return output.

## JavaScript Practical 3: Arrays

Goal: Store a list of learning topics.

```javascript
const topics = ["HTML", "CSS", "JavaScript", "APIs"];

console.log(topics[0]);
console.log(topics[1]);
console.log(topics.length);
```

Expected learning:

- Arrays start counting from `0`.
- Arrays are useful for lists like tasks, users, and posts.

## JavaScript Practical 4: Objects

Goal: Store one real-world item.

```javascript
const student = {
  name: "Anu",
  course: "Full Stack Development",
  completedDay1: true
};

console.log(student.name);
console.log(student.course);
console.log(student.completedDay1);
```

Expected learning:

- Objects store related details together.
- JSON looks very similar to JavaScript objects.

## JavaScript Practical 5: Button Click Event

Goal: Make the page interactive.

Add this to `index.html`:

```html
<p id="message">Click the button to start.</p>
<button id="startButton">Start</button>
```

Add this to `script.js`:

```javascript
const message = document.getElementById("message");
const startButton = document.getElementById("startButton");

startButton.addEventListener("click", () => {
  message.textContent = "JavaScript is working.";
});
```

Expected learning:

- JavaScript can find HTML elements.
- JavaScript can react to user actions.
- JavaScript can update the page without reloading.

## JavaScript Practical 6: Mini Counter App

Goal: Practice variables, events, and DOM updates together.

Add this to `index.html`:

```html
<h2>Counter: <span id="count">0</span></h2>
<button id="plusButton">Add One</button>
```

Add this to `script.js`:

```javascript
let count = 0;

const countText = document.getElementById("count");
const plusButton = document.getElementById("plusButton");

plusButton.addEventListener("click", () => {
  count = count + 1;
  countText.textContent = count;
});
```

Expected learning:

- `let` is used when a value changes.
- UI can change based on JavaScript data.

## JavaScript Practical 7: JSON Preview

Goal: Understand the shape of API data before using `fetch()`.

```javascript
const joke = {
  setup: "Why did the developer go broke?",
  punchline: "Because they used up all their cache."
};

console.log(joke.setup);
console.log(joke.punchline);
```

Expected learning:

- API responses often come as JSON.
- JSON data is read using property names.

## JavaScript Readiness Checklist

- [ ] I can create `let` and `const` variables.
- [ ] I can write a simple function.
- [ ] I can use an array.
- [ ] I can use an object.
- [ ] I can select an HTML element with JavaScript.
- [ ] I can run code when a button is clicked.
- [ ] I understand that API data looks like objects and arrays.

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
- [ ] I understand JavaScript variables, functions, arrays, and objects.
- [ ] I can use a button click event.
- [ ] I can change text on a page using JavaScript.
- [ ] I know what an API is.
- [ ] I can read simple JSON.
- [ ] I used `fetch()` to get data.

---

# Day 3: Node.js Basics and Your First Server

## Node.js Level

Basic Node.js.

Today students learn what Node.js is, how to run JavaScript outside the browser, how npm works, and how a server starts listening on a port.

## What are Node.js and Express.js?

Before building our Express server, students must understand the tools we are using:

- **Node.js**: Normally, JavaScript only runs *inside* a web browser (like Chrome or Safari) to make web pages interactive. **Node.js** is a special runtime environment that allows JavaScript to run directly *on your computer* or *on a server*. This means you can use JavaScript to read files, connect to databases, and act as a backend.
- **Express.js**: Writing a web server from scratch in pure Node.js can be complicated and repetitive. **Express.js** is a "framework" (a pre-written library of code) that makes building web servers and APIs incredibly simple. It handles routing and HTTP requests easily.

## Goal / Project Intro

Today we build an **In-Memory Task API Server**.

The server will store tasks in a JavaScript array. The data will disappear when the server restarts. That is okay for today.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Node.js | Runs JavaScript outside the browser |
| Runtime | A place where code can run |
| Terminal | The place where we type commands |
| npm | Tool to install JavaScript packages |
| `package.json` | Project information and dependency list |
| Module | A reusable file or package |
| `require()` | Imports code from another file or package |
| HTTP Server | A program that receives web requests and sends responses |
| Express.js | A small framework for building APIs |
| Route | A URL handled by the server |
| `GET` | Read data |
| `POST` | Create data |
| Middleware | Code that runs before the route |
| `app.listen(3000)` | Starts the server on port `3000` |

## 8-Hour Practical Plan

| Time | Activity |
| --- | --- |
| 09:30 - 10:00 | Recap JavaScript and explain Node.js |
| 10:00 - 10:45 | Practicals 1 and 2 |
| 10:45 - 11:00 | Break |
| 11:00 - 12:15 | Practicals 3 and 4 |
| 12:15 - 01:00 | Practical 5 |
| 01:00 - 02:00 | Lunch |
| 02:00 - 03:15 | Practicals 6 and 7 |
| 03:15 - 03:30 | Break |
| 03:30 - 04:45 | Practical 8 |
| 04:45 - 05:30 | API testing and recap |

## Node.js Practicals

### Practical 1: Check Node.js and npm

Goal: Confirm the tools are installed.

```bash
node -v
npm -v
```

Expected learning:

- `node` runs JavaScript.
- `npm` installs packages.

### Practical 2: Run a JavaScript File with Node

Create `hello-node.js`:

```javascript
const studentName = "Anu";

console.log("Hello from Node.js");
console.log(`Student: ${studentName}`);
```

Run:

```bash
node hello-node.js
```

Expected learning:

- JavaScript can run outside the browser.
- Backend code usually runs with Node.js.

### Practical 3: Use Functions in Node.js

Create `calculator.js`:

```javascript
function add(a, b) {
  return a + b;
}

function multiply(a, b) {
  return a * b;
}

console.log(add(10, 5));
console.log(multiply(10, 5));
```

Run:

```bash
node calculator.js
```

Expected learning:

- Backend code is still JavaScript.
- Functions help us organize logic.

### Practical 4: Create a Simple Module

Create `math.js`:

```javascript
function add(a, b) {
  return a + b;
}

module.exports = { add };
```

Create `app.js`:

```javascript
const math = require("./math");

console.log(math.add(2, 3));
```

Run:

```bash
node app.js
```

Expected learning:

- Large backend apps are split into files.
- `module.exports` shares code.
- `require()` imports code.

### Practical 5: Create `package.json`

Goal: Start a real Node.js project.

```bash
mkdir day-3-task-api
cd day-3-task-api
npm init -y
```

Open `package.json` and identify:

- Project name
- Version
- Scripts
- Dependencies

Expected learning:

- `package.json` describes the Node.js project.

### Practical 6: Install and Use a Package

Install Express:

```bash
npm install express
```

Expected learning:

- Packages are reusable code written by other developers.
- Installed packages appear in `dependencies`.

### Practical 7: Build a Tiny Node HTTP Server

Create `basic-server.js`:

```javascript
const http = require("http");

const server = http.createServer((req, res) => {
  res.writeHead(200, { "Content-Type": "text/plain" });
  res.end("Hello from a basic Node.js server");
});

server.listen(3000, () => {
  console.log("Server running at http://localhost:3000");
});
```

Run:

```bash
node basic-server.js
```

Open:

```text
http://localhost:3000
```

Expected learning:

- A server waits for requests.
- `3000` is the port.
- Express makes server code easier.

### Practical 8: Build the Express Task API

Goal: Build the main Day 3 project using Express.

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

If you already created `day-3-task-api` in Practical 5, stay inside that folder and continue from `npm install express`.

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

- [ ] I can run JavaScript using `node`.
- [ ] I understand what npm does.
- [ ] I created a `package.json` file.
- [ ] I imported code using `require()`.
- [ ] I built a tiny Node HTTP server.
- [ ] I installed Express.
- [ ] I started a server on port `3000`.
- [ ] I created a `GET` route.
- [ ] I created a `POST` route.

---

# Day 4: Intermediate Node.js, Express APIs, and MongoDB

## Node.js Level

Intermediate Node.js.

Today students improve the Day 3 API and learn how real backend apps receive input, use middleware, organize data, and save records in MongoDB.

## Goal / Project Intro

Today we build a **Database Connector**.

Yesterday's tasks disappeared after restarting the server. Today we save tasks permanently in MongoDB.

## Concepts Introduced

| Term | Simple Meaning |
| --- | --- |
| Database | A place to store app data |
| REST API | A predictable API style using resources and HTTP methods |
| Route Param | A URL value like `/tasks/:id` |
| Query Param | Extra URL data like `/tasks?completed=true` |
| Request Body | Data sent by the client in `POST` or `PATCH` |
| Environment Variable | Secret or setting stored outside the code |
| `dotenv` | Package that loads `.env` values |
| SQL | Table-based database style |
| NoSQL | Document-based database style |
| MongoDB | A NoSQL database |
| Collection | A group of documents |
| Document | One saved object |
| Mongoose | A tool that helps Node.js talk to MongoDB |
| Schema | Rules for what the data should look like |
| Model | Code used to create, read, update, and delete data |

## 8-Hour Practical Plan

| Time | Activity |
| --- | --- |
| 09:30 - 10:00 | Recap Day 3 API |
| 10:00 - 10:45 | Practicals 1 and 2 |
| 10:45 - 11:00 | Break |
| 11:00 - 12:15 | Practicals 3 and 4 |
| 12:15 - 01:00 | Practical 5 |
| 01:00 - 02:00 | Lunch |
| 02:00 - 03:15 | Practicals 6 and 7 |
| 03:15 - 03:30 | Break |
| 03:30 - 04:45 | Practical 8 |
| 04:45 - 05:30 | MongoDB recap and debugging |

## Intermediate Node.js Practicals

### Practical 1: Add Middleware Logging

Goal: See every request that reaches the server.

Add this before your routes:

```javascript
app.use((req, res, next) => {
  console.log(`${req.method} ${req.url}`);
  next();
});
```

Expected learning:

- Middleware runs before route handlers.
- `next()` allows the request to continue.

### Practical 2: Read Data from the Request Body

Goal: Understand how `POST` data enters the backend.

```javascript
app.post("/practice/body", (req, res) => {
  res.json({
    message: "I received your data",
    body: req.body
  });
});
```

Test with:

```text
POST http://localhost:3000/practice/body
Content-Type: application/json

{
  "title": "Learn request body"
}
```

Expected learning:

- `req.body` contains JSON sent by the client.

### Practical 3: Use Route Params

Goal: Read dynamic values from the URL.

```javascript
app.get("/practice/tasks/:id", (req, res) => {
  res.json({
    taskId: req.params.id
  });
});
```

Test:

```text
GET http://localhost:3000/practice/tasks/123
```

Expected learning:

- `:id` means the value can change.
- `req.params.id` reads the value.

### Practical 4: Use Query Params

Goal: Read filters from the URL.

```javascript
app.get("/practice/search", (req, res) => {
  res.json({
    completed: req.query.completed
  });
});
```

Test:

```text
GET http://localhost:3000/practice/search?completed=true
```

Expected learning:

- Query params are useful for filtering and searching.

### Practical 5: Move Settings to `.env`

Goal: Keep secrets and settings outside code.

Install:

```bash
npm install dotenv
```

Create `.env`:

```text
PORT=3000
MONGO_URL=your_mongodb_atlas_connection_string
```

Use it:

```javascript
require("dotenv").config();

const PORT = process.env.PORT || 3000;
```

Expected learning:

- `.env` stores configuration.
- Do not hardcode secrets in backend code.

### Practical 6: Create a Mongoose Schema

Goal: Define what a task should look like.

Students create `Task.js` using the code below.

Expected learning:

- Schema means rules.
- Model means a tool for database actions.

### Practical 7: Insert Data into MongoDB

Goal: Save one task permanently.

Students run `seed.js` using the code below.

Expected learning:

- MongoDB keeps data after the Node script stops.

### Practical 8: Read Data from MongoDB

Goal: Retrieve saved tasks.

Students update `seed.js` to add more tasks and print all tasks.

Expected learning:

- `Task.find()` reads documents from MongoDB.

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

- [ ] I understand middleware and `next()`.
- [ ] I can read `req.body`.
- [ ] I can read `req.params`.
- [ ] I can read `req.query`.
- [ ] I can use `.env` for settings.
- [ ] I know why databases are needed.
- [ ] I created a MongoDB Atlas database.
- [ ] I connected Node.js to MongoDB.
- [ ] I created and read data using Mongoose.

---

# Day 5: Advanced Beginner Node.js, CRUD, and Security

## Node.js Level

Advanced beginner Node.js.

Today students combine everything: Express, MongoDB, CRUD, users, password hashing, JWT tokens, protected routes, ownership checks, and safer error handling.

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
| Ownership Check | Making sure users can access only their own data |
| Validation | Checking user input before saving it |
| Error Handling | Sending safe error messages when something fails |

## 8-Hour Practical Plan

| Time | Activity |
| --- | --- |
| 09:30 - 10:00 | Recap Express and MongoDB |
| 10:00 - 10:45 | Practicals 1 and 2 |
| 10:45 - 11:00 | Break |
| 11:00 - 12:15 | Practicals 3 and 4 |
| 12:15 - 01:00 | Practical 5 |
| 01:00 - 02:00 | Lunch |
| 02:00 - 03:15 | Practicals 6 and 7 |
| 03:15 - 03:30 | Break |
| 03:30 - 04:45 | Practicals 8 and 9 |
| 04:45 - 05:30 | Full API test and recap |

## Advanced Node.js Practicals

### Practical 1: Plan the REST API

Goal: Map routes before coding.

| Feature | Method | Route |
| --- | --- | --- |
| Register | `POST` | `/register` |
| Login | `POST` | `/login` |
| List tasks | `GET` | `/tasks` |
| Create task | `POST` | `/tasks` |
| Update task | `PATCH` | `/tasks/:id` |
| Delete task | `DELETE` | `/tasks/:id` |

Expected learning:

- API design comes before API coding.

### Practical 2: Add Basic Input Validation

Goal: Do not accept empty data.

Example validation:

```javascript
if (!req.body.title) {
  return res.status(400).json({ message: "Title is required" });
}
```

Expected learning:

- Backends must not trust client input.
- `400` means the client sent bad or incomplete data.

### Practical 3: Create the User Model

Goal: Store users safely.

Students create a user schema with:

- `email`
- `passwordHash`

Expected learning:

- Never store plain passwords.

### Practical 4: Hash a Password with bcrypt

Goal: Convert a password into a safe stored hash.

```javascript
const passwordHash = await bcrypt.hash(req.body.password, 10);
```

Expected learning:

- Hashing is one-way.
- During login, we compare the password with the hash.

### Practical 5: Create a JWT Token

Goal: Give the user a signed token after login.

```javascript
const token = jwt.sign({ userId: user._id }, process.env.JWT_SECRET);
```

Expected learning:

- The token proves the user has logged in.
- The frontend sends the token with future requests.

### Practical 6: Build Auth Middleware

Goal: Protect private routes.

Students inspect the `authRequired` function in the code below.

Expected learning:

- Middleware can stop unauthorized requests.
- `401` means login is required.

### Practical 7: Add Full Task CRUD

Goal: Create, read, update, and delete tasks in MongoDB.

Students test:

- `GET /tasks`
- `POST /tasks`
- `PATCH /tasks/:id`
- `DELETE /tasks/:id`

Expected learning:

- CRUD is the foundation of most backend apps.

### Practical 8: Add Ownership Checks

Goal: Make sure users see only their own tasks.

Important pattern:

```javascript
const tasks = await Task.find({ userId: req.userId });
```

For update and delete:

```javascript
{ _id: req.params.id, userId: req.userId }
```

Expected learning:

- Never search only by task ID.
- Always include the current user's ID.

### Practical 9: Test Failure Cases

Goal: Prove the API is safer.

Students test:

- Missing token
- Wrong password
- Empty task title
- Updating a task that does not belong to the user
- Deleting a task that does not exist

Expected learning:

- Good APIs handle both success and failure.

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

  try {
    const token = authHeader.replace("Bearer ", "");
    const payload = jwt.verify(token, process.env.JWT_SECRET);

    req.userId = payload.userId;
    next();
  } catch (error) {
    res.status(401).json({ message: "Invalid token" });
  }
}

app.post("/register", async (req, res) => {
  if (!req.body.email || !req.body.password) {
    return res.status(400).json({ message: "Email and password are required" });
  }

  const passwordHash = await bcrypt.hash(req.body.password, 10);

  const user = await User.create({
    email: req.body.email,
    passwordHash
  });

  res.status(201).json({ id: user._id, email: user.email });
});

app.post("/login", async (req, res) => {
  if (!req.body.email || !req.body.password) {
    return res.status(400).json({ message: "Email and password are required" });
  }

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
  if (!req.body.title) {
    return res.status(400).json({ message: "Title is required" });
  }

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

- [ ] I can plan REST API routes before coding.
- [ ] I can validate required input.
- [ ] I understand CRUD.
- [ ] I hashed a password with bcrypt.
- [ ] I created a JWT after login.
- [ ] I protected task routes.
- [ ] I made sure users can only access their own tasks.
- [ ] I tested success and failure cases.

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
