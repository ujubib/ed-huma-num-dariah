# Research Infrastructures for the Digital Humanities

**Quarto website + Reveal.js presentation**  
UPPA ED 481 SSH & UNITA CHORAL Programme — 16 march 2026

## Project Structure

```
.
├── _quarto.yml              # Website project config (journal theme, sidebar, footer)
├── _brand.yml               # UPPA brand: fonts (Amaranth/Arsenal/B612 Mono), colours, logo
├── custom.scss              # SCSS overrides: UPPA colours, headings, callouts, sidebar
├── styles.css               # CSS: body, title block, tables, bibliography
├── index.qmd                # Home page
├── slides.qmd               # Page embedding the Reveal.js slideshow via iframe
├── slides/
│   ├── index.qmd            # Self-contained Reveal.js presentation
│   └── slides.scss          # Dark theme for the presentation
└── resources/
    ├── humanum.qmd          # Huma-Num: history, mission, data lifecycle
    ├── consortiums.qmd      # Huma-Num consortiums
    ├── services.qmd         # Huma-Num services + FAIR data
    ├── dariah.qmd           # DARIAH-EU
    ├── clarin.qmd           # CLARIN ERIC (concise)
    ├── eosc.qmd             # EOSC (substantive)
    ├── connections.qmd      # How they connect (Mermaid diagram)
    └── references.qmd       # Bibliography & useful links
```

## How to Render

### Prerequisites
[Quarto](https://quarto.org/docs/get-started/) ≥ 1.5

### 1. Render the presentation (standalone, self-contained)

```bash
cd slides
quarto render index.qmd --to revealjs
cd ..
```

This produces `slides/index.html` — a self-contained Reveal.js file embedded via iframe in `slides.qmd`.

### 2. Render the full website

```bash
quarto render
```

Or for live preview:

```bash
quarto preview
```

## Deployment

Deploy the `_site/` folder to:
- **Netlify** (drag & drop or via `netlify.toml`)
- **GitHub Pages** (`quarto publish gh-pages`)
- **Quarto Pub** (`quarto publish quarto-pub`)

> Make sure `slides/index.html` is present in `_site/slides/` before deploying.  
> If rendering the site doesn't auto-render the slides, run `quarto render slides/index.qmd` first.

## Images

Place the UPPA logo and any other images in `img/`:
- `img/logoUPPA-RepFr.png` — required by `_brand.yml`

## Author

Julien Rabaud  
Applied Mathematics Research Library · UPPA  
Pôle Numérique · Research Data Management  
ORCID: [0000-0002-6604-9777](https://orcid.org/0000-0002-6604-9777)
