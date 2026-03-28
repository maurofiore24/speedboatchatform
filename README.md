# ⛵ Lola Boat Rent Montenegro — Booking Form

A lightweight, single-file booking form for boat tour reservations in Montenegro. Built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies, no backend required.

---

## ✨ Features

- **Custom calendar** with real-time availability pulled from Google Calendar API
- **Color-coded dates** — green for available, orange for partially booked
- **Hover tooltips** showing existing bookings on busy days
- **WhatsApp & Instagram** share buttons on booking confirmation
- **Mobile-first** responsive design
- **Elegant dark UI** with gold accents — no external CSS frameworks

---

## 🚀 Live Demo

> Hosted on GitHub Pages at: `https://maurofiore24.github.io/speedboatchatform/just-book-it2.html`

---

## 📁 Project Structure

```
speedboatchatform/
└── just-book-it2.html   # Complete app — single self-contained file
```

---

## ⚙️ Setup

### 1. Google Calendar API

This project reads availability from a public Google Calendar.

- Go to [console.cloud.google.com](https://console.cloud.google.com)
- Create a new project → enable **Google Calendar API**
- Create an **API Key** under Credentials
- In Google Calendar settings, set the calendar to **"Make available to public"** → **"See all event details"**

### 2. Configure the HTML file

Open `just-book-it2.html` and update these two lines near the bottom:

```js
var API_KEY = 'YOUR_GOOGLE_API_KEY';
var CAL_ID  = 'your-calendar-id@gmail.com';
```

### 3. Host it

The file must be served over HTTPS for the Google Calendar API to work (browsers block API calls from `file://`).

Recommended free hosting options:
- **GitHub Pages** — enable in repo Settings → Pages → main branch
- **Netlify** — drag & drop the file at netlify.com
- **tiiny.host** — upload and get a link instantly

---

## 📱 How It Works

1. Customer opens the booking form
2. Selects a date from the live calendar
3. Fills in tour details (duration, passengers, route, time)
4. Submits — sees a booking summary
5. Sends the summary to the operator via **WhatsApp** or copies it for **Instagram DM**

No data is stored — the form generates a pre-filled message that the customer sends directly to the boat operator.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| UI | HTML5 + CSS3 (custom properties) |
| Logic | Vanilla JavaScript (ES5 compatible) |
| Calendar data | Google Calendar API v3 |
| Fonts | Google Fonts — Cormorant Garamond + DM Sans |
| Hosting | GitHub Pages / Netlify / tiiny.host |

---

## 🔒 Security Note

The Google API Key is embedded in the client-side HTML. For production use, it is recommended to:
- Restrict the API key to specific HTTP referrers in Google Cloud Console
- Or proxy the calendar request through a serverless function (e.g. Cloudflare Workers)

---

## 📄 License

MIT — free to use and modify.

---

*Built for Lola Boat Rent Montenegro 🇲🇪*
