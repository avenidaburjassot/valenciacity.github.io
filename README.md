# Daphne Inn Valencia — Public Safety Information Website

Public-facing, bilingual (Spanish / English) informational website documenting compliance failures, safety deficiencies, and active legal proceedings related to **Daphne Inn Valencia** accommodation at Avenida de Burjassot 228, Valencia, Spain. Operated by **Valencia City Roof Terrazas S.L.**

🔗 **Live site:** [daphneinnvalencia.es](https://daphneinnvalencia.es/)

---

## Overview

This repository hosts the source code for a static GitHub Pages website that serves as a public service announcement. The site presents verified, publicly-sourced information about documented issues at Daphne Inn Valencia, including:

- Absence of mandatory rental registration (NRA)
- Lack of habitability licence (Licencia de Segunda Ocupación)
- Fire safety deficiencies documented by the fire brigade
- Catastro (land registry) discrepancies
- Active administrative and legal proceedings
- User reviews archived from Google Maps

The site is bilingual — all content is presented in both **Spanish (primary)** and **English** to serve both local residents and international visitors.

## Features

- **Single-page static site** — fast loading, no server dependencies
- **Bilingual content** — Spanish and English throughout
- **SEO-optimised** — structured data (JSON-LD), Open Graph, Twitter Cards, sitemap, canonical URLs, geo meta tags
- **Accessible** — ARIA labels, semantic HTML, keyboard-navigable popup, `lang` attributes for bilingual sections
- **Responsive design** — mobile-first CSS with sticky navigation
- **Structured data** — `WebPage`, `FAQPage`, and `BreadcrumbList` JSON-LD schemas for enhanced search results
- **Official verification links** — direct links to Spanish public registries (Catastro, Registro Mercantil, AEAT, Agència de l'Habitatge)

## Project Structure

```
├── index.html      # Main single-page site (HTML, CSS, JS — all inline)
├── robots.txt      # Search engine crawling directives
├── sitemap.xml     # XML sitemap for search engine indexing
├── CNAME           # Custom domain configuration (daphneinnvalencia.es)
└── README.md       # This file
```

## Technology

| Component       | Technology                                |
|-----------------|-------------------------------------------|
| Hosting         | GitHub Pages                              |
| Domain          | daphneinnvalencia.es (via CNAME)          |
| Markup          | Semantic HTML5                            |
| Styling         | Inline CSS with CSS custom properties     |
| Fonts           | Libre Franklin, Libre Baskerville (Google Fonts) |
| Structured Data | JSON-LD (Schema.org)                      |
| JavaScript      | Vanilla JS (popup dismiss only)           |

## Local Development

No build step is required. To preview locally:

```bash
# Clone the repository
git clone https://github.com/avenidaburjassot/valenciacity.github.io.git
cd valenciacity.github.io

# Serve with any static file server
python3 -m http.server 8000
# or
npx serve .
```

Then open `http://localhost:8000` in your browser.

## SEO Configuration

The site includes the following SEO components:

- **Meta tags** — title, description, keywords, robots, author, theme-color, geo tags
- **Open Graph** — og:title, og:description, og:url, og:type, og:locale
- **Twitter Card** — summary card with title and description
- **Structured data** — `WebPage` with `LodgingBusiness` about entity, `FAQPage` with six Q&A pairs, `BreadcrumbList`
- **Hreflang** — `es`, `en`, `x-default` for multilingual indexing
- **Canonical URL** — prevents duplicate content issues
- **Sitemap** — `sitemap.xml` referenced in `robots.txt`

## Sections

| Section              | Anchor ID    | Description                                         |
|----------------------|-------------|-----------------------------------------------------|
| Warnings             | `#warnings` | Primary warning about compliance failures           |
| Critical Incident    | `#incident` | Documented incident of 26 March 2026                |
| Entity               | `#entity`   | Company and administrator identification            |
| Safety & Compliance  | `#safety`   | Registration, habitability, fire safety status      |
| Legal Proceedings    | `#legal`    | Active cases across multiple authorities            |
| Platform Status      | `#platforms`| Listing status on Airbnb, Spotahome, Flatio        |
| Verification         | `#verify`   | Links to official Spanish public registries         |
| Reviews              | `#reviews`  | Archived Google Maps user reviews                   |
| FAQ                  | `#faq`      | Bilingual frequently asked questions                |

## Contributing

Contributions that improve accuracy, accessibility, SEO, or code quality are welcome. Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feat/your-improvement`)
3. Make your changes
4. Test locally to verify rendering and responsiveness
5. Submit a pull request with a clear description

### Commit message conventions

This project uses [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` — new features or content sections
- `fix:` — bug fixes or content corrections
- `docs:` — documentation updates (README, comments)
- `style:` — CSS or formatting changes (no logic change)
- `refactor:` — code restructuring without behaviour change
- `perf:` — performance improvements

## Troubleshooting

| Issue                          | Solution                                                  |
|--------------------------------|-----------------------------------------------------------|
| Fonts not loading              | Check network connectivity to fonts.googleapis.com        |
| Images not displaying          | Verify `assets/img/` files exist; check browser console   |
| Custom domain not working      | Verify CNAME file contains `daphneinnvalencia.es`         |
| Popup not showing              | Clear `sessionStorage` (`policePopupDismissed` key)       |

## License

This project is published as a public service information resource. Content is derived from public records and documented sources. All factual claims are referenced. Where opinions or beliefs are expressed, they are clearly identified as such.

## Disclaimer

This website is an independent informational resource. It is not affiliated with, endorsed by, or connected to the owners, operators, or management of Daphne Inn or any related business entity. Nothing on this website constitutes legal advice.
