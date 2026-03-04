# ⚡ Zenith Focus — Deep Work Suite

> A Pomodoro-based focus app with ambient sounds, statistics, and PWA support. Works offline once installed.

---

## 🚀 Features

### ⏱ Timer
- **4 modes:** Focus (25 min), Short Break (5 min), Long Break (15 min), Custom (1–180 min)
- **Automatic Pomodoro cycle:** After each focus session, the next phase starts automatically with a 5-second countdown
- **Adjustable cycle length:** Set how many focus sessions before a long break (2–8)
- **Progress ring:** Visual SVG ring tracks time remaining

### 🎵 Music & Sound
| Source | Description |
|--------|-------------|
| **Local Mixer** | Mix Rain, Forest, Fire, and Café sounds independently |
| **YouTube** | Built-in Lo-Fi, Nature, Jazz channels — or paste your own video link |
| **Spotify** | Paste your own playlist link, opens in Spotify |
| **Apple Music** | Paste your own playlist link, opens in Apple Music |

**Built-in presets:** 🌧️ Deep Rain · 🌲 Forest Calm · ☕ Café Study

### 📋 Task List
- Add daily tasks, mark as done, delete
- Persisted via `localStorage`

### 🎯 Daily Goal
- Set a session target between 1–12
- Live progress bar
- Turns green when the goal is reached
- Updates automatically after each completed session

### 📊 Statistics
- Today's minutes · Total sessions · This week · Avg. session length
- Best day ever · Current day streak 🔥
- 7-day bar chart

### 🌐 Multi-language
- Turkish / English — switch with one click
- All UI text updates instantly, preference is saved

### 🔔 Notifications
- Desktop notification on session/break end

### 📱 PWA
- Add to home screen (iOS, Android, desktop)
- Service Worker for full offline support
- 192×192 and 512×512 app icons

---

## 📁 File Structure

```
zenith-focus/
├── index.html          # Entire app (single file)
├── manifest.json       # PWA manifest
├── sw.js               # Service Worker
├── icon-192.png        # App icon (192×192)
├── icon-512.png        # App icon (512×512)
└── assets/
    ├── rain.mp3        # Rain ambience
    ├── forest.mp3      # Forest ambience
    ├── fire.mp3        # Fire crackling
    ├── cafe.mp3        # Café ambience
    └── complete.mp3    # Session complete sound
```

---

## ⚙️ Setup

### Local development

Opening files directly in a browser blocks audio (CORS). Use a simple local server:

```bash
# Python
python3 -m http.server 8080

# Node.js
npx serve .
```

Then open `http://localhost:8080` in your browser.

### Deploying to a server

Upload all files to your web server's root directory. No backend required — fully static.

> **Note:** HTTPS is required for PWA installation and Service Worker functionality.

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Space` | Start / Pause timer |
| `Esc` | Reset timer / Close modal |

---

## 🎨 Theming

- **Dark mode** (default): `#030305` background, `#a5b4fc` accent
- **Light mode:** `#f8fafc` background, `#4f46e5` accent
- Automatically detects system theme via `prefers-color-scheme`
- Respects `prefers-reduced-motion`

---

## 🔊 Sound License

Audio files in the `assets/` folder are licensed under the [Mixkit Free Sound Effects License](https://mixkit.co/license/). Free for both personal and commercial use — no attribution required.

---

## 🛠 Technical Notes

- Pure vanilla JS — no framework, no build step
- All data stored in `localStorage` (no server required)
- YouTube integration via IFrame Player API
- Fonts: [Outfit](https://fonts.google.com/specimen/Outfit) + [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono)
- Icons: [Font Awesome 6](https://fontawesome.com/)

---

## 📄 License

MIT
