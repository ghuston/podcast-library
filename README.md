# Grant's Podcast Library — GitHub Pages

A static site: one `index.html` page, a `styles.css` file, and MP3s in `episodes/`.
No build step, no server, no database.

## Publish it (free, public repo)

1. Create a new public repository on GitHub (for example, `podcast-library`).
2. Upload everything in this folder to the repository root, including the
   empty `.nojekyll` file (it stops Jekyll from interfering with the MP3s).
   You can upload in the browser, or with git:
   ```
   git init
   git add .
   git commit -m "Podcast library"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/podcast-library.git
   git push -u origin main
   ```
3. In the repository: Settings → Pages → Build and deployment → Source:
   "Deploy from a branch", Branch: `main`, Folder: `/ (root)`.
4. Your site will be at `https://YOUR-USERNAME.github.io/podcast-library/`
   (or `https://YOUR-USERNAME.github.io/` if the repo is named
   `YOUR-USERNAME.github.io`).

## Add an episode

1. Copy its MP3 into `episodes/` (keep each file under 100 MB).
2. In `index.html`, copy an existing `<article class="card">` block,
   paste it at the top of `<main>`, and change the series, title, date,
   runtime, description, and MP3 file name.
3. Commit and push. Pages rebuilds automatically.

## Notes

- Total site size here is about 41 MB, well under GitHub Pages' 1 GB site limit.
- GitHub Pages on a free plan is public: anyone with the link can listen
  and download. There is no password gate on the free tier.
- The corrected Grok Bots guide and the coin grading / inventory episode
  currently live only as Library pages, so their audio is not in this
  GitHub version yet — but their research companions are, under `research/`.
  Add their audio the same way once exported.
