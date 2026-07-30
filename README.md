# CRUD — Product Management System

A lightweight, no-framework **CRUD** (Create, Read, Update, Delete) app for managing products, built with vanilla HTML, CSS, and JavaScript. All data is persisted locally in the browser using `localStorage` — no backend or database required.

![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## Features

- **Create** — add new products with title, price, taxes, ads cost, discount, quantity, and category.
- **Read** — view all products in a dynamically rendered table.
- **Update** — edit an existing product's details in place.
- **Delete** — remove a single product from the list.
- **Auto-calculated total** — price, taxes, and ads are summed and the discount subtracted in real time as you type.
- **Search** — filter the product table live by title or category.
- **Bulk create** — set a "count" to insert multiple copies of the same product at once.
- **Persistent storage** — product data is saved to the browser's `localStorage`, so it survives page reloads.
- **Dark, minimal UI** — custom dark theme using the `Syne` and `JetBrains Mono` Google Fonts.

## Tech Stack

- **HTML5** — page structure (`index.html`)
- **CSS3** — custom dark-themed styling (`style.css`)
- **Vanilla JavaScript** — all CRUD logic and DOM manipulation (`main.js`)
- **Browser `localStorage`** — client-side data persistence
- `nodemon` (dev dependency) — optional auto-reload while developing locally

No frameworks, build tools, or backend server are required to run the app.

## Getting Started

### Option 1: Just open it
Since this is a static site, you can simply open `index.html` directly in your browser.

### Option 2: Run with a local dev server (recommended)
Using a local server avoids any browser quirks with `localStorage` and gives you live reload via `nodemon`.

```bash
# Clone the repository
git clone https://github.com/your-username/crud-project.git
cd crud-project

# Install dependencies
npm install

# Serve the project (e.g. with a static server / live-server of your choice)
npx nodemon
```

## Project Structure

```
CRUD Project/
├── index.html          # Markup: input form, search bar, and product table
├── style.css            # Dark-themed styling
├── main.js              # CRUD logic, search, and localStorage handling
├── package.json          # Project metadata & dependencies
└── package-lock.json
```

## How It Works

1. **Adding a product** — fill in the title, price, taxes, ads, discount, count, and category, then click **Create**. The total is calculated automatically as `price + taxes + ads - discount`.
2. **Updating a product** — click **update** on any row to load that product's data back into the form; the button switches to **update** mode until you submit the change.
3. **Deleting a product** — click **delete** on a row to remove it immediately.
4. **Searching** — type in the search box and toggle between **Search By Title** and **Search By Category** to filter the table live.
5. All changes are written to `localStorage` under the `product` key, so your data is preserved between sessions on the same browser.

## Roadmap / Possible Improvements

- [ ] Add a "delete all" confirmation action
- [ ] Form validation and user-facing error messages
- [ ] Replace `localStorage` with a real backend (Node/Express + database)
- [ ] Add sorting on table columns
- [ ] Add unit tests
