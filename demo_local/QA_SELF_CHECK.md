# Local browser self-QA — 2026-09-01

## Result

`SELF-QA = PASS — READY FOR INDEPENDENT VISUAL ACCEPTANCE`.

This is local browser evidence only. It is not deployment, public-link, outreach, production, customer approval or independent-review evidence.

## Browser evidence

| Viewport | Browser result | Screenshot evidence | Layout result |
|---|---|---|---|
| 1440 × 900 | `http://127.0.0.1:4173/` loaded; title `Landscaping Greentree | Mitcham` | `evidence/desktop-top-1440x900.png`, `desktop-middle-1440x900.png`, `desktop-bottom-1440x900.png` | `documentWidth=1440`, matching viewport; no horizontal overflow. |
| 390 × 844 | same local page loaded | `evidence/mobile-top-390x844.png`, `mobile-middle-390x844.png`, `mobile-bottom-390x844.png` | `documentWidth=390`, matching viewport; no horizontal overflow. |

## Official-asset enrichment recheck

After the user-requested brand/detail enrichment, a fresh local Playwright session loaded five rendered official Nextdoor assets (one 100×100 logo and four 760–774×900 gallery images) without failed image loads. `documentWidth=1440` at desktop and `documentWidth=390` at mobile. Evidence: `evidence/enriched-desktop-top-1440x900.png`, `enriched-desktop-gallery-final-1440x900.png`, `enriched-mobile-top-390x844.png`, `enriched-mobile-gallery-390x844.png`. The prior misclassified brand-poster file was removed from the rendered gallery before this final recheck.

## Checks passed

- Header/hero, service trio, visual work section, enquiry path and bottom contact block are present at both target viewports.
- Telephone and email links resolve to the documented `tel:` and `mailto:` routes; no form, tracking, booking or server action exists.
- One official logo and four separately sourced official public-gallery files are used once each; exact hashes, direct source URLs and use boundaries are in `IMAGE_LEDGER.md` and `ASSET_INVENTORY.csv`.
- Customer-visible copy gives a descriptive gallery treatment only. It does not invent project names, project locations, dates, customers, prices, reviews, credentials, availability, hours, placeholder/TODO language, internal process text or an AI-generation claim.
- CSS only has small hover/focus transitions. `prefers-reduced-motion: reduce` removes transition/smooth-scroll behaviour; no automatic motion or runtime dependency is used.

## Console note

The first local run reported only a missing `/favicon.ico` 404. `index.html` was then amended with an inline empty favicon. A fresh `greentree_verify` browser session loaded the page successfully with no console entries reported; it also confirmed 390px document width equals its viewport and found three telephone links plus two email links.

## Acceptance boundary

Independent visual acceptance remains pending. `PRE_CODE REVIEWER CHECK` also remains pending because this execution was expressly non-delegated.

## Gallery-fill recheck

Following the requested final-row correction, the 21st gallery card is full-width only at desktop widths, so the final desktop gallery row has no unused grid columns. Fresh full-page local screenshots are `evidence/portfolio-fill-desktop-1440x900.png` and `evidence/portfolio-fill-mobile-390x844.png`; 26 of 26 rendered images loaded in the local browser. The 1440px and 390px document widths matched their respective viewports, so no horizontal overflow was observed. Mobile retains its existing two-column gallery rhythm.

## Motion optimisation recheck

`motion-design` now supplies a restrained Premium/grounded sequence: a 720–900ms Hero entrance, 580ms one-time section/gallery reveals, and existing 450ms image-hover feedback. It has no autoplay loop, carousel, video, parallax or dependency. The implementation never hides unvisited content: a full-page capture remains complete before scroll, and unsupported JavaScript leaves the same static page. `prefers-reduced-motion: reduce` disables the transitions/animations. Fresh local captures are `evidence/motion-final-desktop-1440x900.png` and `evidence/motion-final-mobile-390x844.png`; the desktop local browser reported zero console messages/errors.

## Faithful display-image recheck

The Hero and main work feature now use separately named 2× local resamples of their retained official originals (`1544×1800` and `1548×1800`). No generative edit was adopted because inspection showed it would alter real-project details. The derived files, source hashes, output hashes and non-semantic processing boundary are recorded in `IMAGE_LEDGER.md`. Local 1440×900 evidence: `evidence/upscale-desktop-top-1440x900.png`; browser console: 0 messages/errors.

## Full public-service grouping recheck

The repeated public category strings are represented once as four legible groups: Garden & landscape; Paving, paths & decking; Fences, walls & stonework; and Property maintenance. The outdoor business remains the page's primary identity; the mixed indoor/handyman items are clearly separated as additional publicly listed work. Fresh local 1440×900 and 390×844 full-page screenshots completed with no desktop console messages/errors.
