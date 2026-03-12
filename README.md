# Digital Research Infrastructures for the Humanities

**Quarto website + Reveal.js presentation**  
UPPA ED 481 SSH & UNITA CHORAL Programme — 2026

## Structure

```
.
├── _quarto.yml              # Website project config
├── custom.scss              # Site-wide styles
├── index.qmd                # Home page
├── humanum.qmd              # Huma-Num overview
├── consortiums.qmd          # Huma-Num consortiums
├── services.qmd             # Services & FAIR data
├── dariah.qmd               # DARIAH-EU
├── clarin.qmd               # CLARIN ERIC
├── connections.qmd          # How they connect (+ Mermaid diagram)
├── presentation.qmd         # Page embedding the slideshow
├── references.qmd           # Bibliography & links
└── slides/
    ├── index.qmd            # Reveal.js presentation (self-contained)
    └── slides-custom.scss   # Presentation styles
```

## How to render

### Prerequisites
- [Quarto](https://quarto.org/docs/get-started/) ≥ 1.4

### Render the presentation first (standalone)

```bash
cd slides
quarto render index.qmd
cd ..
```

This produces `slides/index.html` (self-contained Reveal.js file).

### Render the full website

```bash
quarto render
```

Or for a live preview:

```bash
quarto preview
```

## Deployment

Deploy the `_site/` folder (plus `slides/index.html` at `_site/slides/index.html`) to:
- **Netlify** (drag & drop or GitHub integration)
- **GitHub Pages**
- **Quarto Pub**: `quarto publish quarto-pub`

## Customisation

- Edit `_quarto.yml` to update navbar, theme, or site URL
- Replace logo URLs with local images in `IMG/` for offline use
- Update `slides/index.qmd` front matter (date, institute, footer)
- Add/edit content pages as `.qmd` files

## Author

Julien Rabaud — SCD | Bibliothèque de l'IPRA · CSP Numérique Recherche  
Université de Pau et des Pays de l'Adour  
ORCID: [0000-0002-6604-9777](https://orcid.org/0000-0002-6604-9777)

