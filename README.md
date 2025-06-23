# Blog Posts App

A simple blog post manager using vanilla JavaScript, JSON Server, and Live Server. This project allows you to view, add, edit, and delete blog posts with a mock API.

---

## Table of Contents

- [Setup](#setup)
- [API Endpoints](#api-endpoints)
- [Core Features](#core-features)
- [Advanced Features](#advanced-features)
- [Extra Advanced Features](#extra-advanced-features)
- [Project Structure](#project-structure)
- [Notes](#notes)

---

## Setup

1. **Create Project Structure**

   Create a new folder and add the following files:
   - `index.html`
   - `src/index.js`
   - `css/styles.css`
   - `db.json`

2. **Install JSON Server**

   - `npm install -g json-server@0.17.4`


3. **Add Sample Data**

Add valid JSON sample data to `db.json`. Example:

{
"posts": [
{
"id": 1,
"title": "My First Blog Post",
"content": "Welcome to my blog!",
"author": "Jane Doe",
"image": ""
}
]
}


4. **Start JSON Server**

- `json-server db.json` 

The mock API will be available at `http://localhost:3000`.

5. **Start Live Server**

In your project folder, run:
- `live-server`

This will open your frontend in the browser.

6. **Write Your Code**

- Write all JavaScript logic in `src/index.js`.
- Ensure all DOM manipulation works as specified.

---

## API Endpoints

Your base URL is: `http://localhost:3000`

| Method | Endpoint         | Description                        |
|--------|------------------|------------------------------------|
| GET    | /posts           | Retrieve all blog posts            |
| GET    | /posts/:id       | Retrieve a single blog post by ID  |
| POST   | /posts           | Create a new blog post             |
| PATCH  | /posts/:id       | Update an existing blog post       |
| DELETE | /posts/:id       | Delete a blog post                 |

---

## Core Features

- **View All Posts**
- On page load, `displayPosts` fetches all posts and displays their titles and images in the `#post-list` div.

- **View Post Details**
- Clicking a post title calls `handlePostClick`, fetching and displaying the post's title, content, and author in `#post-detail`.

- **Add New Post**
- Submitting the form with ID `new-post-form` triggers `addNewPostListener`.
- Creates a new post from form values and adds it to `#post-list` (no persistence required for this deliverable).

- **Initialization**
- The `main()` function should call `displayPosts` and `addNewPostListener` after the DOM has fully loaded.

---
### Authored By
- Mcadams Njogu

### License
- GNU
