# vamos-web

Marketing site and legal pages for [readyvamos.com](https://readyvamos.com). Static HTML, deployed via Vercel. No build step required.

## Pages

| Route | File | Description |
|-------|------|-------------|
| `/` | `vamos-landing.html` | Main landing page |
| `/apply` | `coach-form.html` | Founding coach application form |
| `/coaches` | `coaches.html` | Founding coaches directory |
| `/privacy` | `privacy.html` | Privacy policy |
| `/terms` | `terms.html` | Terms of service |
| `/thanks` | `thanks.html` | Post-application confirmation |

Routes are defined in `vercel.json` as rewrites.

## Assets

All web assets live in `assets/logos/`. Only SVGs are used — no PNGs are in the repo.

| File | Used by |
|------|---------|
| `Vamos-Icon.svg` | All pages (favicon) |
| `Vamos-Lockup-Orange.svg` | Landing page nav |
| `Vamos-Mark-White.svg` | Landing page footer |
| `Vamos-Lockup-Black.svg` | Available (unused) |
| `Vamos-Lockup-Color.svg` | Available (unused) |
| `Vamos-Lockup-Primary-AllWhite.svg` | Available (unused) |
| `Vamos-Lockup-White.svg` | Available (unused) |
| `Vamos-Mark-Black.svg` | Available (unused) |

> **Note:** `assets/vamos-landing.css` exists but is not linked in any HTML file. It appears to be an extracted copy of the inline styles from `vamos-landing.html`. Either wire it up as an external stylesheet or delete it.

## Local development

Open any `.html` file directly in a browser, or serve locally to test routing:

```bash
npx serve .
```

Then visit `http://localhost:3000`.

## Deployment

Deploys automatically to [readyvamos.com](https://readyvamos.com) via Vercel on push to `main`. No build step — Vercel serves the static files directly using the rewrites in `vercel.json`.

## Tech stack

- Plain HTML/CSS/JS — no framework, no bundler
- Fonts: Inter, Special Gothic Expanded One, Caveat (Google Fonts)
- Form submission handled externally (form `action` attribute)
- Hosted on Vercel
