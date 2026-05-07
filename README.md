# ☁️ Cloud Vault — Personal Cloud Storage App

Store photos, videos, and files in the cloud without using any phone storage.

## How it works
Your files are uploaded to **Cloudinary** (free cloud storage service). The app is a **PWA** (Progressive Web App) — meaning you install it on your phone like a real app, but it lives on the web.

---

## 🚀 Step-by-step: Deploy to GitHub Pages

### Step 1 — Create a GitHub account
Go to [github.com](https://github.com) and sign up (free).

### Step 2 — Create a new repository
1. Click the **+** button → "New repository"
2. Name it: `cloud-vault`
3. Set it to **Public**
4. Click **Create repository**

### Step 3 — Upload the files
1. Click **"uploading an existing file"** on the repository page
2. Drag and drop ALL these files into the box:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
3. Click **"Commit changes"**

### Step 4 — Enable GitHub Pages
1. Go to **Settings** (in your repository)
2. Click **Pages** in the left sidebar
3. Under "Source", select **main** branch → **/ (root)**
4. Click **Save**
5. Wait ~1 minute, then your app URL will appear:  
   `https://YOUR-USERNAME.github.io/cloud-vault`

---

## 📱 Install on your phone

### iPhone (Safari):
1. Open your GitHub Pages URL in Safari
2. Tap the **Share** button (box with arrow)
3. Scroll down → tap **"Add to Home Screen"**
4. Tap **Add** — the app appears on your home screen!

### Android (Chrome):
1. Open your GitHub Pages URL in Chrome
2. Tap the **three dots** menu
3. Tap **"Add to Home Screen"** or **"Install app"**
4. Tap **Add** — done!

---

## ☁️ Connect Cloudinary (free storage)

1. Sign up free at [cloudinary.com](https://cloudinary.com/users/register_free)
2. Copy your **Cloud name** from the dashboard
3. Go to **Settings → Upload → Upload presets**
4. Click **Add upload preset** → set Signing mode to **Unsigned** → Save
5. Copy the preset name
6. Open your Cloud Vault app → enter both values → tap Connect

**Free plan includes:** 25 GB storage + 25 GB bandwidth/month

---

## ⚠️ About deleting files

Removing a file from your vault **removes it from the app's gallery** but the file **stays on Cloudinary's servers**. To fully delete a file from the cloud, go to your [Cloudinary Media Library](https://cloudinary.com/console/media_library).

---

## Features
- 📸 Upload photos directly from camera
- 🎥 Upload videos and documents
- 🖼️ Beautiful photo gallery with filters
- 🔗 Share file links with anyone
- 📲 Works offline (PWA)
- 🌙 Dark/light mode automatic
- 💾 Zero phone storage used
