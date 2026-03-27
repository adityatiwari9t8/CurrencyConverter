# Currency Converter

A simple client-side currency converter web app powered by the free [Exchange Rates API](https://www.exchangerate-api.com/) (`open.er-api.com`).

## Project Structure

- `index.html` — UI layout and basic form elements
- `style.css` — visual styling
- `codes.js` — mapping of currency code to country code (for flag icons)
- `app.js` — app logic (dropdown setup, API fetch, swap, validation)

## Features

- Choose source (`From`) and target (`To`) currencies
- Input amount (default 1)
- Fetch latest exchange rate from `https://open.er-api.com/v6/latest/{base}`
- Display converted value and dynamic flag icons
- Swap currency pair with a single click
- Auto-converts on page load

## How to Run

1. Open `index.html` in your browser (double-click or serve from local HTTP server)
2. Enter an amount
3. Select source and target currencies
4. Click **Get Exchange Rate**

## Live API

The app requests rates via:
- `https://open.er-api.com/v6/latest/{fromCurrency}`

## Notes

- Handles empty or invalid amounts by resetting to `1`
- Flags use `https://flagsapi.com/{countryCode}/flat/64.png`
- Works in modern browsers that support `fetch` and ES6

## Optional Enhancements

- Add offline/detailed error handling and retry logic
- Add loading spinner instead of message text
- Add currency search/filter in dropdowns
- Persist last selection via `localStorage`
