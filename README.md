# sudozaid.wiki

Source for **[sudozaid.wiki](https://sudozaid.wiki)** — CTF writeups and offensive-security notes by Muhammad Zaid (`sudo-zaid`). Built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/).

## Preview locally

```bash
pip install -r requirements.txt
python -m mkdocs serve
```

Open <http://127.0.0.1:8000>. The site auto-reloads as you edit files in `docs/`.

## Add a writeup

1. Drop your `.md` file in `docs/ctf/<event>/` (create the event folder if new).
2. Add it to the `nav:` list in [`mkdocs.yml`](mkdocs.yml).
3. Commit and push — it deploys automatically.

## Deploy

Every push to `main` triggers `.github/workflows/deploy.yml`, which builds the site and publishes it to **GitHub Pages**. The custom domain `sudozaid.wiki` is set via [`docs/CNAME`](docs/CNAME).

**One-time setup on GitHub:**

1. Repo → **Settings → Pages → Build and deployment → Source → GitHub Actions**.
2. Repo → **Settings → Pages → Custom domain** → `sudozaid.wiki` → Save, then tick **Enforce HTTPS** once the certificate is issued.
3. At your DNS provider for `sudozaid.wiki`, add:
   - `CNAME` record: `www` → `sudo-zaid.github.io`
   - Four `A` records for the apex `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (or an `ALIAS`/`ANAME` on `@` → `sudo-zaid.github.io` if your DNS supports it)

## Structure

```
docs/
├── index.md                 # landing page
├── about.md
├── ctf/
│   ├── index.md             # events overview
│   └── cyberchess-2026/      # one folder per event
│       ├── index.md
│       └── 01-…18-*.md
└── stylesheets/extra.css    # gold-accent brand polish
```

---

Writeups are documented with the help of Claude Code, from screenshots and notes by Muhammad Zaid.
