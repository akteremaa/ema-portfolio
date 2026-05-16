# Ema Akter Portfolio

A single-page portfolio site for Ema Akter, a Top Rated Social Media and Content Operator on Upwork. Six years on platform, 53 jobs completed, 4,221 hours billed, 100% Job Success Score.

Built with vanilla HTML, CSS, and JavaScript. No build step. No framework. No dependencies. Deploy to GitHub Pages, Netlify, Vercel, or any static host in under five minutes.

## What is in this folder

| File | Purpose |
|---|---|
| `index.html` | The entire portfolio in one self-contained file. CSS and JS inlined. |
| `404.html` | Custom 404 page matching the portfolio's design system. |
| `ema.png` | Portrait image. Currently a placeholder EA monogram. Replace with a real portrait when available. |
| `og-image.png` | 1200x630 Open Graph card for LinkedIn, Twitter, WhatsApp previews. |
| `favicon.ico` | Multi-size ICO for legacy browsers. |
| `favicon-16x16.png`, `favicon-32x32.png`, `favicon-48x48.png` | Standard favicon sizes. |
| `apple-touch-icon.png` | 180x180 PNG for iOS home screen. |
| `android-chrome-192x192.png`, `android-chrome-512x512.png` | Android home screen icons. |
| `sitemap.xml` | Search engine sitemap. Replace SITE_ROOT placeholder before deploy. |
| `robots.txt` | Crawler guidance. Replace SITE_ROOT placeholder before deploy. |
| `README.md` | This file. |

## Deployment in five steps

### 1. Create a new GitHub repository

Name suggestion: `ema-akter-portfolio` or `portfolio`. Public visibility.

### 2. Upload all files in this folder to the repository root

All 14 files go at the root, not inside a subfolder. The site is the root.

### 3. Replace the SITE_ROOT placeholders

Three files contain `SITE_ROOT` as a placeholder. Open each in any text editor and replace with the actual deployment URL (e.g. `https://emaakter.github.io/portfolio/`):

- `sitemap.xml` (10 occurrences)
- `robots.txt` (1 occurrence)
- `index.html` (1 occurrence in the OG image meta tag, optional - relative paths work too)

### 4. Enable GitHub Pages

Repository Settings -> Pages -> Source: Deploy from branch -> Branch: main -> Folder: / (root) -> Save.

GitHub will provide the live URL within a minute. Format: `https://<username>.github.io/<repo-name>/`.

### 5. Verify

Open the live URL. Check:

- Hero loads with the EA monogram in the topbar and "Content that earns attention" headline
- All 12 case studies render with images and metadata
- All 4 testimonials appear with star ratings and Upwork verified badges
- All 10 services render with pricing
- Hover effects work on cards
- Filter chips toggle case study visibility
- The Reviews link in the topbar nav scrolls to the testimonials section
- The Upwork link in the topbar opens her real profile at `https://www.upwork.com/freelancers/emakter`

If anything is broken, the most common cause is a missing file. Verify all 14 files are in the repo root.

## Replacing the portrait placeholder

The current `ema.png` is a chromatic EA monogram placeholder. To swap in Ema's actual photo:

1. Take or source a portrait photo of Ema (any aspect ratio, but 4:5 portrait works best with the layout)
2. Use a background removal tool (recommended: https://remove.bg) to create a transparent PNG
3. Save as `ema.png` and replace the file in the repo
4. Commit and push. The new portrait appears on the next page load.

The portrait tile in the hero uses `object-fit: contain` with bottom-center anchoring, so any reasonable portrait composition will work. Avoid square crops; the tile expects negative space above the head.

## What is intentionally NOT in this site

A few choices worth understanding before edits:

- **No animations on initial load** beyond gentle fade-ins. The site is fast on slow connections by design. Bangladeshi mobile-network speeds were the baseline test.
- **No tracking scripts.** No Google Analytics, no Meta Pixel, no Hotjar. Add them at your discretion. The contact CTAs all point to her Upwork profile, which already has its own analytics.
- **No cookie banner.** Because there are no tracking cookies. Add a banner if you add tracking.
- **No third-party fonts beyond Google Fonts.** Instrument Serif, Geist, and Geist Mono are served from Google's CDN with `preconnect` hints.
- **No contact form.** All inbound goes through Upwork escrow. This is deliberate per the FAQ.
- **No blog.** The site is a portfolio, not a content marketing engine. If Ema wants a blog later, it deserves its own subdomain and stack.

## Customization basics

### Updating copy

Open `index.html` in any editor. Search for the text you want to change and replace it directly. No build step means no compile cycle.

### Updating case studies

Each case study is an `<article class="case ...">` block inside `<div class="work-bento">`. Copy any existing case as a template, change the `data-case` number, the `data-category`, the heading, summary, and metrics. The filter chips at the top of the section will need their count updated if you change the number of cases per category.

### Updating services

Each service is an `<article class="service ...">` inside `<div class="services-grid">`. Same pattern: copy an existing one and edit.

### Updating colors

The chromatic gradient (mint, cyan, violet) is defined as a CSS variable at the top of the inline `<style>` block. Search for `--chroma:` to find it. Update the three hex codes to reskin the entire site.

## Technical notes

- The site is **one HTML file** with everything inlined. This is intentional. It means no CDN dependencies, no build pipeline, no broken links between files. The whole portfolio is portable: open `index.html` in a browser locally and it works.
- **Mobile breakpoint** is at 768px. Below that, the bento grid collapses to a single column.
- **Print stylesheet** is included. Printing the page from a browser produces a clean PDF resume-style document.
- **Keyboard navigation** is fully supported. Cmd+K (Mac) or Ctrl+K (Windows) opens the quick nav.
- **Section scroll observer** highlights the current section in the topbar nav as you scroll.

## Things to verify before sharing the live URL

A short pre-launch checklist:

1. Open in Chrome, Firefox, Safari, and at least one mobile browser
2. Test the filter chips on a touch device
3. Right-click and "Inspect" the page; check for console errors
4. Run https://pagespeed.web.dev/ on the URL; aim for 90+ on mobile
5. Run https://validator.w3.org/ on the URL; fix any HTML warnings
6. Share the URL in a private LinkedIn DM to yourself; verify the OG preview renders correctly
7. Share the URL in a private WhatsApp message to yourself; same check
8. Search the live URL on Google after a week to confirm indexing

## Contact

Site owner: Ema Akter
Upwork: https://www.upwork.com/freelancers/emakter
Location: Khulna, Bangladesh (UTC+6)

Built by Shaikh Eamin.
