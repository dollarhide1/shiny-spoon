# Nursing Study Style 🧠

An interactive **learning-style quiz + printable success guide** for nursing students.
This repo contains a marketing **landing page** (for GitHub Pages / Netlify) and the **product** itself (sold on Payhip for **$12 one-time**).

---

## 📁 What's in this folder

| File | What it is | Where it goes |
|------|------------|---------------|
| `index.html` | The landing / sales page | GitHub Pages + Netlify |
| `demo.html` | **Free live demo** — quiz + teaser result + buy CTA | GitHub Pages + Netlify (this is what "Try the demo" links to) |
| `guide.html` | The **full paid product** (quiz + complete guide + printable PDF) | Upload to **Payhip** as the download |
| `assets/payhip-cover.png` | Square 1080×1080 cover | Upload as the **Payhip product image** |
| `assets/og-image.png` | 1200×630 social-share image | Used automatically by the landing page |
| `favicon.svg` | Site icon | Auto-used by the pages |
| `netlify.toml` | Netlify config (no build step) | Netlify |
| `.gitignore` | Housekeeping | GitHub |

> **Free demo vs. paid product:** `demo.html` gives visitors the fun quiz, their learning style, and **3 sample tips** — then prompts them to buy. The full strategies, all the tip sections, and the printable PDF live only in `guide.html`, which you sell on Payhip. The public site never links to `guide.html`, so the paid content isn't given away.

---

## 🔑 STEP 0 — Payhip link (already wired in ✅)

The buy buttons are **already pointing at your live product:**
`https://payhip.com/b/op0TD`

Nothing to change to start selling. If you ever need to point them somewhere else, open
`index.html` and find & replace `op0TD` with your new product ID (the part after `/b/` in the
product URL). There are 4 buy buttons (top bar, hero, pricing, final CTA) — one replace covers them all.

> The page includes Payhip's `payhip.js`, so the buttons open a smooth **overlay checkout**.
> If the script ever fails, they fall back to a normal link to your product page.

---

## 🐙 STEP 1 — Put it on GitHub

```bash
# from inside this folder
git init
git add .
git commit -m "Nursing Study Style — landing page + product"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/nursing-study-style.git
git push -u origin main
```

### (Optional) Free hosting with GitHub Pages
- On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**
- Branch: `main`, folder: `/ (root)` → **Save**
- Your site goes live at `https://YOUR_USERNAME.github.io/nursing-study-style/`

---

## 🌐 STEP 2 — Deploy on Netlify

**Easiest (drag & drop):**
1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Deploy manually**
2. Drag this whole folder onto the page. Done — you get a live URL instantly.

**Connected to GitHub (auto-deploys on every push):**
1. **Add new site → Import an existing project → GitHub** → pick your repo.
2. Build command: *(leave blank)* · Publish directory: `.` → **Deploy**.
3. `netlify.toml` is already set up, so no other config is needed.

**Custom domain:** Netlify → **Domain settings → Add a domain** and follow the prompts.

---

## 🛒 STEP 3 — Sell it on Payhip

1. [payhip.com](https://payhip.com) → **Add new product → Digital product**.
2. **Upload file:** `guide.html` (that's what the buyer downloads).
   - *Tip:* you can also zip it first if you'd like to add a short "how to open" note — see below.
3. **Price:** `12.00` · set currency to USD · one-time (Payhip products are one-time by default).
4. **Cover image:** upload `assets/payhip-cover.png`.
5. **Title & description:** copy from the next section.
6. Publish, then copy the product link and go back to **Step 0**.

### Suggested Payhip listing copy

**Title:**
> Nursing Study Style — Learning Quiz + Printable Success Guide

**Short description:**
> Find your learning style and study the way your brain actually works.

**Full description:**
> Nursing school is hard enough without forcing study methods that don't fit you.
>
> This interactive guide starts with a quick 8-question quiz that reveals whether you learn best by **seeing, hearing, reading, or doing** — then reshapes itself around your result with strategies built for *your* brain.
>
> **What's inside:**
> • 🧠 8-question learning-style quiz
> • 📚 Study, note-taking & organization strategies for your style
> • ✅ NCLEX prep mindset & high-yield priorities
> • 🏥 Clinical prep, communication & debrief routines
> • 😴 Self-care, time management & mindset tips
> • 📄 One-click **printable PDF**, personalized to your result
>
> Works on phone, tablet, and laptop. No app, no account — just open and go.
>
> *This is a general study-skills resource for nursing students. It is not affiliated with the NCLEX® or NCSBN, and is not medical or academic advice — always follow your program's official guidance.*

### (Optional) Zip the product before uploading
```bash
zip nursing-study-guide.zip guide.html
```
Upload the `.zip` instead of the raw HTML if you prefer giving buyers a tidy download.

---

## 🎨 Brand reference
- **Fonts:** Fraunces (headlines) + DM Sans (body)
- **Colours:** lavender `#B7A6EE` · sky `#9CCDF2` · mint `#92DEBC` · peach `#FFC3A0` · butter `#FBE08C`
- **Canvas:** `#FBF8FF` · ink `#39334F`

## 🔧 Notes
- Everything is plain static HTML/CSS/JS — no build tools, no dependencies.
- The free demo (`demo.html`) only reveals the learning style + 3 tips, so it drives sales without giving away the paid guide. To remove it entirely, delete the **"Try the live demo"** button + footer link in `index.html` and don't deploy `demo.html`.
- Keep `guide.html` **off** the public site (it's the Payhip download). This GitHub-ready folder intentionally does **not** include it — upload `guide.html` straight to Payhip from your original copy.

---
Made with 💜 for nursing students.
