# 👗 WardrobeOracle — Web SPA Prototype

**WardrobeOracle** is a mobile-first, single-file web app that helps you choose outfits faster.  
Digitize your closet, get daily swipe-style outfit suggestions, and keep a **style streak** to nudge sustainable re-wear.

This repository ships a **self-contained SPA** (`wardrobe_oracle.html`) built with **HTML + Tailwind CSS + Vanilla JS**.

---

## ✨ Features

- **Swipe to Style**
  - Randomized outfits from your own wardrobe (Top, Bottom, Shoes).
  - Approve an outfit to **increment your streak**; skip or swap for a fresh combo.

- **Gamified Streaks**
  - Visual streak counter in the header.
  - “Love it!” → streak +1 and locks the day’s choice.

- **Wardrobe Management**
  - Add items (name, category, optional image URL).  
  - Auto-image fallback via placeholder if you don’t provide one.
  - Grid view with hover label + quick remove.

- **Category Management**
  - Default categories: Top, Bottom, Shoes, Outerwear, Accessory.
  - Add custom categories and remove any you don’t need.
  - **AI Auto-Categorize** button (Gemini) from the “Add Item” modal.

- **Style Coaching (AI)**
  - Get a short, positive **style tip** (text) for the current outfit (Gemini).
  - After approving an outfit, request another text tip.

- **Photo Feedback (AI)**
  - Upload a photo of your outfit; receive a brief, constructive note (Gemini).

- **Local Guide (AI)**
  - “📍 Where to wear in Barcelona?” suggests 3 activities/places for your look (Gemini).

- **Mobile-First UI**
  - Tailwind CSS, soft cards, bottom nav, and smooth view transitions.

> ℹ️ State is **in-memory** only—refresh clears items/streak. Persisting data (LocalStorage/IndexedDB) is a future enhancement.

---

## 🧱 Tech Stack

- **HTML5** — structure and content
- **Tailwind CSS (CDN)** — utility-first responsive styling
- **Vanilla JavaScript** — state, rendering, and interactions
- **Google Fonts (Inter)**

No build tools. No frameworks. Just open the file.

---

## 🚀 Quick Start

1. **Clone / Download** this repo.
2. Open `wardrobe_oracle.html` in any modern browser (Chrome, Edge, Firefox, Safari).

That’s it. The prototype runs locally with no install steps. 🎉

---

## 🔑 Optional: Enable Gemini-Powered Features

Several buttons call the **Google Generative Language (Gemini) API**:

- ✨ Get Style Tip  
- ✨ Get Style Tip (Text-based)  
- 📸 Get Feedback on Your Look  
- 📍 Where to Wear in Barcelona?  
- ✨ Auto-categorize with AI

To enable these:

1. Create an API key in **Google AI Studio / Generative Language API**.
2. Open `wardrobe_oracle.html`.
3. Find `const apiKey = "";` and paste your key as a string.

```js
const apiKey = "YOUR_API_KEY_HERE";

##⚠️ Security note: This SPA is client-side only. Embedding API keys in the browser is not secure for production. For real apps, proxy requests via a backend you control and keep secrets server-side. Add rate-limit and CORS policies accordingly.

