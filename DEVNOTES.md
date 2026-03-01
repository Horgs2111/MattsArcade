# DEVNOTES.md

Developer notes for the MattsArcade repository.

## Project Purpose

Matt's game homepage — a static website that serves as a hub linking to various games under development.

## Development

No build step. Open `index.html` directly in a browser to preview, or use a simple local server:

```bash
# Python (if available)
python -m http.server 8000

# Node (if available)
npx serve .
```

## Deploying

The `deploy/` folder is what Netlify serves. After every change to `index.html` or `screenshots/`, copy the updated files into `deploy/` before committing and pushing. Both `index.html` and `deploy/index.html` must always be kept in sync.

```bash
cp index.html deploy/index.html
```

## Stack

Static HTML/CSS/JS — no frameworks, no bundler, no package manager unless one is introduced later.
