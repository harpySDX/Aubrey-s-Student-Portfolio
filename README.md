# Aubrey Chen — Portfolio

A retro, liquid-glass portfolio with a walking pixel-pup mascot, plus a
Spotify-style algorithm visualizer as one of the projects.

```
.
├── index.html              ← the portfolio (start here)
├── visualizer/
│   └── index.html           ← the algorithm visualizer, linked from Projects
└── .github/workflows/
    └── pages.yml             ← auto-deploys to GitHub Pages on every push
```

Both pages are self-contained (HTML + CSS + JS in one file each, only Google
Fonts loaded externally) and link to each other with plain relative paths, so
the whole thing also works if you just double-click `index.html` on your own
computer — no build step, no server required.

## Deploy it to GitHub Pages

**Option A — GitHub Actions (already set up, recommended)**

1. Create a new repository on GitHub and push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
2. On GitHub, go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **GitHub Actions**.
4. That's it — the included workflow (`.github/workflows/pages.yml`) builds
   and deploys the site automatically on every push to `main`. Check the
   **Actions** tab for progress; your site will be live at
   `https://<your-username>.github.io/<repo-name>/` a minute or two later.

**Option B — plain GitHub Pages, no Actions**

1. Push the folder to GitHub the same way as above.
2. Go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, pick `main` and `/root`,
   then save.
4. Same URL, same result — just without the automatic workflow (you'd redo
   this step if you ever move to a different branch).

## Updating the site later

Edit `index.html` or `visualizer/index.html` directly, commit, and push —
Pages picks up the change automatically (within a minute or two with Option A,
almost instantly with Option B).

## Using a custom domain (optional)

Settings → Pages → **Custom domain**, enter your domain, and add the DNS
records GitHub shows you. GitHub will also offer to add a `CNAME` file to the
repo for you.
