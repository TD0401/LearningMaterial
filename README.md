# LearningMaterial

This is going to be a learning material website related to new stuff we want to learn.

Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and published to GitHub Pages at <https://td0401.github.io/LearningMaterial/>.

## Structure

```
docs/
├── index.md              # landing page
├── module-01-intro/
│   ├── index.md          # module overview
│   ├── lesson-01.md
│   └── images/           # images for this module
├── module-02-basics/
└── assets/               # shared images, downloads
templates/
└── lesson-template.md    # copy this to start each new lesson
mkdocs.yml                # site config and navigation
.github/workflows/deploy.yml
```

## Run locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Then open <http://127.0.0.1:8000>. The site reloads as you edit.

## Add a lesson

1. Copy `templates/lesson-template.md` to `docs/<module>/lesson-NN.md`.
2. Fill it in. Put images in that module's `images/` folder.
3. Add the lesson to `nav` in `mkdocs.yml` and to the module's `index.md`.

## Add a module

1. Create `docs/module-NN-name/` with an `index.md` and an `images/` folder.
2. Add it to `nav` in `mkdocs.yml` and to the table in `docs/index.md`.

## Deploy

Pushing to `main` builds and deploys the site via GitHub Actions.

One-time setup: in the GitHub repo go to **Settings → Pages** and set **Source** to **GitHub Actions**.
