# CLAUDE.md — GrizzOPS Website Source of Truth

> **Every Claude session working on this project must read this file first before making any changes.**

---

## 1. BUSINESS OVERVIEW

**What it is:** GrizzOPS is an operations consulting and systems-build service for hunting outfitters, fishing charters, guides, and lodges. It fixes broken booking, deposit, and follow-up systems.

**Owner:** K.J. "GRIZZ" Krueger — former professional hunting guide and outfitter (Wyoming & Alaska, 20 years).

**Contact details (as shown live on site):**
- Phone: (520) 753-1741 — `tel:+15207531741`
- Email: grizz@grizzops.com
- Booking: https://calendly.com/kjkrueger12/30min
- Facebook: https://www.facebook.com/profile.php?id=61570996226927
- Domain: https://grizzops.com

---

## 2. SERVICES & PRICING

All three tiers are live on the site. Prices and descriptions below are pulled directly from index.html.

### Tier 1 — GrizzREPORTS
- **Badge:** Step 1 — Find the Leak
- **Tagline:** Diagnose Before You Fix
- **Price:** $500 (one-time project fee)
- **Description:** Full audit of your booking, deposit, and follow-up system. Delivered within 5 business days.
- **For:** Any outfitter who suspects something's broken but can't pinpoint it.
- **Stripe link:** https://buy.stripe.com/28EfZgeE0cPYacE6j4bEA00
- **Sample report:** /GrizzREPORT_HighCountry_Sample.pdf

### Tier 2 — GrizzBACKBONE
- **Badge:** Step 2 — Fix It
- **Tagline:** Install the System
- **Price:** $3,500 (one-time project fee) — GrizzREPORT clients receive $500 off ($3,000)
- **Description:** Complete system build. Booking, deposits, and communication — built, tested, and handed off ready to run.
- **For:** Operators booking manually who want it executed.
- **Stripe links:**
  - Standard: https://buy.stripe.com/7sYeVc8fCdU2gB2dLwbEA01 (Get Started — $3,500)
  - Reports client discount: https://buy.stripe.com/bJe7sK53qbLUacEfTEbEA04 (Reports Client — $3,000)
- **Setup time:** Most operations fully installed and running within 3 weeks of kickoff.

### Tier 3 — GrizzCORE
- **Badge:** Step 3 — Keep It Running
- **Tagline:** Ongoing Management
- **Price:** $297/mo (monthly retainer — no long-term contract)
- **Note:** One recovered repeat client covers the first month.
- **Description:** Monthly system monitoring, seasonal updates, and a standing check-in — you'll always know who to call if something needs attention.
- **For:** Clients who want it executed without touching it themselves.
- **Stripe link:** https://buy.stripe.com/eVqdR83Zm8zI0C48rcbEA05
- **Cancel policy:** Cancel anytime, no penalty. The built system stays with the client — they own it.

---

## 3. BRAND

### Color Palette (CSS variables in index.html)
| Variable | Hex | Usage |
|---|---|---|
| `--black` | `#0a0a0a` | Page background |
| `--gold` | `#D4A017` | Primary brand color, headings, GrizzREPORTS tier |
| `--gold-light` | `#e8b820` | Hover states |
| ~~`#f5c542`~~ | — | **Do not use.** This belongs to GrizzAI (separate project). Not a GrizzOPS color. |
| `--blue` | `#00BFFF` | Accent color, GrizzBACKBONE tier, links |
| `--blue-dark` | `#0088cc` | Blue hover states |
| `--grey` | `#888` | Muted labels |
| `--dark-card` | `#111111` | Card backgrounds, utility bar |
| `--border` | `rgba(212,160,23,0.2)` | Dividers and borders |
| Body text | `#bbb` / `#ccc` | General paragraph text |

### Typography
- **Headlines:** Arial Narrow, Arial, sans-serif — weight 900, uppercase, tracked
- **Body:** Arial, sans-serif — 17px base, 1.6 line-height
- **Buttons:** Arial Narrow — weight 700-900, uppercase, letter-spacing 0.1em

### Visual Style
- Dark, high-contrast — black background, gold and blue accents
- No rounded corners on primary buttons (square-edged CTA style)
- Section labels: small caps, gold, tracked uppercase
- Fade-in scroll animations on `.fade-up` elements

### Tone of Voice
- Direct, no-fluff, outfitter-speaks-to-outfitter
- Short declarative sentences. No corporate language.
- First person from Grizz's perspective
- Acknowledges the operator's pain before offering a fix
- No pressure sales language — "No pitch. No pressure."

---

## 4. TECH FACTS

### Stack
- **Plain HTML/CSS/JS — no framework, no build tool, no CMS**
- All pages are standalone `.html` files
- Inline `<style>` blocks; no external stylesheet
- Inline `<script>` blocks; no bundler
- Google Analytics: `G-74L8MG3PK4`

### Pages
| File | URL |
|---|---|
| index.html | https://grizzops.com/ |
| thank-you.html | https://grizzops.com/thank-you |
| privacy-policy.html | https://grizzops.com/privacy-policy |
| 404.html | https://grizzops.com/404 |

### Hosting — ⚠️ UNCONFIRMED — SEE OPEN QUESTIONS
- **GitHub repo:** https://github.com/GrizzOPS/grizzops-website
- **There is NO `CNAME` file, NO `netlify.toml`, NO `_redirects`, NO `_headers` file in the repo root.**
- The absence of a `CNAME` file means **GitHub Pages is not configured** (GitHub Pages requires a CNAME file to serve a custom domain).
- The `data-netlify="true"` attribute on the contact form and the `action="/thank-you"` redirect are Netlify Forms conventions.
- **Most likely host: Netlify** — but this is inferred, not confirmed from a config file. Netlify can be connected directly to a GitHub repo via the Netlify dashboard without any config file in the repo.

### Contact Form — ⚠️ IMPORTANT
- The contact form uses `data-netlify="true"` and `data-netlify-honeypot="bot-field"`.
- **Netlify Forms ONLY capture submissions if Netlify is actually serving the site.**
- **If the site IS on Netlify:** form submissions are being captured in the Netlify dashboard. ✅
- **If the site is NOT on Netlify:** form submissions are going nowhere — they submit to `/thank-you` but no data is stored. ❌
- This must be confirmed (see Open Questions). If not on Netlify, the form needs a different backend.

### Other Integrations
- **Stripe:** Three active payment links (see Services section above)
- **Calendly:** https://calendly.com/kjkrueger12/30min
- **Google Analytics:** G-74L8MG3PK4 (present on all pages)
- **Sitemap:** /sitemap.xml
- **robots.txt:** Present, allows all crawlers, points to sitemap

### Language Toggle
- A Spanish/English toggle (`#lang-toggle` button) exists in the nav.
- It covers the major hero/about/tiers/CTA sections via a `translations` JS object.
- FAQ, contact form labels, tier card details, and footer are NOT fully covered by the translation system yet.

---

## 5. RULES FOR CLAUDE (The Constitution)

1. **Read this file first.** Every session, before touching any file.
2. **Pull facts from the site — never invent them.** Prices, claims, timelines, names — everything must match what is actually live. If unsure, put it in Open Questions.
3. **Check cross-page consistency.** The favicon, GA tag, and nav style must stay consistent across index.html, privacy-policy.html, thank-you.html, and 404.html.
4. **No framework creep.** This is plain HTML/CSS/JS. Do not introduce npm, React, Tailwind, or any build tool.
5. **Commit messages must be descriptive.** State what changed and where.
6. **Never push a broken page.** If an edit touches JS or a form, sanity-check the logic before committing.
7. **Stripe links are live payment links.** Do not change them without explicit instruction from Grizz.
8. **Keep the site AEO/SEO clean.** Structured, semantic HTML. OG tags on every page. Do not remove or mangle meta tags.
9. **Do not change prices without explicit written confirmation from Grizz in the session.**
10. **Canonical brand gold is `#D4A017`.** Never use `#f5c542` on this site — that color belongs to GrizzAI (a separate project). If you see `#f5c542` anywhere in this codebase, flag it as a bug.
11. **Flag anything that looks wrong** — broken links, missing favicons on a page, inconsistent copy — rather than silently ignoring it.

---

## OPEN QUESTIONS — Confirm with Grizz

| # | Question | Why it matters |
|---|---|---|
| 1 | **Is the site hosted on Netlify?** Log into netlify.com and confirm grizzops.com is listed as an active site. | Determines whether the contact form is capturing submissions or silently dropping them. |
| 2 | **Are contact form submissions arriving?** Check Netlify dashboard → Forms → contact. If no submissions appear, the form is broken. | Direct revenue impact — missed leads. |
| 3 | **Is the Stripe account live or in test mode?** The three Stripe links are hardcoded. Confirm payments are going to the correct Stripe account. | Direct revenue impact. |
| 4 | **Is the Calendly link active?** https://calendly.com/kjkrueger12/30min — confirm it's open for bookings. | Every CTA on the page points here. |
| 5 | **`#f5c542` still appears in the favicon and some buttons** — needs to be replaced with `#D4A017` across all files. | Visual consistency / brand accuracy. |
| 6 | **Spanish translation is incomplete.** The ES toggle does not cover FAQ, contact form, tier card details, or footer. Is full Spanish coverage a priority? | UX for Spanish-speaking operators. |
| 7 | **GrizzCORE "Get Started" button** — the Stripe link `eVqdR83Zm8zI0C48rcbEA05` was recently updated. Confirm the product in Stripe matches $297/mo. | Pricing accuracy. |
