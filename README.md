# DropSmart Website

Static multi-page website prototype for DropSmart, a water-awareness planning and guidance experience for households.

## Project Structure

```text
.
|-- index.html
|-- get-started/
|   `-- index.html
|-- how-it-works/
|   `-- index.html
|-- tips-learning/
|   `-- index.html
|-- help-support/
|   `-- index.html
|-- robots.txt
|-- sitemap.xml
|-- css/
|   |-- styles.css
|   |-- base/
|   |-- components/
|   |-- layout/
|   `-- pages/
`-- assets/
    `-- icons/
```

## Pages

- `index.html`: home page with hero, problem, solution, benefits, and CTA sections.
- `get-started/index.html`: static multi-step planning flow using hash targets and CSS `:has()` state.
- `how-it-works/index.html`: placeholder page shell.
- `tips-learning/index.html`: placeholder page shell.
- `help-support/index.html`: placeholder page shell.

## Running Locally

There is no build step. Open `index.html` directly, or run a simple static server from the project root:

```powershell
python -m http.server 8080
```

Then visit:

```text
http://localhost:8080/
```

## CSS Organization

- `css/styles.css` imports all CSS modules.
- `css/base/` contains reset, tokens, typography, and small utilities.
- `css/layout/` contains site layout, header, footer, containers, and section spacing.
- `css/components/` contains reusable UI pieces such as buttons, cards, icons, logo, and eyebrows.
- `css/pages/` contains page-specific styles for `home` and `get-started`.

## Conventions

- Internal navigation uses relative links so the site can work from a static folder.
- Shared styling should live in `components/` or `layout/` only after it is reused.
- Page-specific composition should stay in `css/pages/`.
- Cards are static by default. Add `interactive` to opt into hover motion.
- The get-started flow relies on modern CSS features, including native CSS nesting and `:has()`.
- Crawl metadata uses the GitHub Pages project URL, `https://silentlie.github.io/dropsmart-website/`, in canonical links, `robots.txt`, and `sitemap.xml`.

## Notes

- Google Fonts are loaded from the network.
- Form fields in the get-started flow are static prototype fields and do not submit data.
- If the site moves to a custom domain, update the canonical URLs, sitemap URLs, and `robots.txt` sitemap URL together.
