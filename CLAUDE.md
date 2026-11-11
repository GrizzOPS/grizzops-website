# CLAUDE.md — GrizzOPS Website Source of Truth

> **Every Claude session working on this project must read this file first before making any changes.**

---

## 1. BUSINESS OVERVIEW

**What it is:** GrizzOPS is an operations consulting and systems-build service for hunting outfitters, fishing charters, guides, and lodges. It fixes broken booking, deposit, and follow-up systems.

**Owner:** K.J. "GRIZZ" Krueger — former professional hunting guide and outfitter (Wyoming & Alaska, 20 years).

**Contact details (as shown live on site):**
- Phone: (520) 753-1741 — `tel:+15207531741`
- Email: grizz@grizzops.com
- Booking: https://api.leadconnectorhq.com/widget/booking/ovMgFv2AlGutTzkI7hsU (GHL discovery-call calendar)
- Facebook: https://www.facebook.com/profile.php?id=61570996226927
- Domain: https://grizzops.com

---

## 2. SERVICES & PRICING

All four cards are live on the site. Prices and descriptions below are pulled directly from index.html.

> **Pricing note (Aug 2026):** every published price is the base fee plus a 3% card-processing
> surcharge ($500 -> $515, $297 -> $306, $1,500 -> $1,545, $3,000 -> $3,090, $4,000 -> $4,120,
> $2,000 -> $2,060, $800 -> $824).

### Tier 1 — GrizzREPORTS
- **Badge:** Step 1 — Find the Leak
- **Tagline:** Diagnose Before You Fix
- **Price:** $515 (one-time project fee)
- **Description:** Full audit of your booking, deposit, and follow-up system. Delivered within 5 business days.
- **For:** Any outfitter who suspects something's broken but can't pinpoint it.
- **Payment link (GHL):** https://link.fastpaydirect.com/payment-link/6ab327c685ad343a1541b0d0
- **Sample report:** /GrizzREPORT_HighCountry_Sample.pdf

### Tier 2 — GrizzBACKBONE
- **Badge:** Step 2 — Fix It
- **Tagline:** Install the System
- **Price:** $3,605 headline. $3,090 for clients who start with GrizzREPORTS — the $515 audit
  is credited in full. (Set Sept 2026; supersedes the $3,090 headline from Aug 2026.)
- **Payment split:** $1,545 deposit to start · $2,060 on delivery ($1,545 on delivery if they
  started with GrizzREPORTS). Both paths use the SAME $1,545 deposit Stripe link.
- **Card copy:** the credited-price sub-line sits directly under the headline. The old italic
  line "Already got a GrizzREPORT? The $515 comes off your final payment." was deleted as a
  duplicate of it.
- **Description:** Complete system build. Booking, deposits, and communication — built, tested, and handed off ready to run.
- **For:** Operators booking manually who want it executed.
- **Payment link (GHL):** https://link.fastpaydirect.com/payment-link/6ab32c8d9a013c156f1f99b2 (Pay Deposit — $1,545)
- **Setup time:** Most operations fully installed and running within 3 weeks of kickoff.

### Tier 2b — GrizzBACKBONE + Website
- **Badge:** Step 2 — Fix It + Get Found
- **Tagline:** Install the System & the Site
- **Price:** $4,635 headline. $4,120 for clients who start with GrizzREPORTS — the $515 audit
  is credited in full. (Set Sept 2026; supersedes the $4,120 headline from Aug 2026.)
- **Payment split:** $2,320 deposit to start · $2,315 on delivery ($1,800 on delivery if they
  started with GrizzREPORTS).
- **Description:** Complete system build plus a custom website — one main page covering camp, packages, and pricing, plus a photo gallery, an FAQ section, and an inquiry form wired into the booking system. Mobile-friendly and fast-loading.
- **Add-on:** Additional camp or property pages at $824 each.
- **Payment link (GHL):** https://link.fastpaydirect.com/payment-link/6ab32e1c9a013c156f1f99ba (Pay Deposit — $2,320)
  Verified live in Stripe: "GrizzBACKBONE + Website Bundle Deposit", $2,320.00, GrizzOPS account.
- **Note:** Badge, tagline, and "For" line were written by Claude and reviewed/approved by Grizz
  (Aug 2026). As of Sept 2026 this card DOES carry two `tier-note` lines (credited price +
  payment split), matching the BACKBONE card; the old "50% deposit to start, remaining balance
  invoiced on delivery" sentence was removed from the description because the split line
  replaces it and "50%" is inaccurate for the GrizzREPORTS path.

### Tier 3 — GrizzCORE
- **Badge:** Step 3 — Keep It Running
- **Tagline:** Ongoing Management
- **Price:** $306/mo (monthly retainer — 3-month minimum, then month-to-month)
- **Note:** "A single $6,000 hunt, or two $2,000 charters, covers this for the whole year."
  (Set Sept 2026, replacing "One recovered repeat client covers the first month.") The claim is
  against $306/mo x 12 = $3,672/yr — a $6,000 hunt clears it, two $2,000 charters ($4,000)
  clear it with $328 to spare. If CORE ever goes above $333/mo the charter half stops being
  true and this line must be rewritten.
- **Description:** Monthly system monitoring, seasonal updates, and a standing check-in — you'll always know who to call if something needs attention.
- **For:** Clients who want it executed without touching it themselves.
- **Payment link (GHL):** https://link.fastpaydirect.com/payment-link/6ab32ecf9a013c156f1f99bb
- **Cancel policy:** Cancel anytime, no penalty. The built system stays with the client — they own it.

### Retired Stripe links (removed from site — archive in Stripe if still live)
- `cNi28qcvScPY98AfTEbEA0b` — old Bundle $2,060 deposit (replaced Sept 2026; CONFIRMED STILL
  LIVE at time of replacement — archive it in Stripe)
- `5kQdR9aOVc6JglEbfibjW01` — old BACKBONE $1,750 deposit
- `00wdR92ipfiV3yS3MQbjW03` — old BACKBONE $1,500 deposit
- `fZu9AT3mt1s5d9sgzCbjW00` — old GrizzREPORTS $500
- `14AbJ12ip5Il6L43MQbjW05` — old GrizzCORE $297/mo

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

### Hosting — ✅ CONFIRMED
- **Host: Netlify** — confirmed live, deployed from GitHub.
- **Netlify account:** grizz@grizzops.com under GrizzOPS team.
- **GitHub repo:** https://github.com/GrizzOPS/grizzops-website
- Netlify is connected directly to the GitHub repo via the Netlify dashboard. No config file in the repo is required.

### Contact Form — ✅ CONFIRMED WORKING
- The contact form uses `data-netlify="true"` and `data-netlify-honeypot="bot-field"`.
- **2 active Netlify forms:** `contact` and `testimonial-submission`.
- Last confirmed contact form submission: **May 25**.
- Submissions are captured in the Netlify dashboard under Forms.

### Other Integrations
- **Stripe:** Three active payment links (see Services section above)
- **Booking (GHL):** https://api.leadconnectorhq.com/widget/booking/ovMgFv2AlGutTzkI7hsU — discovery-call calendar (replaced Calendly Oct 2026)
- **Google Analytics:** G-74L8MG3PK4 (present on all pages)
- **Sitemap:** /sitemap.xml
- **robots.txt:** Present, allows all crawlers, points to sitemap

### Demo Video
- `<section id="demo">` sits directly under the hero, before "The Real Problem".
- Privacy-enhanced YouTube embed (`youtube-nocookie.com`), **YouTube ID: `xmSlckHF52Y`** (https://youtu.be/xmSlckHF52Y).
- Responsive 16:9 player (`.demo-frame`, `aspect-ratio:16/9`, max-width 900px, centered, 8px radius). Label above it: "See how it works — 76 seconds."
- A matching `VideoObject` JSON-LD block is in `<head>` (4th structured-data block).

### Language Toggle
- **REMOVED permanently** (June 2026 sprint). The ES/EN toggle button, all JS translation logic (`translations` object, `selectors` object, `toggleLang()` function), and all `data-en`/`data-es` attributes have been deleted from index.html. Do not re-add.

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
| 3 | **Is the Stripe account live or in test mode?** The three Stripe links are hardcoded. Confirm payments are going to the correct Stripe account. | Direct revenue impact. |
| 4 | **Is the GHL booking link active?** https://api.leadconnectorhq.com/widget/booking/ovMgFv2AlGutTzkI7hsU — confirm it's open for bookings. | Every CTA on the page points here. |
| 7 | **GrizzCORE "Get Started" button** — link is now `dRmeVc67u2bkesUdLwbEA0d`. Confirm the Stripe product matches $306/mo. | Pricing accuracy. |

## SITE STATUS — Last updated June 2026

### Testimonials
- **Bill Perry · Owner, Hidden Creek Outfitters** — live ✅ (FIRST in "What People Say"). Verbatim
  except two spelling fixes to "GrizzOPS"; first two paragraphs always shown, the last paragraph
  sits behind a "Read more" button. No phone/email for Bill, no review/rating structured data.
- **Tim Hockhalter · Retired Outfitter** — live ✅
- **Caleb Norris, Co-Outfitter · Hidden Creek Outfitters · License #BG366** — live ✅
- **Cayla Norris, Business Manager · Hidden Creek Outfitters** — live ✅
- **Rotator behavior:** fades between the four cards. Each card's time is set by `data-duration`
  on its slide — Bill 12s, the others 7s — via a `setTimeout` that restarts fresh every time a card
  shows (no `setInterval`). It does NOT pause on mouse hover. It pauses only while Bill's Read more
  is expanded (Read less restarts his full 12s) or while a keyboard user has focus in the carousel
  (full time again when focus leaves). Prev/next arrows + one dot per card (gold = active), all real
  44px buttons with aria-labels; clicking any of them jumps there and restarts that card's timer.
  Arrows sit either side of the quote at ≥1000px and flank the dot row below that. The box sizes to
  the showing card (0.5s height transition, `ResizeObserver`). Hidden cards are inert +
  aria-hidden. With "reduce motion" on, no auto-rotation — arrows and dots only.

### PageSpeed Scores (recorded June 2026)
| Page | Desktop | Mobile |
|---|---|---|
| index.html | 100 / 96 / 100 / 100 | 98 / 96 / 100 / 100 |
*(Performance / Accessibility / Best Practices / SEO)*

### Sprint Completed — June 2026 ✅ DONE

- AEO/SEO upgrade: meta descriptions, OG tags, Twitter cards, JSON-LD (ProfessionalService, FAQPage, Service ItemList) on all pages
- Accessibility fixes: `<main>` landmark, form label/input linking, FAQ heading roles, aria-labels, aria-hidden on decorative elements
- Color contrast fixes: `#555` → `#888` on footer-copy and proof-placeholder; `#f5c542` → `#D4A017` in util-bar CSS
- sitemap.xml: removed /404 entry; sitemap resubmitted to Google Search Console
- Image optimization complete: headshot.png 2.7MB → 177KB, horses.jpg 534KB → 173KB
- Backup files (.bak) removed from repo
- Spanish language toggle permanently removed (all HTML, JS, CSS)
- Final verified PageSpeed scores: Desktop 100/96/100/100, Mobile 98/96/100/100
- CLAUDE.md created and maintained as source of truth

## CHANGE LOG

### 2026-11-11 — Testimonial rotator timing fixed, arrows + dots added
- Rotator: 12s Bill / 7s others with a fresh `setTimeout` per card; pauses only on Bill's Read more
  expanded or keyboard focus (never on hover); prev/next arrows + dots; box height follows the
  showing card (no blank gap); no auto-rotate under prefers-reduced-motion. Full spec in SITE STATUS →
  Testimonials. All four testimonials' wording and order unchanged.
- Changes confined to the `#proof` section plus a new `/* ── TESTIMONIAL ROTATOR CONTROLS ── */`
  CSS block beside `.read-more-btn`.
- Verified in Chrome (desktop + true 390px phone frame): rotates with the mouse over it, measured
  12.01s / 7.01s / 7.02s / 7.01s; Read more held 16s+, Read less → next card at +12.00s; arrow and
  dot clicks/taps land correctly and restart the timer (+7.00s); keyboard Tab/Enter works and pauses
  until focus leaves; box height = card height on every card; no overlap or sideways scroll on phone;
  reduce-motion stays put past 14s while arrows still work.

### 2026-11-11 — Added Bill Perry testimonial (first in "What People Say")
- New first card: Bill Perry · Owner, Hidden Creek Outfitters. Bill's words verbatim except the
  two "GrizzOPS" spelling fixes he approved. Paragraphs 1–2 always visible; paragraph 3 ("As being
  an outfitter yourself…") is behind a "Read more" / "Read less" `<button>` with `aria-expanded`
  + `aria-controls="bill-perry-more"` (blue accent, 44px tap target, `.read-more-btn` CSS).
  Same card markup/classes as the other three (quote mark, `.proof-quote`, `.proof-attr`).
- Tim's card moved from the "shown first" slot to the stacked slot (wrapper style only; its text
  is unchanged). Tim, Caleb and Cayla text and name lines untouched.
- Rotator script updated so the button works: hidden slides get `pointer-events:none`, `inert`
  and `aria-hidden` (they're stacked on top and were catching clicks), and rotation pauses while
  Bill's card is expanded, mouse-hovered, or keyboard-focused. Still 5s per card otherwise.
- No phone/email for Bill; no Review/AggregateRating structured data added.
- Checked: desktop + true 390px phone viewport (iframe), mouse click, phone tap, and keyboard
  Enter all expand/collapse; no horizontal scroll; all 4 JSON-LD blocks still parse.

### 2026-11-02 — Accuracy pass: features as options, "I" not "we", broader operation types
- **Voice:** site now speaks as a solo operator ("I/me/my") instead of "we/us/our" everywhere it
  refers to GrizzOPS/KJ — the booking-agency line ("I'M NOT A BOOKING AGENT. I don't chase down
  clients…"), GrizzCORE + GrizzREPORTS "What You Actually Get" descriptions, the GrizzREPORT FAQ,
  the cancel FAQ export line, the FAQ heading ("Questions I get on every call"), the contact
  headline ("whether I've solved it before"), and the matching FAQPage JSON-LD answers.
  Testimonials (client voice) and the "GrizzOPS" business name left unchanged. Meta/OG/Twitter
  descriptions and the ProfessionalService / VideoObject / ItemList structured data were already
  third-person with "GrizzOPS" — no "we" there to change.
- **GrizzBACKBONE features = options, not guarantees:** the "What You Actually Get" BACKBONE
  paragraph now frames the calendar/missed-call-text/voicemail-to-text/deposit/payment/follow-up
  features as "depending on how you run, it can include… you pick what fits; I leave out what
  doesn't," and adds that texting features require a separate carrier registration billed
  separately.
- **Broader fit + accuracy tweaks:** "Will this work for my type of operation?" now names dude
  ranches / "booked outdoor business"; setup-time FAQ notes it depends on how fast client info
  arrives; part-time-admin FAQ softened ("can quit", "sends every follow-up on schedule").
- Text only — all prices, links, payment buttons, and styling unchanged. JSON-LD re-validated
  (4 blocks parse; all 10 FAQ answers match HTML byte-for-byte).

### 2026-11-02 — Removed "never touch it" claims to match the software FAQ
- Three spots updated so they no longer claim the client never touches the system, matching the
  rewritten "What software do you use?" FAQ (client does a few manual steps by hand):
  1. FAQ "What if I'm not tech savvy?" (HTML + FAQPage JSON-LD, identical text) — now names the
     few manual steps (send deposit link, check contract, mark trip done) instead of "you do not
     touch the system… runs on its own."
  2. GrizzCORE description in "What You Actually Get" — "without you touching it" → "and you're
     never the one fixing it."
  3. GrizzCORE pricing card "For" line — "want it executed without touching it themselves" →
     "want the system kept running without maintaining it themselves."
- Text only; styling and all other content untouched. JSON-LD re-validated.

### 2026-11-02 — "What software do you use?" FAQ rewritten for accuracy
- Replaced the answer (HTML + FAQPage JSON-LD, identical text) so it's accurate about the manual
  steps the client actually does by hand: after talking with a client they tap to send the
  deposit link, they review the contract before it goes out, and they mark the trip done when
  it's over — everything else (replies, deposit reminders, forms, follow-ups) runs automatically.
  Replaces the old "you do not need to learn anything / without touching a dashboard" claim.
- Answer text only; question, styling, and all other FAQs untouched. JSON-LD re-validated.

### 2026-11-02 — Site now leads with GrizzBACKBONE; GrizzREPORTS made optional
- Pricing cards reordered to GrizzBACKBONE, GrizzBACKBONE + Website, GrizzCORE, GrizzREPORTS (last).
  GrizzREPORTS kept on the site as an optional last card. Badges renumbered (BACKBONE "Step 1 —
  Fix It", Website "Step 1 — Fix It + Get Found", CORE "Step 2 — Keep It Running", REPORTS
  "Optional — Not Sure Where You Stand?"). Per-card colors preserved by remapping the
  `:nth-child` badge/name/price CSS to the new positions — no visual color change to any card.
  All prices, credited-price lines, sample-report link, payment links, and arrows unchanged.
- "What You Actually Get" descriptions reordered to BACKBONE, CORE, REPORTS; intro paragraph
  rewritten to lead with BACKBONE and frame REPORTS as optional.
- Hero secondary button changed from "Get a sample report first →" (#sample) to
  "Watch the 76-second demo →" (#demo).
- FAQ "How do the three levels work?" and "Do I have to do all three?" rewritten (HTML + FAQPage
  JSON-LD, identical text) to lead with BACKBONE and the 3-month GrizzCORE minimum.
- Sample report section (`<section id="sample">`) and its CSS removed entirely; nothing links to
  `#sample` anymore. The /GrizzREPORT_HighCountry_Sample.pdf sample link still lives on the
  REPORTS card.

### 2026-11-02 — FAQ cancel/ownership wording matched to GrizzCORE Retainer Agreement v2
- Rewrote the answers to "Do I have to sign a long-term contract?" and "What happens if I want
  to cancel?" so the cancel terms (3-month minimum, then month-to-month; cancel in writing
  before the next billing date), data ownership/export, and the $150/hr (2-hr min) migration fee
  match the GrizzCORE Retainer Agreement v2. Answer text only — questions, styling, and the
  other 8 FAQs untouched.
- Updated the matching two answers in the FAQPage JSON-LD to the identical text; all 4 JSON-LD
  blocks re-validated as parsing, and each HTML answer verified byte-identical to its JSON-LD.

### 2026-11-02 — Added embedded demo video under hero
- New `<section id="demo">` between hero and "The Real Problem". Label "See how it works —
  76 seconds." + responsive 16:9 `youtube-nocookie.com` embed of video `xmSlckHF52Y`
  (`?rel=0`, `loading="lazy"`, `allowfullscreen`, title "GrizzOPS demo — booking systems for
  outfitters"). Player max-width 900px centered, 8px radius, 1px `--border`; full-width with
  24px side padding on phones (added `#demo` to the existing mobile padding rule).
- Added a 4th JSON-LD block (`VideoObject`) in `<head>`: name "GrizzOPS Demo — Booking Systems
  for Outfitters", embedUrl (nocookie), contentUrl (youtu.be), thumbnail hqdefault.jpg,
  uploadDate 2026-11-02, duration PT1M16S.
- No other section, text, link, button, or price changed. Checked at desktop + phone widths:
  video loads/plays, no horizontal scroll, nothing else shifted.

### 2026-10-24 — Booking migrated from Calendly to GoHighLevel (GHL)
- Replaced all 3 booking CTAs in index.html (nav "Book a Call", hero/CTA "Book a Free Call" x2)
  from `https://calendly.com/grizzops/30min` to
  `https://api.leadconnectorhq.com/widget/booking/ovMgFv2AlGutTzkI7hsU`. Button text, classes,
  `target="_blank"` all left exactly as they were (no `rel` attrs were present; none added).
- Updated the 3 Calendly references in this file (Booking contact, Integrations, Open Q#4) to the
  GHL link so the repo has zero remaining "calendly" references.
- FLAGGED: the old site links used the `grizzops/30min` slug while this file had previously
  documented `kjkrueger12/30min` — a pre-existing mismatch, now moot since both are retired.
- No prices, other links, or any other site content changed.

### 2026-09-02 — GrizzCORE note rewritten
- Replaced the CORE `tier-note` second sentence: "One recovered repeat client covers the first
  month." -> "A single $6,000 hunt, or two $2,000 charters, covers this for the whole year."
- Copy only. Price ($306/mo), Stripe link (`dRmeVc67u2bkesUdLwbEA0d`), description and every
  other card untouched.
- Math checked against the live price before committing — see the CORE section above for the
  $333/mo ceiling that keeps the charter claim true.

### 2026-09-02 — Bundle repriced to $4,635 + new Stripe deposit link
- Headline $4,120 -> $4,635. Sub-line added: "$4,120 if you started with GrizzREPORTS. Your
  $515 audit is credited in full." (4,635 - 515 = 4,120.)
- Split line ADDED (this card previously had none — the 50% split lived in the description):
  "$2,320 deposit to start · $2,315 on delivery ($1,800 if you started with GrizzREPORTS)".
  Checks: 2,320 + 2,315 = 4,635 and 2,320 + 1,800 = 4,120.
- Removed "50% deposit to start, remaining balance invoiced on delivery." from the description
  — duplicated by the new split line, and "50%" is wrong for the GrizzREPORTS path.
- Deposit button: new Stripe link `00w00i53qdU2acEbDobEA0f`, label "Pay Deposit — $2,320".
  Grizz created the link; it was loaded and read before committing — "GrizzBACKBONE + Website
  Bundle Deposit", $2,320.00, GrizzOPS account. Amount and product match the button.
- JSON-LD bundle Offer + UnitPriceSpecification 4120 -> 4635. Also updated `priceRange` on the
  ProfessionalService block ("$515 – $4,120" -> "$515 – $4,635") since the bundle is the top of
  that range — Grizz approved this as in-scope.
- UNCHANGED: REPORTS, BACKBONE and CORE cards and their three Stripe links.
- Verified: all 3 JSON-LD blocks parse; all four cards read back correct prices/notes/buttons/
  hrefs from the rendered DOM; exactly 4 Stripe links in the file and the retired one is gone.

### 2026-09-02 — GrizzBACKBONE repriced to $3,605
- Headline $3,090 -> $3,605 (explicit written instruction from Grizz in-session, per rule 9).
- New sub-line under the price: "$3,090 if you start with GrizzREPORTS. Your $515 audit is
  credited in full." The maths checks: 3,605 - 515 = 3,090.
- Split line updated to carry both paths: "$1,545 deposit to start · $2,060 on delivery
  ($1,545 if you started with GrizzREPORTS)". It previously read $1,545 + $1,545 = $3,090,
  which would have contradicted the new headline on the live card.
- Deleted the old italic line, now a duplicate of the new sub-line.
- JSON-LD BACKBONE Offer + UnitPriceSpecification both 3090 -> 3605, so structured data
  matches the visible price (rule 8 / rich-results risk).
- UNCHANGED as instructed: the Pay Deposit button and its Stripe link
  (aFacN467ucPY1G85f0bEA0a), the CORE card, the Bundle card, all other Stripe links.
- NOTE: the GrizzREPORTS card was checked and contains NO line referencing the BACKBONE price
  or the credit, so nothing needed updating there. If an upsell line is wanted on that card it
  still needs writing.
- Verified: all 3 JSON-LD blocks parse; the only remaining "3,090" in index.html is the
  intentional credited-price copy; card rendered and checked in a browser.

## RESOLVED QUESTIONS

| # | Question | Resolution |
|---|---|---|
| 1 | Is the site hosted on Netlify? | ✅ Confirmed Netlify. Account: grizz@grizzops.com, GrizzOPS team. Deployed from GitHub. |
| 2 | Are contact form submissions arriving? | ✅ Confirmed working. 2 active forms. Last contact submission May 25. |
| 5 | `#f5c542` color — canonical gold? | ✅ Canonical gold is `#D4A017`. `#f5c542` belongs to GrizzAI (separate project) — do not use on this site. |
| 6 | Spanish toggle incomplete — priority? | ✅ REMOVED permanently in June 2026 sprint. |
| 8 | GrizzBACKBONE headline ($3,000) vs deposit halves ($1,545 × 2 = $3,090) | ✅ Grizz chose the $3,090 headline (Aug 2026). SUPERSEDED Sept 2026 — headline is now $3,605, with $3,090 as the GrizzREPORTS-credited price. Card and JSON-LD both show 3605. |
