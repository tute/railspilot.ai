# Web Quality Audit — RailsPilot.ai

## Critical

- [ ] **[Accessibility] Color contrast failure for muted text.** `--muted: #718096` on `--bg: #FFFBF5` yields ~3.9:1 contrast, below WCAG AA 4.5:1 minimum for normal-size text. Used in FAQ answers, price notes, process times, footer text, contact notes. **Fix:** Darken `--muted` to at least `#5A6A7D` (~5.0:1).

## High

- [ ] **[HTML] Broken HTML in `case_studies/programadores-que-esperan-menos/index.html`.** `<article>` opened at line 24 is never closed. Line 49 has `</div>` instead of `</article>`. **Fix:** Add `</article>` before the `</div>` on line 49.
- [ ] **[SEO] Missing `meta description` in `case_studies/programadores-que-esperan-menos/index.html`.** **Fix:** Add `<meta name="description" content="...">`.
- [ ] **[SEO] No `robots.txt`.** **Fix:** Create a minimal `robots.txt` with `Sitemap:` directive.
- [ ] **[SEO] No `sitemap.xml`.** **Fix:** Create a `sitemap.xml` listing all 5 pages and submit to Search Console.
- [ ] **[Accessibility] No `<main>` landmark on any page.** **Fix:** Wrap content between `<header>` and `<footer>` in `<main>` on each page.
- [ ] **[Accessibility] No skip navigation link.** **Fix:** Add a visually-hidden skip link as first focusable element in `<body>`.
- [ ] **[Performance] `@import` in `case_studies/styles.css`.** Creates a render-blocking chain. **Fix:** Replace with two `<link>` tags in each case study HTML, or concatenate CSS files.
- [ ] **[Performance] Oversized favicon.** `favicon.ico` is 130KB (typical < 15KB). **Fix:** Re-export at 32x32 and 16x16.

## Medium

- [ ] **[SEO] No canonical URLs.** **Fix:** Add `<link rel="canonical" href="...">` to each page.
- [ ] **[SEO] No structured data (JSON-LD).** **Fix:** Add `Organization` on homepage, `Article` on case studies.
- [ ] **[SEO] No Open Graph / Twitter Card tags on case study pages.** **Fix:** Add OG and Twitter meta tags to each case study page.
- [ ] **[Accessibility] Footer `.footer-sub` uses `opacity: 0.6`.** Low effective contrast on dark background. **Fix:** Use an explicit color meeting 4.5:1 contrast instead.
- [ ] **[CLS] Missing dimensions on `tute-avatar.jpg` and footer `logo.png`.** **Fix:** Add `width` and `height` attributes.
- [ ] **[Accessibility] No `<nav>` landmark.** **Fix:** Wrap navigational elements in `<nav aria-label="...">`.
- [ ] **[CSS] Missing `.reveal` / `.visible` animation styles.** JS adds classes but no CSS rules exist. Dead code. **Fix:** Add CSS animation rules or remove the JS and `.reveal` classes.
- [ ] **[Consistency] Footer text mismatch in `programadores-que-esperan-menos/`.** Says English "Staff-level Rails. Shipping this week." while other Spanish pages use "Tu equipo tiene la experiencia, la IA la multiplica". **Fix:** Match the other case study pages.
- [ ] **[SEO] Missing `apple-touch-icon` on case study pages.** **Fix:** Add `<link rel="apple-touch-icon">` with correct path.

## Low

- [ ] **[Best Practices] Inline styles in `case_studies/index.html`.** **Fix:** Move to named CSS classes.
- [ ] **[Performance] Google Fonts loads many weights (8 total).** Some likely unused. **Fix:** Audit and remove unused weights.
- [ ] **[Performance] Images are PNG/JPG instead of WebP/AVIF.** **Fix:** Convert to WebP with fallback via `<picture>`.
- [ ] **[Accessibility] Tooltip lacks ARIA pattern.** No `role="tooltip"` or `aria-describedby`. **Fix:** Add proper ARIA attributes.
