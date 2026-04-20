# 📚 TaskRing

A personal assignment tracker built as a single, standalone HTML file. No installation, no server, no dependencies to install — just open in a browser and use.

---

## 🚀 Getting Started

### Option 1 — Browser (Desktop)
1. Download `taskring.html`
2. Double-click the file
3. It opens directly in your browser — done

### Option 2 — PWA on Android (feels like an app)
1. Open `taskring.html` in **Chrome on Android**
2. Tap the 3-dot menu → **"Add to Home Screen"**
3. It installs as an app icon on your home screen with no APK needed

### Option 3 — Build an APK
If you want a real Android APK, wrap the HTML using Capacitor:
```bash
npm create vite@latest taskring -- --template react
# paste the component code in
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap add android
npx cap open android   # opens Android Studio → Build → Generate Signed APK
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 📊 Dashboard | Overview of all assignments with stats, progress ring, and overdue alerts |
| ✏️ Add Assignment | Create tasks with subject, priority, due date/time, notes, and reminder |
| ✅ Mark Complete | Tick off finished work; completed items are archived |
| 🔔 Alerts | Notification inbox + upcoming deadline list + test alert button |

---

## 🗂 Pages

### Dashboard
- 4 stat cards: Total / Pending / Done / Overdue
- Circular progress ring showing overall completion %
- Overdue banner (glowing red) and "due today" banner (orange)
- All pending assignments sorted by due date (soonest first)
- Tap any card to open the detail modal

### Add Assignment
- Required fields: Title, Due Date
- Optional fields: Subject, Priority, Due Time, Notes
- Reminder slider: set alert from 15 minutes to 24 hours before due
- Subjects available: Math, Physics, Chemistry, English, History, Computer Science, Biology, Art, Music, Economics
- Priorities: `low` · `medium` · `high` · `urgent`

### Mark Complete
- Circle checkbox on each row — hover to confirm, click to complete
- Completed items move to an archived section below
- Tap any row to open the detail modal
- Delete button on each row

### Alerts
- Notification inbox with type-coded borders (red = urgent, orange = warning, blue = info)
- "Clear all" button
- Test alert button to simulate a ringing reminder
- Upcoming deadlines list (next 8 pending assignments)

---

## 🎨 Design

| Token | Value |
|---|---|
| Background | `#0A0A0F` |
| Surface | `#13131A` |
| Card | `#1C1C26` |
| Accent (purple) | `#6C63FF` |
| Success (green) | `#22D3A4` |
| Warning (orange) | `#FF8C42` |
| Danger (red) | `#FF4D6D` |
| Highlight (yellow) | `#FFD166` |
| Body font | Plus Jakarta Sans |
| Mono font | Space Mono |

---

## 🧱 Tech Stack

| Layer | Technology |
|---|---|
| UI framework | React 18 (via CDN) |
| JSX compiler | Babel Standalone (via CDN) |
| Styling | Inline React styles + CSS keyframes |
| State | React `useState` / `useEffect` / `useCallback` |
| Storage | In-memory (resets on refresh — no backend) |
| Fonts | Google Fonts (requires internet on first load) |

> **Note:** Since there is no database or localStorage, data resets every time the page is refreshed. To persist data, a localStorage integration or a backend would need to be added.

---

