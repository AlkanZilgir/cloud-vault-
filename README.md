# Cloud Vault — Private photo & file vault

A no-signup, no-cloud Progressive Web App for storing photos, videos and files privately on your own device.

## How it works

Cloud Vault has two storage modes. No server, no account, no upload — files never leave your machine.

### 1. Browser storage (default, works everywhere)
Files live in your browser's IndexedDB. Limited by the browser's per-site quota — usually a few GB up to ~10 GB depending on free disk and the browser.

### 2. Disk folder (unlimited)
Click **Connect a folder for unlimited storage** in Settings. The app saves every upload directly to a real folder on your hard drive using the File System Access API. Capacity = your free disk space. Existing browser files are migrated automatically.

> Disk folder mode works in Chrome, Edge and Opera on desktop. On Safari, Firefox and mobile the app falls back to browser storage — install it as a PWA there to get a larger quota.

Install Cloud Vault once and use it like a native gallery app.

---

## Features

- No signup, no sign-in — just open and use
- Connect a real disk folder for unlimited capacity (Chrome / Edge desktop)
- Photos, videos, documents — anything
- Auto-generated thumbnails for fast gallery scrolling
- Built-in storage usage meter
- Drag & drop or tap to upload
- Multi-select for batch delete or export
- Full-screen image & video lightbox
- Persistent storage request (browser mode)
- Works offline as a PWA
- Dark / light mode follows your system
- Export everything back to your device anytime

---

## Run it

It's a single static page. Two ways to use it:

### A) Open locally
Just double-click `index.html` — most features work, but service workers and `navigator.storage.persist()` need a real origin.

### B) Serve over HTTP (recommended)
From the project folder:

```bash
# Python 3
python -m http.server 8080
```

Then visit `http://localhost:8080`.

### C) Deploy to GitHub Pages
Push the folder to a GitHub repo, then in **Settings → Pages** pick the `main` branch and `/ (root)`. Your app will be live at `https://<you>.github.io/<repo>`.

---

## Install on your phone

### iPhone (Safari)
1. Open the URL in Safari
2. Tap **Share** → **Add to Home Screen**

### Android (Chrome / Edge)
1. Open the URL
2. Tap the menu → **Install app** or **Add to Home Screen**

Installed apps get a much larger storage quota and the OS won't evict the data.

---

## Storage notes

- Modern browsers give a single site somewhere between a few hundred MB and several GB by default. Cloud Vault shows the actual estimate in **Settings**.
- Click **Request persistent storage** in Settings so the browser won't auto-clear your vault if disk is low.
- Files are not encrypted at rest — they sit in your normal browser profile. Treat this app like a local folder.

---

## Tech

- Pure HTML, CSS, vanilla JS — no build step, no dependencies (Tabler Icons via CDN)
- IndexedDB for blob storage (images, videos, files all stored directly)
- Service worker for offline support
- Web Share API for sharing files where supported
