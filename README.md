# davidawatkit.github.io

My personal portfolio: plain HTML, CSS and vanilla JS with a Frutiger Aero look. There's no build step and no dependencies other than Google Fonts.

## Structure

```
index.html                 ← all content lives here
css/style.css              ← theme tokens at the top (light + dark)
js/main.js                 ← theme toggle, mobile nav, scroll reveal, bubbles, counters
favicon.svg
.nojekyll                  ← tells GitHub Pages to serve files as-is
assets/
  resume/David_Watkins_Resume.pdf
  img/
    profile.jpg            ← YOUR PHOTO GOES HERE
    og-image.jpg           ← optional link-preview image (1200×630)
    projects/              ← project screenshots
    side-quests/           ← travel & camping photos
```

## Adding your images

Any image that's missing falls back to a glossy placeholder, so you can add them in any order. Filenames are **case-sensitive** on GitHub Pages.

| Where it shows | Drop the file at | Suggested size |
|---|---|---|
| Hero portrait (circle crop) | `assets/img/profile.jpg` | Square, ~800×800, face centered |
| NOMAD card | `assets/img/projects/nomad.jpg` | 16:10, ~1200×750 |
| MLB Scouting Assistant | `assets/img/projects/mlb-scouting.jpg` | 16:10 |
| mlb-alpha | `assets/img/projects/mlb-alpha.jpg` | 16:10 |
| Brewed Wins | `assets/img/projects/brewed-wins.jpg` | 16:10 |
| Decaf Compiler | `assets/img/projects/decaf.jpg` | 16:10 |
| Momentum Tracking | `assets/img/projects/momentum.jpg` | 16:10 |
| "Out there" photos | `assets/img/side-quests/trip-1.jpg` … `trip-6.jpg` | 4:3, ~1200×900 |

After adding travel photos, search `index.html` for `edit me` and replace the captions and `alt` text (e.g. `alt="Sunrise over Lake Superior from the Porcupine Mountains"`).

To use `.png` or `.webp` instead, change the `src` in `index.html` to match. Keep photos under ~400 KB each; [squoosh.app](https://squoosh.app) works well for this.

## Deploying to GitHub Pages

1. Create a public repo named exactly **`davidawatkit.github.io`**.
2. Push the contents of this folder to the root of the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/davidawatkit/davidawatkit.github.io.git
   git push -u origin main
   ```
3. In the repo, go to **Settings → Pages → Build and deployment**, choose **Deploy from a branch**, then `main` / `(root)`.
4. After a minute or two, the site is live at **https://davidawatkit.github.io**.

All paths are relative, so the site also works from a project repo (e.g. `/portfolio/`) or opened locally.

## Previewing locally

```bash
python3 -m http.server 8080
```
Then open http://localhost:8080.

## TODOs

- [ ] Add `assets/img/profile.jpg`
- [ ] Add project screenshots and travel photos, then edit the captions
- [ ] Name and link the contracting marketplace in the "Currently Exploring" section (search for `TODO`)
- [ ] Add a live demo link for Brewed Wins once it's deployed
- [ ] Add a phone-free résumé at `assets/resume/David_Watkins_Resume.pdf`, then delete the `hidden` attribute from the two résumé buttons in `index.html` (search for `hidden`)
