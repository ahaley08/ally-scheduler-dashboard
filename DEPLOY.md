# Deployment Guide — Ally Scheduler Dashboard

## What You're Deploying

A single HTML file hosted as a static website on Render (free tier).
No server. No database. No coding required after this setup.

---

## Step 1 — Create a GitHub Account (if you don't have one)

1. Go to https://github.com
2. Click **Sign up** and create a free account
3. Verify your email

---

## Step 2 — Create a New GitHub Repository

1. Log into GitHub
2. Click the **+** icon (top right) → **New repository**
3. Fill in:
   - **Repository name:** `ally-scheduler-dashboard`
   - **Visibility:** Private ✅ (keep it private — internal tool)
   - Leave everything else unchecked
4. Click **Create repository**
5. You'll land on an empty repo page — leave this tab open

---

## Step 3 — Upload the Files to GitHub

You have 4 files to upload:
- `index.html`
- `render.yaml`
- `README.md`
- `.gitignore`

**Upload method (no Git knowledge required):**

1. On your empty repo page, click **uploading an existing file**
   (or drag files directly onto the page)
2. Drag all 4 files into the upload area
3. Scroll down, add a commit message like `Initial deploy`
4. Click **Commit changes**

Your repo is now ready.

---

## Step 4 — Create a Render Account

1. Go to https://render.com
2. Click **Get Started for Free**
3. Sign up with your GitHub account (easiest — links them automatically)

---

## Step 5 — Deploy to Render

1. In Render dashboard, click **+ New** → **Static Site**
2. Click **Connect a repository**
3. Find `ally-scheduler-dashboard` in the list and click **Connect**
4. Render will auto-detect the `render.yaml` file and fill in settings
5. Check the settings:
   - **Name:** ally-scheduler-dashboard (or whatever you like)
   - **Branch:** main
   - **Publish directory:** `.`
   - **Build command:** (leave blank)
6. Click **Create Static Site**

Render will deploy in about 30 seconds.

---

## Step 6 — Get Your URL

Once deployed, Render gives you a URL like:
```
https://ally-scheduler-dashboard.onrender.com
```

**Share this URL with your team.** That's the app.

---

## Updating the Dashboard in the Future

When you get an updated `index.html` from Claude:

1. Go to your GitHub repo
2. Click on `index.html`
3. Click the **pencil icon** (Edit) — or drag the new file to replace it
4. Commit the change
5. Render auto-deploys within ~30 seconds

---

## Notes on Data Storage

- Each person's logged entries save to **their own browser's localStorage**
- This means: data entered on one computer does NOT appear on another computer
- The March 2026 historical data is baked into the file itself — it loads for everyone
- If you need shared/cloud data across devices, that requires a database upgrade
  (ask Claude to add a backend when you're ready)

---

## Free Tier Limits (Render Static Sites)

- ✅ Unlimited deploys
- ✅ Custom domain (optional)
- ✅ HTTPS included
- ✅ No credit card required
- ⚠️ Site may "spin down" after 15 min of inactivity on free tier
  (first load after inactivity takes ~30 sec — static sites don't spin down,
  only web services do, so this does NOT apply here)

Static sites on Render are always-on with no spin-down. You're good.
