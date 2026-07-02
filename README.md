# Justin Knowles — Developer Portfolio

A responsive, single-page portfolio website (plain HTML/CSS/JS — no build step, no
dependencies) plus a print-ready PDF version. Built to showcase real, deployed software
for job applications.

```
portfolio/
├── index.html        The portfolio page
├── styles.css        All styling (incl. a print/PDF stylesheet)
├── script.js         Mobile nav + project category filter
├── portfolio.pdf     Generated PDF version (attach to applications)
└── README.md         This file
```

## View it locally

Just open `index.html` in any browser — no server needed.

Optional local server (nicer for testing):

```bash
# from the portfolio/ folder
python -m http.server 8000
# then visit http://localhost:8000
```

## Regenerate the PDF

The site has a dedicated print stylesheet, so the cleanest PDF comes straight from the
browser: open `index.html`, press **Ctrl+P**, and choose **Save as PDF** (Background
graphics ON, margins Default).

To regenerate it from the command line with Edge (headless):

```powershell
& "C:\Program Files (x86)\Microsoft\Edge\Application\msedge.exe" `
  --headless --disable-gpu --no-pdf-header-footer `
  --print-to-pdf="C:\Users\Justi\projects\portfolio\portfolio.pdf" `
  "file:///C:/Users/Justi/projects/portfolio/index.html"
```

## Deploy it free (recommended: GitHub Pages)

A live link is worth a lot on an IT job application. Steps:

1. Create a **public** repo on GitHub, e.g. `JayKnows242/portfolio`.
2. Push these files:
   ```bash
   cd C:/Users/Justi/projects/portfolio
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/JayKnows242/portfolio.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Source: `main` / root → Save**.
4. Your site goes live at **https://jayknows242.github.io/portfolio/** in ~1 minute.
   (Optionally rename the repo to `JayKnows242.github.io` to serve it at the root domain.)

Alternatives: drag the folder onto [Netlify Drop](https://app.netlify.com/drop), or point
Render/Cloudflare Pages at the repo.

## ⚠️ Before you send it — fill these in

I used placeholders where I didn't have the info. Search the files for these and update:

- ~~Phone~~ ✅ set to (242) 825-5000 / (242) 477-3377, with a WhatsApp link.
- ~~Email~~ ✅ set to Justin_knowles1@outlook.com.
- ~~LinkedIn~~ ✅ linkedin.com/in/justin-knowles1 (hero, About, and Contact).
- **Location** — set to "Nassau, The Bahamas". Adjust if needed.
- **Project stats** ("10+ projects", "3 deployed") — in the hero; tweak to taste.
- **Screenshots** (optional but high-impact) — add images of BahamUs, Smart Camera Hub, etc.
  to make cards pop. I can wire these in if you drop them in an `assets/` folder.
- **Live links** — BahamUs and AXON are linked. Add Perfect Puff's live URL if you want it public.

## Notes

- The three projects marked private on GitHub (BahamUs, Perfect Puff, Stream Backpack) are
  described but not linked to source, which is appropriate for client/commercial work.
- The color scheme (aquamarine + gold on navy) is a subtle nod to the Bahamian flag.
