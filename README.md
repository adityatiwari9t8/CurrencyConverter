# Currency Converter

![Status: Production Ready](https://img.shields.io/badge/status-production%20ready-brightgreen)
![License: MIT](https://img.shields.io/badge/license-MIT-blue)

A simple, responsive single-page currency converter powered by the free [Exchange Rates API](https://www.exchangerate-api.com/) (`open.er-api.com`).

> **Live demo**: open `index.html` in your browser, no backend required.

---

## 🚀 Quick Start

1. Clone or download this repository
2. Open `index.html` directly (double-click) or run:
   - `python -m http.server 8000` (or any static server)
   - then visit `http://localhost:8000`
3. Enter amount, select currencies, click **Get Exchange Rate**

---

## 📁 Project Structure

- `index.html` — UI layout and basic structure
- `style.css` — responsive styling and themed buttons
- `codes.js` — currency-to-country mapping for flag icons
- `app.js` — logic (dropdown fill, conversion, swap, API calls, validation)

---

## ✨ Features

- Input amount (default = 1)
- Select source (`From`) and target (`To`) currencies
- Fetch latest rate from `https://open.er-api.com/v6/latest/{base}`
- Display converted result instantly
- Show country flags next to each currency code
- Swap pair with one click
- Auto-convert on page load

---

## 🔌 API Endpoint

- `GET https://open.er-api.com/v6/latest/{fromCurrency}`

Example:

```sh
https://open.er-api.com/v6/latest/USD
```

---

## 🛠️ Behavior & Validation

- Invalid or empty amount resets to `1`
- Uses `fetch()` and modern ES6 syntax
- Works in modern browsers and fallback-friendly due to static content

---

## 🎯 UI Improvements (already included)

- Clean, minimal layout
- Interactive swap button
- Live conversion output
- Inline status text for errors and success

---

## 💡 Optional Enhancements

- Add search/filter for currency dropdowns
- Add loading spinner + aria-live updates
- Offline fallback using `localStorage` cached rates
- Add test coverage for conversion and endpoint error handling
- Add theme switch (light/dark)

---

## 📝 License

MIT License

