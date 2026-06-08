# 📚 Library Management System

A fully functional **CRUD-based Library Management System** built with vanilla HTML, CSS, and JavaScript. Developed as part of the **DevOps B2 Program** academic assignment.

🔗 **Live Demo:** [vishalpandey1329.github.io/library-management-system](https://vishalpandey1329.github.io/library-management-system/)

---

## 📌 Project Overview

This application allows users to manage a library's book collection through a clean, responsive interface. It demonstrates all four **CRUD operations** — Create, Read, Update, and Delete — with persistent data storage using the browser's `localStorage`.

---

## ✅ Features

| Feature | Description |
|---|---|
| ➕ Add Book | Add a new book with title, author, genre, year, ISBN and status |
| 📋 View Records | Browse all books in a structured table with live stats |
| ✏️ Edit Book | Update any book's details via a pre-filled modal form |
| 🗑️ Delete Book | Remove a book with a confirmation prompt |
| 🔍 Search | Search by title, author, or ISBN in real time |
| 🔽 Filter | Filter books by status (Available / Issued / Lost) and genre |
| ✔️ Validation | Inline error messages for required fields, year range, and duplicate ISBN |
| 💾 Database | Data persists across page reloads using localStorage |
| 📱 Responsive | Works on desktop and mobile screens |
| 🌙 Dark Mode | Automatically adapts to system dark/light preference |

---

## 🛠️ Tech Stack

- **HTML5** — Structure and semantic markup
- **CSS3** — Styling, responsive layout, dark mode via CSS variables
- **JavaScript (Vanilla)** — CRUD logic, validation, DOM manipulation
- **localStorage** — Client-side persistent database
- **Tabler Icons** — Icon library via CDN
- **GitHub Pages** — Free static site hosting / deployment

---

## 📂 Project Structure

```
library-management-system/
│
├── index.html        # Main application (all-in-one: HTML + CSS + JS)
└── README.md         # Project documentation
```

---

## 🔄 CRUD Operations Explained

### Create
Clicking **"Add book"** opens a modal form. On submit, a new book object with a unique ID is created and saved to localStorage.

### Read
The `renderTable()` function loads all records from localStorage, applies search and filter criteria, and renders them as table rows. Stats cards update live.

### Update
Clicking the ✏️ edit icon pre-fills the modal form with that book's existing data. On save, the matching record is found by ID and replaced with updated values.

### Delete
Clicking the 🗑️ delete icon triggers a confirmation dialog. On confirm, the record is removed from the array and localStorage is updated.

---

## ✔️ Validation Rules

- **Title** — Required field
- **Author** — Required field
- **Year** — Must be a number between 1000 and 2026 (optional)
- **ISBN** — Must be unique across all records (optional)

---

## 🚀 How to Run Locally

No installation or server required.

1. Clone or download this repository
2. Open `index.html` in any modern browser
3. The app runs fully offline

```bash
git clone https://github.com/VishalPandey1329/library-management-system.git
cd library-management-system
# Open index.html in your browser
```

---

## 🗄️ Database Design

Each book record is stored as a JSON object:

```json
{
  "id": "b_1234567890_abc12",
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "genre": "Technology",
  "year": 2008,
  "isbn": "978-0-13-235088-4",
  "status": "Available"
}
```

All records are stored in `localStorage` under the key `lms_books_v1`.

---

## 👨‍💻 Author

**Vishal Pandey**
Student ID: 500125280
DevOps B2 Program

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
