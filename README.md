# Outpost — Premium Home Page

Single-file static site (`index.html`, no build step) built for the
Acdyon Technologies frontend challenge, Part 2.

## What's here
- `index.html` — the whole site (HTML + CSS + JS, no dependencies except
  Google Fonts, loaded via `<link>`).
- `DECISIONS.md` — the 1-page written explanation the assessment asks for.

## Run it locally
Just open `index.html` in a browser. No server, no build step.

## Deploy it (pick one — all free, all under 2 minutes)

### Option A — Netlify Drop (fastest, no account juggling)
1. Go to https://app.netlify.com/drop
2. Drag the whole `outpost` folder onto the page.
3. Copy the live URL it gives you.

### Option B — GitHub Pages (gives you the repo link too, in one step)
1. Create a new repo on GitHub, e.g. `outpost-home`.
2. From this folder:
   ```
   git add -A
   git commit -m "Outpost home page"
   git branch -M main
   git remote add origin https://github.com/<your-username>/outpost-home.git
   git push -u origin main
   ```
3. In the repo: Settings → Pages → Source: "Deploy from a branch" → Branch:
   `main`, folder `/ (root)` → Save.
4. Your live URL will be `https://<your-username>.github.io/outpost-home/`
   (takes ~1 minute to go live).

### Option C — Vercel
1. Go to https://vercel.com/new, import the GitHub repo from Option B
   (or drag-and-drop the folder if using the Vercel CLI: `vercel deploy`).
2. No build command needed — it's static HTML.

## Before you submit
- Open `index.html` and actually read it — the follow-up call grades
  whether you can defend every decision without "the AI suggested it."
- Fill in section 3 of `DECISIONS.md` honestly (see the comment inside it).
- Test at 390px and 1440px widths, and toggle dark/light mode, before
  you submit the link.
- Try the Konami code (↑ ↑ ↓ ↓ ← → ← → b a) on the live page for the
  bonus easter egg — harmless if you skip it, no points either way.
