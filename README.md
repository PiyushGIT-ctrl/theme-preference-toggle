# theme-preference-toggle
A JavaScript-based theme toggle system that detects system preference (dark/light) and updates UI dynamically with smooth transitions.

This project detects the user's system theme, allows manual toggling, and persists user preferences using `localStorage`.

---

##  Features

*  Detects system theme using `prefers-color-scheme`
*  Real-time update when system theme changes
*  Manual theme toggle button
*  Saves user preference using `localStorage`
*  Smooth UI transitions using CSS

---

## How It Works

### 1. System Theme Detection

* Uses:

  ```
  window.matchMedia("(prefers-color-scheme: dark)")
  ```
* Automatically applies `dark` or `light` class to `<body>`

---

### 2. User Preference (Override System)

* When user clicks toggle button:

  * Theme switches between `dark` and `light`
  * Preference is stored in `localStorage`

---

### 3. Persistence

* On page load:

  * Checks if a saved theme exists in `localStorage`
  * If yes → applies saved theme
  * If no → falls back to system preference

---

### 4. Live System Updates

* Listens for system theme changes:

  ```
  matchMedia(...).addEventListener("change")
  ```
* Updates UI dynamically (unless overridden by user)

---

## ⚙️ Tech Stack

* HTML
* CSS (Flexbox + Variables)
* JavaScript (DOM + Events + Storage)

---

## 📂 Project Structure

```
index.html
script.js
```

---

## Key Concepts Used

* `matchMedia()` for system detection
* `classList` for dynamic styling
* `localStorage` for persistence
* Event listeners for interactivity

---

## What I Learned

* Difference between **system preference vs user preference**
* Debugging browser-specific behavior (Brave forcing dark mode)

---

## Future Improvements

* Add toggle icon (🌙 / ☀️)
* Add transition animations between themes
* Add “Reset to system preference” option
* Improve UI design

---

💡 Built as part of my JavaScript learning journey.
