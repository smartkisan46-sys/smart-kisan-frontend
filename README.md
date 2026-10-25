# Smart Kisan 🌱 — Maharashtra Farmer Weather, Crop Advisory & Mandi Portal

**Smart Kisan** is a responsive, multilingual (English, मराठी, हिंदी) agricultural weather and advisory web application built for farmers in **Maharashtra, India**.

---

## 1. Quick Start (Zero Build Required or Vite Dev Server)

### Option A: Instant Browser Launch (Simplest for Demo)
Open `index.html` directly in any desktop or mobile browser (Chrome, Edge, Firefox, Safari). Everything is self-contained and works immediately.

### Option B: Local Development Server with Vite
```bash
npm install
npm run dev
```

---

## 2. Connecting Your Credentials (Supabase & Optional APIs)

1. Click the **"⚙️ API & Cloud Setup"** button in the top-right banner of the website.
2. **Supabase (`farmer_profiles`)**:
   - Open your existing Supabase project dashboard → **Project Settings** → **API**.
   - Copy your **Project URL** (`https://<project-id>.supabase.co`) and your **Public `anon` key** (publishable key).
   - Paste both into the Setup modal and click **Save & Reconnect Services**.
   - *Security Rule*: Never place your `service_role` secret key in browser code.
3. **Live Weather Data**:
   - Smart Kisan connects automatically to the **Open-Meteo API** (`https://api.open-meteo.com/v1/forecast`) using the selected village's exact GPS coordinates—**no API key required** when your browser has internet access!
   - If offline, the website automatically falls back to clearly labelled **Demo Weather Data** and never pretends static numbers are live.

---

## 3. Deploying Safely to GitHub Pages (`SmartKiran-S/Smart-Kisan-`)

To publish to `https://smartkiran-s.github.io/Smart-Kisan-/` without losing any existing files in your repository:

```bash
# 1. Clone your existing repository first so current contents are preserved
git clone https://github.com/SmartKiran-S/Smart-Kisan-.git
cd Smart-Kisan-

# 2. (Optional) Create a backup branch of whatever is currently in the repo
git checkout -b backup-before-smart-kisan
git push origin backup-before-smart-kisan
git checkout main

# 3. Copy the files from smart_kisan_project.zip into the repository folder, then commit and push:
git add .
git commit -m "Add Smart Kisan interactive Maharashtra farmer weather website"
git push origin main
```

Then on GitHub:
1. Go to **Settings** → **Pages** in `https://github.com/SmartKiran-S/Smart-Kisan-`.
2. Under **Build and deployment**, select **Deploy from a branch** → Branch: `main` / `/ (root)` (or select **GitHub Actions** to use the included `.github/workflows/deploy-pages.yml`).
3. Within 1–2 minutes, your live website will be available at:
   `https://smartkiran-s.github.io/Smart-Kisan-/`
