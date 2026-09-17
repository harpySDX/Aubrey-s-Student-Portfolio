# Aubrey Chen — Portfolio

A retro, liquid-glass, winter-themed portfolio with a walking pixel-pup mascot
and a built-in Spotify-style algorithm visualizer — all in one page.

```
.
├── index.html              ← the whole site (start here)
└── .github/workflows/
    └── pages.yml             ← auto-deploys to GitHub Pages on every push
```

Everything — the trail, About/Projects/Skills/Blog/Achievements, and the
Algorithm Visualizer — lives in this single self-contained HTML file (only
Google Fonts loaded externally). The Visualizer is reached the same way as
every other page: click "View project" on the Projects page. No separate
pages, no folders to keep in sync — just the one file.

It also works if you just double-click `index.html` on your own computer —
no build step, no server required.

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

Edit `index.html` directly, commit, and push — Pages picks up the change
automatically (within a minute or two with Option A, almost instantly with
Option B).

## A note on file size

The file embeds a handful of photos (achievement certificates, event photos,
the coffee-shop scene art) directly as base64 data, so it's a few megabytes —
that's normal and expected, and GitHub Pages has no problem serving it.

## Using a custom domain (optional)

Settings → Pages → **Custom domain**, enter your domain, and add the DNS
records GitHub shows you. GitHub will also offer to add a `CNAME` file to the
repo for you.
