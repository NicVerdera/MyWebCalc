# Scientific Calculator & Math Reference

A single-page scientific calculator with a live "paper tape" step log, plus a
compiled formula reference (Algebra, Geometry, Trigonometry, General Math,
Probability, Statistics, Calculus) with worked, manual computations.

Everything lives in one static file — `index.html` (HTML + CSS + vanilla JS,
no build step, no dependencies).

## Deploy to Vercel

### Option A — Vercel CLI (fastest)

```bash
npm i -g vercel       # one-time install
cd scientific-calculator-repo
vercel                # follow the prompts (first deploy → preview URL)
vercel --prod         # promote to your production URL
```

### Option B — GitHub + Vercel dashboard

1. Push this folder to a new GitHub repo:
   ```bash
   cd scientific-calculator-repo
   git init
   git add .
   git commit -m "Initial commit: scientific calculator"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
2. Go to [vercel.com/new](https://vercel.com/new) and import the repo.
3. Framework preset: **Other** (no build command, no output directory needed —
   Vercel will serve `index.html` as a static site automatically).
4. Click **Deploy**.

### Option C — Drag and drop

Go to [vercel.com/new](https://vercel.com/new) and drag the
`scientific-calculator-repo` folder directly onto the page.

## Local preview

No build tools needed — just open `index.html` in a browser, or serve it
locally:

```bash
npx serve .
```

## Files

- `index.html` — the entire app (calculator + formula reference)
- `vercel.json` — minimal static-deploy config (clean URLs)
- `.gitignore` — standard ignores for the Vercel CLI / Git
