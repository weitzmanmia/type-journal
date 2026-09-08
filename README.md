# Type Journal

A weekly typography field notebook by Mia Weitzman — ARTDES 210, Fall 2026.

This is a plain HTML/CSS site. No build step, no dependencies — just files.

## Structure

```
index.html            ← homepage (hero, about, schedule, entry archive)
style.css             ← all styling, shared across every page
entries/
  entry-00.html        ← the first real entry
  _template.html        ← blank copy to start each new week's entry
```

## Publish it for free with GitHub Pages

1. Create a free GitHub account at [github.com](https://github.com) if you don't have one.
2. Create a new repository (e.g. `type-journal`). Keep it public.
3. Upload all the files in this folder to that repository, keeping the same
   folder structure (`index.html` and `style.css` at the top level, the
   `entries` folder with its files inside it).
4. In the repository, go to **Settings → Pages**.
5. Under "Build and deployment," set **Source** to **Deploy from a branch**,
   pick the `main` branch and the `/ (root)` folder, then **Save**.
6. GitHub will give you a live URL, usually:
   `https://<your-username>.github.io/type-journal/`
   It can take a minute or two to go live the first time.

Every time you upload changed files afterward, the site updates automatically
within a minute or so — no re-deploying needed.

## Adding a new entry each week

1. Duplicate `entries/_template.html` and rename it, e.g. `entry-01.html`.
2. Open it and fill in the marked spots: entry number, date, category tag,
   specimen title, and your 50–100 word writeup.
3. Add your photo to the `entries` folder and swap the placeholder `<div>`
   for an `<img>` tag (the commented-out line shows the format).
4. Open `index.html` and add a new row inside `<div class="entry-list">`,
   copying the existing entry-00 row and pointing it at your new file.
   Put new entries at the top so the archive reads newest-first.
5. Update the "Next entry" / "Previous entry" links at the bottom of the
   entry pages so they connect to their real neighbors.
6. Upload the changed/new files to your GitHub repository — the live site
   updates automatically.

## Customizing

All colors, type, and spacing live in `style.css` as CSS variables at the
top (`--paper`, `--ink`, `--accent`, etc.) — change those to restyle the
whole site at once.
