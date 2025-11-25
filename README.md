# 🧱 Lego Collection — Full-Stack Web App  
A complete Node.js + Express + EJS + TailwindCSS application for managing a personal LEGO set collection.

This project provides a full CRUD interface, a clean UI, LEGO set data integration, and a structured modular codebase ready for deployment (including Vercel configuration).

---

## 📁 Project Structure

```
Lego-Collection/
│
├── data/                   # JSON datasets (LEGO themes, sets, details)
├── modules/                # Helper modules for data operations
├── public/                 # CSS, JS, images (static assets)
├── views/                  # EJS templates (pages + layouts)
│   ├── layout.ejs
│   ├── home.ejs
│   ├── sets.ejs
│   ├── set-details.ejs
│   └── errors.ejs
│
├── server.js               # Main Express server
├── package.json
├── tailwind.config.js
├── vercel.json             # Deployment config
└── .gitignore
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

### 1️⃣ Install dependencies

```
npm install
```

### 2️⃣ Run the server

```
npm start
```

Or with nodemon:

```
npm run dev
```

### 3️⃣ Visit the app  
Open:

```
http://localhost:3000
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

