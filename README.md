# Ledger — Bangladesh Stock Market Fundamental Analysis

A single-page, static website that lets investors enter a company's raw
financial data once and automatically calculates 13 financial ratios and
9 valuation/scoring models (Piotroski F-Score, Altman Z-Score, Beneish
M-Score, Sloan Ratio, Ohlson O-Score, DuPont Analysis, Dividend Growth
Model, DCF, CAPM).

No backend, no build step, no dependencies — it's a single `index.html`
file that runs entirely in the browser.

## Files in this repo

- `index.html` — the entire website (HTML + CSS + JavaScript in one file)
- `vercel.json` — minimal Vercel config (clean URLs)
- `.gitignore`

## Deploy: GitHub → Vercel

**1. Push this folder to a new GitHub repository**

```bash
cd ledger-bd-analysis
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

(Replace `<your-username>/<your-repo>` with your actual GitHub username and
repository name. Create the empty repository on GitHub first if you
haven't already, at https://github.com/new — do not initialize it with a
README so the push above doesn't conflict.)

**2. Import the repo into Vercel**

1. Go to https://vercel.com and sign in (you can sign in directly with
   your GitHub account).
2. Click **Add New → Project**.
3. Select **Import Git Repository** and choose the repo you just pushed.
4. Vercel will auto-detect it as a static site — you don't need to set a
   Build Command or Output Directory. Leave those fields blank/default.
5. Click **Deploy**.

**3. Done**

Within a minute you'll get a live URL like
`https://your-repo-name.vercel.app`. Every time you push a new commit to
the `main` branch on GitHub, Vercel automatically redeploys the site.

## Custom domain (optional)

In your Vercel project, go to **Settings → Domains** and add your own
domain (e.g. `ledgerbd.com`). Vercel will show you the DNS records to add
at your domain registrar.

## Updating the site later

Edit `index.html` directly (all the ratio/model logic, field labels, and
styling live in that one file — search for `SECTIONS` for the input
fields and `METRICS` for the calculation logic), then:

```bash
git add .
git commit -m "Update site"
git push
```

Vercel redeploys automatically.
