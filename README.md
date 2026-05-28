# M. Keerthi — Portfolio

## Deploy to Vercel (3 steps)

### Option A — Vercel CLI (fastest)
```bash
npm i -g vercel
cd keerthi-portfolio
vercel
```
Follow the prompts — done in ~30 seconds.

### Option B — Drag & Drop (no code needed)
1. Go to https://vercel.com/new
2. Sign up / log in (free)
3. Click **"Deploy"** → drag the entire `keerthi-portfolio` folder into the upload zone
4. Vercel gives you a live URL instantly (e.g. `keerthi-portfolio.vercel.app`)

### Option C — GitHub (recommended for updates)
1. Push this folder to a GitHub repo
2. Go to https://vercel.com/new → Import Git Repository
3. Select your repo → Deploy
4. Every `git push` auto-redeploys ✓

---

## What was optimised for speed

| Issue | Fix |
|-------|-----|
| Google Fonts blocked rendering | Converted to `preload` + async |
| Three.js blocked HTML parse | Added `defer` |
| Full resolution 3D on mobile | Mobile gets 1x pixel ratio, no shadows |
| 5 robot bots with PointLights on mobile | Reduced to 1 on mobile |
| 4 drones with PointLights on mobile | Reduced to 1 on mobile |
| 40 data particles | Reduced to 18 on mobile, 36 on desktop |
| antialiasing on mobile | Disabled (invisible on small screens) |
| Shadow map 1024px on mobile | Reduced to 512px |
| No GPU compositing hint | Added `will-change: transform` to canvas |
| Layout recalc on scroll | Added `contain: layout style` to sections |

## Before deploying — personalise these links in index.html
- `mailto:keerthi@email.com` → your real email
- `https://linkedin.com` → your LinkedIn URL  
- `https://github.com` → your GitHub URL
- Resume `href="#"` → link to your actual resume PDF
