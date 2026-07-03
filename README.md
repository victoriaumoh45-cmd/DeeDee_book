# DeeDee Books — your reading tracker

A private, offline library app for EPUB and PDF books: add books, read them, and track
progress, shelves, notes, and yearly reading goals. Everything is stored **on your device
only** — nothing is uploaded anywhere.

## What's in this version

- **Dark mode** — Settings → Appearance (Light / Dark / follows your phone automatically)
- **Search** — tap the magnifying glass on Library to search by title or author
- **Sort** — recently added, recently read, title, author, or grouped by series
- **Series grouping** — tag a book with a series name in its detail sheet
- **Notes** — tap the pencil while reading to jot a note tied to your current spot; view
  them all from a book's detail sheet → "View notes"
- **Reading Goals** — a yearly goal ring (like Apple Books), pace estimate, streak, and a
  year-over-year comparison chart
- **Backup & Restore** — Settings → Export downloads your whole library (books, progress,
  notes, shelves) as one file; Restore loads it back in, e.g. on a new phone

## Get it onto your phone (easiest: host it free, 2 minutes)

Because this needs a real web address to install properly and cache itself for offline use,
the simplest path is a free static host. **GitHub Pages** works well:

1. Create a free GitHub account if you don't have one.
2. Create a new repository (e.g. `shelf-app`), and upload these four items into it:
   `index.html`, `manifest.json`, `sw.js`, and the `icons` folder.
3. In the repo, go to **Settings → Pages**, set source to the `main` branch, root folder, and save.
4. GitHub gives you a URL like `https://yourname.github.io/shelf-app/`. Open that link
   on your Android phone in Chrome.
5. Tap Chrome's **⋮ menu → "Add to Home screen" → Install**.
6. Open it from your home screen icon — it now runs full-screen like a real app, and after
   that first visit it keeps working **with no internet connection at all.**

Other free static hosts work identically if you'd rather use one of those (e.g. Cloudflare
Pages, Netlify) — just upload the same four items to the root.

## Using it

- **Add a book** — tap the `+` in the top right, pick one or more `.epub`/`.pdf` files from
  your phone's storage.
- **Read** — tap a cover to open the detail sheet, then **Open**. Swipe/use the ‹ › buttons
  or drag the progress bar to move through the book.
- **Shelves** — organize books into custom shelves from the **Shelves** tab, and assign a
  book to one from its detail sheet.
- **Stats** — the **Stats** tab shows your reading streak, books finished this year, time
  spent reading, and a 18-week activity heatmap. Time is measured automatically while a book
  is open on screen.

## A note on "installable APK"

A real compiled `.apk` requires the Android SDK/Gradle build toolchain, which I couldn't
reach from my sandboxed build environment. This app is a **Progressive Web App (PWA)**
instead — once installed via "Add to Home screen," it looks and behaves like a native app
(own icon, full-screen, offline) with none of the download-and-track functionality missing.
If you later want a literal `.apk` file, the same code can be wrapped with a tool called
**Capacitor** on a machine that has Android Studio installed — happy to prepare that project
structure if you ever want to go that route.
