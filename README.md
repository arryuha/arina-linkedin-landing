# Arina — LinkedIn mentoring (static site)

A single-page landing (`index.html`) with EN pages under `en/`, React tweak panel, and images in `uploads/`. No build step: open locally or host as static files.

## Publish on GitHub Pages (simplest)

1. Create a new **empty** repository on GitHub (any name, e.g. `linkedin-landing`).

2. In this folder, connect and push:

   ```bash
   git remote add origin https://github.com/YOUR_USER/YOUR_REPO.git
   git branch -M main
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages** → **Build and deployment** → **Source: Deploy from a branch** → Branch **main** → Folder **/ (root)** → Save.

4. The site will be at `https://YOUR_USER.github.io/YOUR_REPO/` (or your custom domain if you add a `CNAME` file in Settings → Pages).

If the page looks cached, do a hard refresh. Add an empty **`.nojekyll`** in the root (this repo has it) so GitHub does not run Jekyll on your static files.

## What to edit

- Contact links and Telegram: search for `SITE_CONTACT` and `t.me` in `index.html`.
- Hero / About images: `uploads/` (paths referenced in HTML).

## Local preview

```bash
python3 -m http.server 8000
```

Open `http://127.0.0.1:8000/`.
