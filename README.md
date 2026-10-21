# 🎬 Road to Doomsday: MCU Watch Tracker

An interactive, single-page tracker for catching up on the entire Marvel Cinematic Universe before **Avengers: Doomsday (Dec 18, 2026)**. It lists every movie, series, special and short in order, tells you which ones actually matter, and lets you search, filter and tick off what you've watched.

---

## ✨ Features

- **Live search**: type a title, year, phase, format (Movie / Series / Short / Special) or platform and the list narrows instantly.
- **Importance filters**: view only *Essential*, *Context* or *Skippable* titles, so you can pick between a full marathon and a short prep run.
- **Unwatched-only view**: hide everything you've already finished.
- **Progress checkboxes**: mark titles as watched; they get struck through and dimmed.
- **Doomsday countdown**: a live "days left" counter to the Dec 18, 2026 release.
- **Streaming info**: each title shows where to watch it (mostly Disney+).
- **Phase-wise layout**: Phase 1 through Phase 6, plus an optional X-Men homework section for the legacy-cast appearances.
- **Responsive, dark UI** with a sticky search bar that stays visible as you scroll.

## 🧰 Tech Stack

- HTML5
- CSS3 (custom properties, flexbox, sticky positioning)
- Vanilla JavaScript (no frameworks, no build step)
- Google Fonts (Anton, IBM Plex Sans, JetBrains Mono)

The whole app is one self-contained HTML file.

## 🚀 Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/NeerajM01/Doomsday-tracker.git

# 2. Open the file in your browser
cd <repo-name>
open mcu_doomsday_tracker.html   # macOS
# or just double-click the file on Windows/Linux
```

No installs or dependencies needed.

### Host it for free with GitHub Pages

1. Rename `mcu_doomsday_tracker.html` to `index.html`.
2. In your repo go to **Settings → Pages**.
3. Choose the `main` branch and `/ (root)`, then save.
4. Your tracker will be live at `https://github.com/NeerajM01/Doomsday-tracker.git/`.

## 📂 Project Structure

```
.
├── mcu_doomsday_tracker.html   # The entire app (markup, styles, logic, data)
└── README.md
```

## 🧠 How It Works

All titles live in a single `DATA` array in the script. Each entry holds its watch-order number, phase, title, year, type, importance level and streaming platform. The search box and filter chips update two state variables, and a `render()` function rebuilds the list from the array, grouping entries under their phase headings.

To add a title, append an object to `DATA`:

```js
{ n: 68, phase: "Phase 6 — Direct Lead-In", t: "Title Here", y: 2026,
  type: "Series", imp: "ctx", plat: "Disney+" }
```

`imp` takes `ess`, `ctx` or `skip`.

## ⚠️ Known Limitations

- Watch progress is kept in memory only, so it resets when you refresh the page.
- Streaming availability changes often; check the platform before you plan a marathon.
- The Netflix-era Marvel shows (Daredevil, Jessica Jones, Luke Cage, Iron Fist, The Punisher), *Agents of S.H.I.E.L.D.*, *Runaways*, *Cloak & Dagger* and *Helstrom* are not in the list yet.

## 🗺️ Roadmap

- [ ] Add the Netflix, ABC and Hulu Marvel series
- [ ] Save watch progress with `localStorage`
- [ ] Progress bar showing the percentage watched
- [ ] "Essential only" quick-start marathon mode
- [ ] Release-order vs. chronological-order toggle

## 🙌 Acknowledgements

Marvel, the Marvel Cinematic Universe and all related titles and characters belong to Marvel Studios / The Walt Disney Company. This is an unofficial fan project made for personal use and is not affiliated with or endorsed by Marvel or Disney.

## 👤 Author

**Neeraj**
GitHub: [@NeerajM01](https://github.com/NeerajM01)

If you find this useful, give it a ⭐ and happy watching!