# DocScan – Deployment Guide

## What's in this folder

| File | Purpose |
|---|---|
| `index.html` | The full app (camera, PDF, sharing) |
| `manifest.json` | Makes it installable on iPhone |
| `sw.js` | Service worker — offline support |
| `vercel.json` | Vercel hosting config |
| `icon-192.png` | App icon (home screen) |
| `icon-512.png` | App icon (large) |

---

## Step 1 – Put it on GitHub

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **New repository** → name it `docscan` → click **Create repository**
3. On your computer, open the folder where these files are saved
4. Drag all the files into the GitHub page (it accepts drag & drop), or use:
   ```bash
   git init
   git add .
   git commit -m "Initial DocScan app"
   git remote add origin https://github.com/YOUR_USERNAME/docscan.git
   git push -u origin main
   ```

---

## Step 2 – Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign in with your GitHub account
2. Click **Add New → Project**
3. Select your `docscan` repository
4. Leave all settings as-is (no build command needed)
5. Click **Deploy** — done in ~30 seconds!

You'll get a URL like: `https://docscan.vercel.app`

---

## Step 3 – Install on iPhone

1. Open the Vercel URL in **Safari** on your iPhone
2. Tap the **Share button** (box with arrow) at the bottom
3. Scroll down and tap **"Add to Home Screen"**
4. Tap **Add** — DocScan is now on your home screen like a real app!

---

## How to use

1. Open DocScan from your home screen
2. Tap **Scan Document** → your camera opens
3. Take a photo of your document
4. Tap **Add Another Page** to scan more pages
5. Tap **Create PDF** — the app enhances and compiles everything
6. Tap **Download PDF** or **Share to WhatsApp**

---

## Notes

- Works **offline** after first visit (service worker caches everything)
- All processing happens **on your phone** — nothing is uploaded to any server
- WhatsApp sharing uses iOS's native share sheet (requires iOS 15+)
