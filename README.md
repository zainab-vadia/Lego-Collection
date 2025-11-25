# 🧱 Lego Collection — Full-Stack Web App  
A complete Node.js + Express + EJS + TailwindCSS application for managing a personal LEGO set collection.

This project provides a full CRUD interface, a clean UI, LEGO set data integration, and a structured modular codebase ready for deployment (including Vercel configuration).

---

## 📁 Project Structure

```
LegoSets/
│
├── data/                     # LEGO Themes & Sets JSON
│
├── modules/
│   ├── legoSets.js           # Handles set/theme data operations
│   └── auth-service.js       # Handles users, login, register, MongoDB
│
├── public/                   # CSS, images, static assets
│
├── views/                    # EJS templates
│   ├── login.ejs
│   ├── register.ejs
│   ├── userHistory.ejs
│   ├── sets.ejs
│   ├── set.ejs
│   ├── addSet.ejs
│   ├── editSet.ejs
│   ├── about.ejs
│   ├── home.ejs
│   ├── 404.ejs
│   ├── 500.ejs
│   └── partials/             # Headers, navbars, etc.
│
├── .env                      # Environment variables
├── server.js                 # Main Express app
├── tailwind.config.js
├── package.json
└── vercel.json               # Optional deployment config
```

---

## 🚀 Features

### 🔍 Browse LEGO Sets  
- View all available LEGO sets  
- Filter by theme  
- See piece count, year, and images  

### 📦 Set Details  
- Full page for each set  
- Item number, name, description  
- High-quality thumbnails  

### ➕ Add / Edit / Remove  
- Add new sets to your collection  
- Edit existing set details  
- Delete sets from the database (JSON data layer)

### 🎨 Clean UI  
- Styled using **TailwindCSS**  
- Templates powered by **EJS**  
- Fully responsive design  

### ⚙️ Backend  
- Node.js + Express  
- Modular code structure  
- JSON-based database (no external DB)  
- Helper modules for parsing, searching, filtering  

### ☁️ Deployment  
Includes `vercel.json` for instant deployment on Vercel.

---

## 🛠 Installation & Setup

### 1. Install Dependencies
```
npm install
```

### 2. Create a `.env` file
```
PORT=8080
MONGODB=<your MongoDB cluster URI>
```

### 3. Start the Server
```
npm start
```

Visit:

```
http://localhost:8080
```

---

## 🧪 Data Model Overview

### **Sets (`data/sets.json`)**
```json
{
  "set_num": "75257",
  "name": "Millennium Falcon",
  "year": 2019,
  "theme_id": 158,
  "num_parts": 1351,
  "img_url": "...",
  "set_url": "..."
}
```

### **Themes (`data/themes.json`)**
```json
{
  "id": 158,
  "name": "Star Wars"
}
```

---

## 📡 API-Like Helper Methods  
Located inside `/modules`:

- `getAllThemes()`  
- `getAllSets()`  
- `getSetsByTheme(theme)`  
- `getSetByNum(id)`  
- `addSet(setData)`  
- `updateSet(id, updatedData)`  
- `deleteSet(id)`  

These make the project easy to extend into a true REST API later.

---

## 🖼 UI / Pages

- `/` – Home  
- `/sets` – Browse all LEGO sets  
- `/sets/:id` – Set details page  
- `/add-set` – Add new LEGO set  
- `/edit/:id` – Edit existing set  
- `/delete/:id` – Remove set  
- Error pages (404, 500)

---

## 🧰 Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | EJS, TailwindCSS |
| Backend | Node.js, Express |
| Data | Local JSON files |
| Deployment | Vercel (optional) |

---

## 📄 Scripts

From `package.json`:

```
npm start     # Run server
npm run dev   # Run with nodemon
```

---

## 📝 License

This project is for educational use and personal portfolio development.

---

## 👥 Author  
zmvadia

