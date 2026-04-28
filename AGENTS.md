# AGENTS.md

This is a static website for [recent-writings](https://recent.poscic.net) — a personal portfolio showcasing music journalism and reviews.

## Project Structure

```
recent-writings/
├── index.html      # Main page with article entries
├── css/
│   └── style.css   # All styles (no external frameworks)
├── images/         # (optional) locally stored images
└── favicon.ico
```

## No Build System

This is a plain static site — no build tools, no npm/package.json, no tasks. Just raw HTML and CSS.

## Commands

- **Preview locally**: Open `index.html` directly in browser, or serve with any static server (e.g., `python -m http.server 8000`)
- **Deploy**: Push to the `master` branch of the [recent-writings](https://github.com/antonio-poscic/recent-writings) repo — GitHub Pages auto-deploys from root

## Patterns

- Entries are hardcoded in `index.html` — add new writing by copying an existing `.entry` block
- Images are hotlinked from external sources (substack, thequietus, thewire.co.uk) — add new images by copying the URL pattern from existing entries
- CSS uses BEM-adjacent naming (`.entry`, `.entry-link`, `.entry-title`)
- Fonts: Space Mono from Google Fonts
- Color palette: Dark theme (`#333333` background), teal accents (`#4893a5`)

## Gotchas

- External image URLs may break if the source removes the image — there's no local fallback mechanism
- No responsive images — uses `max-width: 200px` for desktop, `width: 100%` for mobile
- CSS comments use `/*noinspection*/` — likely from an IDE auto-format, not standard comment syntax