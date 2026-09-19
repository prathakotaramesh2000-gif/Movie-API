# 🎬 Movie API

<p align="center">
  <img src="https://img.shields.io/badge/Movie-API-red?style=for-the-badge&logo=imdb&logoColor=white" alt="Movie API">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
</p>

<p align="center">
  <strong>🎥 Discover Movies • 🔎 Search Movies • ⭐ Explore Details</strong>
</p>

<p align="center">
  A modern movie-search web application built to demonstrate API integration, asynchronous JavaScript, dynamic UI rendering, and responsive frontend development.
</p>

<p align="center">
  <a href="https://github.com/prathakotaramesh2000-gif/Movie-API">📂 View Source Code</a>
</p>

---

## 🎞️ About The Project

**Movie API** is a frontend web application that allows users to explore movie information through an API-driven interface.

The application demonstrates how a frontend application can communicate with an external API, retrieve movie data, process the response, and dynamically display the results to users.

This project was created as a practical project for learning and demonstrating **Frontend Development + API Integration + JavaScript**.

---

## ✨ Key Features

| Feature              | Description                                    |
| -------------------- | ---------------------------------------------- |
| 🎬 Movie Search      | Search for movies using keywords               |
| 🔌 API Integration   | Retrieve movie information from an API         |
| 🖼️ Movie Posters    | Display movie posters dynamically              |
| ⭐ Movie Information  | Show relevant movie details                    |
| ⚡ Dynamic Rendering  | Update the UI without refreshing the page      |
| 🔎 Search Experience | Quickly find movies                            |
| 📱 Responsive UI     | Designed to work across different screen sizes |
| ❌ Error Handling     | Handles invalid or unsuccessful API requests   |

---

# 🖥️ Application Preview

Add your screenshots here:

```text
screenshots/
├── home.png
├── search.png
├── movie-details.png
└── mobile-view.png
```

Then add them to this section:

```markdown
![Movie API Home](screenshots/home.png)

![Movie Search](screenshots/search.png)

![Movie Details](screenshots/movie-details.png)
```

---

# 🛠️ Tech Stack

### Frontend

<p>
<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white">
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black">
</p>

### API & Data

* REST API
* JSON
* Fetch API
* HTTP Requests

### Development Tools

* Visual Studio Code
* Git
* GitHub
* Web Browser Developer Tools

---

# 📁 Project Structure

```text
Movie-API/
│
├── index.html
├── style.css
├── script.js
├── images/
│   └── ...
├── screenshots/
│   └── ...
└── README.md
```

> Update the structure above if your repository contains different filenames or folders.

---

# 🔄 How The Application Works

```text
                    👤 USER
                      │
                      ▼
              🔎 Enter Movie Name
                      │
                      ▼
                 JavaScript
                      │
                      ▼
                🌐 Movie API
                      │
                      ▼
                📦 JSON Response
                      │
                      ▼
             Process Movie Data
                      │
                      ▼
             🖥️ Dynamic Rendering
                      │
                      ▼
               🎬 Movie Results
```

---

# 🔌 API Integration

The application uses JavaScript to communicate with a movie API.

A typical API request follows this pattern:

```javascript
fetch(API_URL)
    .then(response => response.json())
    .then(data => {
        console.log(data);
    })
    .catch(error => {
        console.error("Error fetching movie data:", error);
    });
```

### API Workflow

```text
Request
   ↓
API Server
   ↓
HTTP Response
   ↓
JSON Data
   ↓
JavaScript
   ↓
DOM
   ↓
Movie Cards
```

---

# 🔎 Movie Search

The search functionality allows users to enter a movie name and retrieve matching results.

Example:

```javascript
const searchMovie = async (movieName) => {

    const response = await fetch(
        `${API_URL}?query=${movieName}`
    );

    const data = await response.json();

    displayMovies(data);
};
```

The basic process is:

```text
User enters movie
        ↓
Search button clicked
        ↓
JavaScript captures input
        ↓
API request sent
        ↓
API returns JSON
        ↓
Movie data processed
        ↓
Movie cards displayed
```

---

# 🧩 Movie Card

Movie information can be displayed dynamically using JavaScript.

Example:

```javascript
const movieCard = `
    <div class="movie-card">
        <img src="${movie.poster}" alt="${movie.title}">
        <h2>${movie.title}</h2>
        <p>⭐ ${movie.rating}</p>
        <p>${movie.releaseDate}</p>
    </div>
`;
```

This demonstrates **dynamic DOM rendering** using JavaScript.

---

# ⚡ Async JavaScript

The project demonstrates asynchronous JavaScript using:

### Promise

```javascript
fetch(API_URL)
    .then(response => response.json())
    .then(data => console.log(data));
```

### Async / Await

```javascript
async function getMovies() {

    try {

        const response = await fetch(API_URL);

        const data = await response.json();

        console.log(data);

    } catch (error) {

        console.error(error);

    }
}
```

Using `async/await` makes API-related code easier to read and maintain.

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/prathakotaramesh2000-gif/Movie-API.git
```

---

## 2️⃣ Navigate to the Project

```bash
cd Movie-API
```

---

## 3️⃣ Open the Project

If you are using VS Code:

```bash
code .
```

---

## 4️⃣ Run the Application

You can use **Live Server** in VS Code.

```text
Right Click index.html
        ↓
Open with Live Server
        ↓
Browser
        ↓
Movie API Application
```

---

# 🔐 API Key Configuration

If your movie API requires an API key, avoid committing the key directly to a public repository.

For example:

```javascript
const API_KEY = "YOUR_API_KEY";
```

Replace it with your own API key when running the project locally.

### ⚠️ Important

Do not publish private API keys in a public GitHub repository.

For production applications, API credentials should be stored securely using appropriate environment/configuration mechanisms.

---

# 🧪 Example User Flow

### Step 1

User opens the application.

```text
🎬 Movie API
```

### Step 2

User enters:

```text
Avatar
```

### Step 3

The application sends a request to the movie API.

### Step 4

The API returns movie information.

### Step 5

The application displays:

```text
┌─────────────────────────┐
│      🎬 Movie Poster     │
│                         │
│        Avatar           │
│                         │
│ ⭐ Rating               │
│ 📅 Release Date         │
│                         │
└─────────────────────────┘
```

---

# 🧠 Concepts Learned

This project demonstrates practical knowledge of:

* HTML5
* CSS3
* JavaScript
* DOM Manipulation
* Event Handling
* Functions
* Arrays
* Objects
* JSON
* REST APIs
* HTTP Requests
* Fetch API
* Promises
* Async/Await
* Error Handling
* Responsive Web Design
* Git
* GitHub

---

# 📈 Future Enhancements

The project can be extended with:

### 🎯 User Experience

* 🎨 Dark / Light mode
* ❤️ Favorite movies
* ⭐ Movie ratings
* 🔖 Watchlist
* 🔍 Advanced search
* 🎭 Genre filters
* 📅 Year filters

### ⚙️ Technical Improvements

* Pagination
* Loading skeletons
* Better error handling
* API caching
* Debounced search
* Environment variables
* Backend integration
* Database support

### 👤 User Features

* User registration
* Login system
* Personal watchlist
* Movie reviews
* Movie ratings
* User profiles

---

# 📊 Project Architecture

```text
┌─────────────────────┐
│       Browser       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│      index.html     │
│     User Interface  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│      style.css      │
│       Styling       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│     script.js       │
│   Application Logic │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│      Movie API      │
│     JSON Response   │
└─────────────────────┘
```

---

# 🎤 Interview Explanation

You can explain this project during an interview like this:

> **"I developed a Movie API web application using HTML, CSS, and JavaScript. The main purpose of the project was to understand real-world API integration. I used the Fetch API to send requests to the movie API, processed the JSON response, and dynamically displayed movie information on the webpage. I also implemented search functionality, asynchronous JavaScript using Promises and Async/Await, error handling, and responsive UI design. This project helped me understand how frontend applications communicate with external APIs and how API data can be dynamically rendered in the DOM."**

---

# ❓ Interview Questions From This Project

### 1. What is an API?

An **API (Application Programming Interface)** allows different software applications to communicate with each other.

### 2. Why did you use Fetch API?

The Fetch API allows JavaScript to make HTTP requests and retrieve data from external services.

### 3. What is JSON?

JSON stands for **JavaScript Object Notation**. It is commonly used to exchange structured data between applications.

### 4. What is asynchronous JavaScript?

Asynchronous JavaScript allows operations such as API requests to execute without blocking the rest of the application.

### 5. What is `async/await`?

`async/await` provides a cleaner way to work with Promises.

### 6. How do you handle API errors?

Using `try/catch` with `async/await` or `.catch()` with Promises.

### 7. What happens when the API returns JSON?

The JSON response is converted into a JavaScript object using:

```javascript
response.json()
```

### 8. How do you display API data?

JavaScript can dynamically create HTML elements and insert them into the DOM.

---

# 🏆 Skills Demonstrated

```text
Frontend Development
        │
        ├── HTML
        ├── CSS
        └── JavaScript
             │
             ├── DOM
             ├── Events
             ├── Fetch API
             ├── JSON
             ├── Promises
             └── Async/Await
                    │
                    ▼
               REST API
                    │
                    ▼
              Dynamic UI
```

---

# 🌐 GitHub Repository

### 🔗 Source Code

**Movie API Repository**

https://github.com/prathakotaramesh2000-gif/Movie-API

---

# 👨‍💻 Author

### Prathakota Ramesh

💻 GitHub:
https://github.com/prathakotaramesh2000-gif

---

# ⭐ Show Your Support

If this project helped you learn API integration or frontend development:

⭐ **Star this repository**

🍴 **Fork the repository**

📚 **Use it for learning**

---

<p align="center">
  <strong>🎬 Movie API • Built with HTML, CSS & JavaScript</strong>
</p>

<p align="center">
  Made with ❤️ for learning and development
</p>
