# msisaif.github.io

Personal portfolio of Md Saiful Islam, built with [Alo](https://github.com/msilabs/alo), a small static site framework. The build produces plain HTML, CSS and JS, so it runs on any static host.

Live site: https://msisaif.github.io

## Run it

Node.js 22 or newer is required.

```bash
npm install
node alo dev      # dev server with live reload on http://localhost:3000
node alo build    # production build into dist/
```

## Project layout

```
pages/        layout.alo (head, nav, footer) and page.alo (the sections)
components/   one component per section: Hero, About, Experience, ...
data/         all editable content as JSON
global/       shared CSS: base, shared styles, theme colors
public/       files copied as they are: photo, favicon, social image
```

## Editing content

Text lives in `data/*.json`, so most changes need no template edits:

| File | Content |
| --- | --- |
| `site.json` | site name, title, description, URL, location |
| `hero.json` | name, role, lead line, chips, stats |
| `about.json` | About paragraphs and side cards |
| `experience.json` | roles, companies, volunteering |
| `open-source.json` | packages |
| `skills.json` | skill rows |
| `certifications.json` | certifications and credential links |
| `links.json` | LinkedIn, GitHub and msilabs links |

## Theme

The menu has a dark/light switch and an accent color picker with six presets and a custom color. The choice is saved in `localStorage`. Colors are CSS variables in `global/theme.css`.

## Deploy

Pushing to `main` builds and deploys the site with GitHub Pages (`.github/workflows/pages.yml`). In the repository settings, set Pages to deploy from GitHub Actions.
