# Engineering Mathematics & BME — Study Site (Osmania University)

A self-contained static website for **BE Biomedical Engineering**, University College of
Engineering (Autonomous), **Osmania University** — mathematics papers I–IV plus the full
BME course syllabus and the C / Python / data-structures programming guide.

All deployable files live in the **`dist/`** folder. Open **`dist/index.html`** to start —
it's the hub that links every page.

## Structure

```
.
├── README.md              ← this file
└── dist/                  ← the website (deploy this folder)
    ├── index.html         ← landing hub (links everything)
    ├── syllabus.html      ← maths syllabus (I–IV) + semester study plan
    ├── tutorial.html      ← condensed maths quick-tutorial (all 20 units)
    ├── maths1-learn.html  ← Mathematics I  — learn & practice
    ├── maths2-learn.html  ← Mathematics II — learn & practice
    ├── maths3-learn.html  ← Mathematics III — learn & practice
    ├── maths4-learn.html  ← Mathematics IV — learn & practice
    ├── bme-syllabus.html  ← full BE Biomedical Engineering syllabus (8 semesters)
    ├── programming.html   ← C, Python & data structures guide
    └── .nojekyll          ← makes GitHub Pages serve files as-is
```

Every page has a link back to the hub (a **⌂ Hub** button, or a **Back to Study Hub** bar
on the BME syllabus and programming pages).

## Deploy to tiiny.host

Point tiiny.host at the **`dist/`** folder:

1. Zip the **contents of `dist/`** so that `index.html` is at the **top level** of the zip.
   The included `bme-maths-site.zip` contains the whole project; if you prefer, zip only the
   inside of `dist/` and upload that.
2. Go to <https://tiiny.host> → **Upload** → select the zip.
3. Name the site and publish. `index.html` loads automatically as the home page.

## Deploy to GitHub + GitHub Pages

```bash
git init
git add .
git commit -m "OU BME study site: maths I–IV, BME syllabus, programming guide"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

Then enable Pages: **Settings → Pages → Build and deployment → Source: Deploy from a
branch → Branch: `main`, Folder: `/dist` → Save.** The site appears at
`https://<your-username>.github.io/<repo-name>/`. The `.nojekyll` file inside `dist/`
ensures Pages serves everything as plain static files.

## Notes

- **Internet:** the maths pages (`tutorial.html` and the four `mathsN-learn.html` modules)
  load MathJax and Google Fonts from a CDN, so they need a connection to render equations.
  `syllabus.html`, `bme-syllabus.html` and `programming.html` work essentially offline
  (only web fonts load remotely).
- **Printing:** every page prints cleanly; the learn modules reveal all practice solutions
  when printed, so you can make paper revision sheets.
- Worked examples and practice questions in the maths modules are **illustrative** standard
  problems written to teach each method — pair them with the prescribed textbooks and past
  Osmania University question papers.
- **Maths IV:** UCE publishes a single Mathematics-IV paper (BS 401 MT); BME follows this
  standard fourth course. Confirm against the printed BME IV-semester scheme in case of a
  branch-specific revision.
- `bme-syllabus.html` is sourced from the official UCE Osmania BME department page; check
  that page for the latest scheme-of-instruction PDFs.

*Compiled study reference — not an official university publication. Prepared 05 July 2026.*
