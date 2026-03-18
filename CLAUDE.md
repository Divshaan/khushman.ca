# Khushman Dhillon Law — Project Reference

> Drop this file in the root of the repo as `CLAUDE.md` so Claude Code can read it.

## Client

**Khushman Dhillon Law** — Solo law practice in Brampton, Ontario, Canada.
- **Lawyer:** Khushman Dhillon — Barrister & Solicitor
- **LSO No.:** 94540K
- **Phone:** +1 942 444 5511
- **Email:** contact@khushman.ca
- **Website:** https://khushman.ca
- **Languages:** English, Hindi, Punjabi
- **Location:** Brampton, Ontario, Canada (service-area business, no specific street address confirmed)

## Practice Areas

Real Estate Law, Family Law, Immigration Law, Wills & Estates, Litigation, Notarization

## Developer

**Divshaan Singh Brar** — Graphic Design student, George Brown Polytechnic (Advance Diploma, graduating 2026). Contact: singhbrardivshaan@gmail.com / 437-297-5009 / Brampton, ON.

## Tech Stack

- Pure **HTML/CSS/JS** — no frameworks, no build tools
- Hosted on **GitHub Pages** (repo: `Divshaan/khushman.ca`)
- Custom domain: `khushman.ca` (via CNAME)
- Contact form: **Formspree**
- Fonts: **Libre Baskerville** (serif headings) + **Jost** (sans-serif body) via Google Fonts
- No Google Maps embed (removed)
- No Google Analytics or Clarity scripts in HTML (set up externally)

## Design System

- **Burgundy:** `#6b2c2c` (primary brand color)
- **Terra/Terracotta:** `#d97e5c` (accent color)
- **Cream:** `#faf8f3` (background)
- **Brown:** `#3d3024` (body text)
- **Brown-light:** `#8a796f` (secondary text)
- CSS variables: `--burg`, `--terra`, `--cream`, `--brown`, `--brown-lt`, `--rule`
- Font variables: `--fd` (display/Libre Baskerville), `--fb` (body/Jost)
- Selection color: burgundy background, cream text (`::selection`)
- Scroll-reveal animations via IntersectionObserver (class `.r`, `.d1`)
- Sticky nav with `.scrolled` class on scroll
- Hamburger menu for mobile

## File Structure

```
khushman.ca/
├── index.html          ← Homepage
├── about.html          ← About Khushman
├── services.html       ← All 6 practice areas with jump nav
├── contact.html        ← Contact form (Formspree) + info
├── process.html        ← "Why Us" page (solo practice differentiators)
├── privacy.html        ← Privacy policy
├── terms.html          ← Terms of use
├── 404.html            ← Custom error page
├── sitemap.xml         ← 7 pages, priority weighted
├── robots.txt          ← Allow all, points to sitemap
├── favicon.ico         ← Browser tab icon (from klogoD.svg)
├── CNAME               ← khushman.ca
├── CLAUDE.md           ← This file
└── assets/
    └── images/
        ├── portrait.jpg          ← Khushman's headshot (100KB, extracted from base64)
        ├── og-image.jpg          ← Social media preview (1200x630, safe-zone design)
        ├── logo.png              ← Square KD mark for schema (400x400)
        ├── favicon-32.png        ← 32px favicon
        ├── apple-touch-icon.png  ← 180px iOS icon
        ├── klogoL.svg            ← Secondary logo — light backgrounds (cream bg, burgundy K + "DHILLON LAW")
        └── klogoD.svg            ← Secondary logo — dark backgrounds (burgundy bg, cream K, terra bar)
```

## Logos

- **Primary logo:** Text-based "Khushman Dhillon Law" in nav (CSS styled, Libre Baskerville)
- **Secondary logos:** `klogoL.svg` (light bg) and `klogoD.svg` (dark bg) — K lettermark with "DHILLON LAW" bar
- **Favicon:** Generated from klogoD.svg

## SEO Setup

- Canonical URLs on all pages
- OG tags (title, description, image, url, locale) + Twitter Card tags on all main pages
- `og:image` and `twitter:image` point to `https://khushman.ca/assets/images/og-image.jpg`
- JSON-LD schema on each page: `LegalService`, `BreadcrumbList`, `FAQPage` (services, process), `WebSite` (index), `Person` (about)
- Schema image: `https://khushman.ca/assets/images/og-image.jpg`
- Schema logo: `https://khushman.ca/assets/images/logo.png`
- Semantic HTML with proper heading hierarchy
- `robots.txt` + `sitemap.xml`
- Geo meta tags for Brampton, ON
- Google Fonts loaded via `<link rel="preconnect">` + `<link rel="stylesheet">` (not `@import`)

## Critical Decisions / Rules

1. **Ontario only** — Khushman will ONLY practice in Ontario. All "dual-licensed", "dual-jurisdiction", "Punjab & Haryana High Court" references have been REMOVED from every page. Do NOT re-add them.
2. **Panjab University education stays** — LL.M. and LL.B. from Panjab University are academic credentials, not practice licenses. Keep them.
3. **Single email everywhere:** `contact@khushman.ca` — `info@khushman.ca` was removed.
4. **No specific street address** — office not confirmed. Use "Brampton, Ontario, Canada" everywhere. No Google Maps embed.
5. **No Google Maps in privacy policy** — removed since embed was removed.
6. **Portrait image is external file** — NOT base64 inline. Reference: `src="assets/images/portrait.jpg"`.
7. **Nav label:** The process page is labeled "Why Us" in nav across ALL pages.
8. **Per-service mailto CTAs** on services page (each service has its own email link with subject line).
9. **Formspree** handles the contact form on contact.html.

## Pages Overview

### index.html (~55KB)
- Hero with "Khushman Dhillon Law" solid/outline treatment
- About section with portrait
- Practice areas grid
- "Why Solo" differentiators (3 cards: Direct Access, Transparent Pricing, Responsive Service)
- CTA section
- Footer

### about.html (~34KB)
- Hero with tagline
- Marquee ticker (Solo Practice, Brampton, English, Hindi, Punjabi, etc.)
- Bio section with portrait
- Credentials section (improved layout with icons):
  - Qualification: Ontario, Canada (LSO, highlighted with terra accent)
  - Master of Laws: LL.M., Panjab University
  - Bachelor of Laws: LL.B., Panjab University
  - Specialized Certificate: Real Estate Transactions, Lincoln Alexander School of Law (2026)
  - Languages: English, Hindi, Punjabi
- Practice areas grid
- CTA

### services.html (~36KB)
- Jump navigation (sticky) for 6 practice areas
- Each area: heading, description, FAQ accordion, mailto CTA
- Areas: Real Estate, Family Law, Immigration, Wills & Estates, Litigation, Notarization

### contact.html (~32KB)
- Contact info (phone, email, location)
- Formspree contact form
- Languages spoken

### process.html (~24KB, labeled "Why Us")
- Why choose solo practice differentiators
- FAQ schema
- CTA

## External Services

- **Google Search Console** — sitemap submitted, 7 pages discovered
- **Bing Webmaster Tools** — sitemap submitted
- **Google Business Profile** — verified (service area business)
- **Yelp** — profile created
- **Microsoft Clarity** — set up for heatmaps
- **Website Launches directory** — verified

## Pending / Future

- Request indexing for each individual page URL in Google Search Console
- Google Business Profile: add photos, complete service listings, business description
- Legal directory listings: LSO directory, Canadian Legal Guide, Lawyer.ca, FindLaw Canada
- LinkedIn business page, Facebook business page
- Google Reviews collection once clients come in
- Blog/content phase for organic traffic
- Possible favicon refinement
