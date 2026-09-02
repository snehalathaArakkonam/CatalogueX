#  CatalogueX

CatalogueX is a full-stack web application for managing and browsing a catalogue of items. It provides separate features for **admins**, who manage the catalogue, and **users**, who browse, search, and view item details.

---

##  Project Overview

CatalogueX simplifies catalogue management for organizations that need to list, organize, and showcase items (products, books, inventory, etc.) through a simple web interface.

Using this application:

- Admins can add, update, and remove catalogue items.
- Admins can manage registered users.
- Users can register and log in to the system.
- Users can search and browse the catalogue.
- Users can view detailed information about each item.
- All data is stored in a database for persistence.

The application follows a simple **MVC-style architecture**.

---

##  Features

###  Admin
- Admin Login
- Add New Catalogue Items
- Update / Delete Items
- View & Manage Users
- Search Catalogue

###  User
- User Registration
- User Login
- Browse Catalogue
- Search Items
- View Item Details

---

##  Technologies Used

| Technology | Usage |
|------------|-------|
| Node.js / Express.js | Backend development |
| React.js | Frontend UI |
| MongoDB | Database |
| HTML | Page structure |
| CSS | Styling |
| JavaScript | Client-side functionality |
| Bootstrap | Responsive UI |
| Git | Version control |

---

##  Architecture

```text
                 ┌──────────────────┐
                 │      User        │
                 │   / Admin        │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │   React Frontend │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │  Express Server  │
                 │  Routes/Controllers│
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │   Models / ORM   │
                 └────────┬─────────┘
                          │
                          ▼
                 ┌──────────────────┐
                 │    MongoDB       │
                 │    Database      │
                 └──────────────────┘
```

---

##  Project Structure

```text
CatalogueX/
│
├── README.md
├── LICENSE
├── package.json
│
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   └── App.js
│   └── public/
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── config/
│   │   └── db.js
│   └── index.js
│
└── database/
    └── schema.sql
```

---

##  Database

The application uses **MongoDB** for storing application data.

```text
Example .env configuration:

DB_URI=mongodb://localhost:27017/cataloguex
PORT=5000
JWT_SECRET=your_secret_key
```

> **Important:** Never upload real credentials or `.env` files to GitHub.

---

##  How to Run

### 1. Prerequisites

- Node.js (v16 or higher)
- MongoDB installed and running
- Git

### 2. Clone the Repository

```bash
git clone https://github.com/snehalathaArakkonam/CatalogueX.git
cd CatalogueX
```

### 3. Install Dependencies

```bash
# Install server dependencies
cd server
npm install

# Install client dependencies
cd ../client
npm install
```

### 4. Configure Environment Variables

Create a `.env` file inside the `server/` directory:

```text
DB_URI=mongodb://localhost:27017/cataloguex
PORT=5000
JWT_SECRET=your_secret_key
```

### 5. Run the Application

```bash
# Start the backend server
cd server
npm start

# Start the frontend (in a new terminal)
cd client
npm start
```

### 6. Open the Application

```text
http://localhost:3000/
```

---

##  Contributing

Contributions are welcome! Please open an issue first to discuss what you'd like to change, then submit a pull request.

---

##  License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2026 Snehalatha Arakkonam

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
