# cindypan.github.io

Static HTML/CSS academic site for Cindy Pan (Assistant Professor of Finance,
Susquehanna University). No build step, no dependencies besides the Google
Fonts CDN.

## Structure
```
index.html      About
research.html   Research
teaching.html   Teaching
service.html    Service
assets/style.css
assets/avatar-placeholder.svg   ← replace with an actual photo
```

## Before you deploy
- Replace `assets/avatar-placeholder.svg` with a real photo. Save it as
  e.g. `assets/photo.jpg`, then in `index.html` change:
  `<img class="avatar" src="assets/avatar-placeholder.svg" ...>`
  to
  `<img class="avatar" src="assets/photo.jpg" alt="Cindy Pan">`

## Deploy to GitHub Pages

Because the repo is named `cindypan.github.io`, GitHub Pages will treat it
as a **user site** and serve it at the domain root once Pages is enabled —
no `/reponame/` path segment, and no branch/folder ambiguity to get wrong.

1. Create the repository on GitHub named exactly `cindypan.github.io`
   (Settings can't rename this later without changing the live URL).
2. Upload files via the web UI:
   - On the repo's main page, click **Add file → Upload files**.
   - Drag in `index.html`, `research.html`, `teaching.html`, `service.html`,
     `README.md`, and the `assets` folder (drag the folder itself so the
     `assets/` path is preserved).
   - Scroll down, add a commit message ("Initial site"), click
     **Commit changes**.
3. Enable Pages:
   - Repo → **Settings** → **Pages** (left sidebar).
   - Under "Build and deployment," set **Source** to `Deploy from a branch`,
     branch `main`, folder `/ (root)` → **Save**.
4. Wait 1–5 minutes, then visit **https://cindypan.github.io/**.

## If you get a 404
- Confirm the repo name is exactly `cindypan.github.io` (case-sensitive,
  no typos) — GitHub only auto-serves at the root domain for a repo with
  this exact naming pattern.
- Confirm `index.html` sits at the **root** of the repo, not inside a
  subfolder (e.g. not `cindypan.github.io/site/index.html`).
- Confirm the Pages source branch matches the branch you actually pushed
  to (commonly `main`; older repos sometimes default to `master`).
- GitHub Pages builds can take a few minutes after the first commit —
  refresh the Settings → Pages screen to see the "your site is live at…"
  banner before assuming it failed.
