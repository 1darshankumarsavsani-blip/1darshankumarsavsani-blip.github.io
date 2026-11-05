# DESIGN.md — Darshankumar Savsani portfolio

Design system applied to https://1darshankumarsavsani-blip.github.io/, following the token spec Darshankumar supplied
(Ingenious Minds Lab style: Sora + DM Sans + DM Mono, coral accent, soft surfaces, animated hero).
Only the style tokens are used. All text, photos and code on the site are original.

## Overview
- **Product:** Darshankumar Savsani portfolio (DARSHAN CORPORATION)
- **Surface type:** marketing / personal portfolio
- **Audience:** recruiters, teachers, people who want his apps
- **Brand character:** confident, friendly, bilingual (English + Gujarati)

### Design principles
- Consistency over novelty — reuse patterns before inventing new ones.
- Token-driven — every visual decision references a token below.
- Accessible by default — visible focus, readable contrast, reduced-motion support.

## Colors
| Token | Light | Dark | Role |
|---|---|---|---|
| --surface | #F6F5F7 | #150F1B | page |
| --bg / --card | #FFFFFF | #1A1322 | cards |
| --ink | #1E1826 | #F1ECF7 | primary text |
| --mut | #5C5468 | #9A939F | secondary text |
| --line | #E5E7EB | #2A2233 | borders |
| --ac | #FF5A5F | #FF5A5F | main accent (buttons, numbers, links) |
| --ac2 | #FD6347 | #FD6347 | gradient end, tags |
| --blue | #0F90FF | #0F90FF | accent, focus ring, tags |
| --teal | #00E2E2 | #00E2E2 | accent on dark panels, dots |
| --soft | #FFEDEE | #2C1A22 | icon tiles |

## Typography
**Font stack:** Sora (headings), DM Sans (body), DM Mono (labels), Instrument Serif italic (accent line), Noto Sans Gujarati (fallback).
| Level | Size | Usage |
|---|---|---|
| hero | clamp(42px, 7vw, 80px) / 800 | main headline |
| h2 | clamp(32px, 4.8vw, 54px) / 800 | section headings |
| h3 | 20px | card titles |
| body | 15–19px | text |
| label | 12–13px DM Mono | eyebrows, chips, tags |
Weights: 400, 500, 700, 800. Sentence case everywhere, no ALL CAPS body text.

## Spacing
Base unit 4px. Used: 4, 6, 8, 10, 12, 16, 20, 24, 40, 64, 84.

## Shapes
radius: 12px (small tiles), 16px, 20.6px (cards), 21.6px (hero card, CTA), 9999px (pills, chips).

## Elevation
- ring: `0 0 0 1px rgba(255,90,95,.12)`
- hero card: `0 28px 70px -32px rgba(255,90,95,.35)`
- card: `inset 0 1px 0 rgba(255,255,255,.95), 0 0 0 1px rgba(120,110,100,.14)` + `0 14px 48px -32px rgba(42,34,51,.14)`
- hover: coral ring + `0 10px 28px -18px rgba(255,90,95,.45)`
- glow on logo and primary button: `0 0 12px rgba(255,90,95,.4)`

## Motion
- fast 0.15s, base 0.3s, slow 0.45–0.5s, all `cubic-bezier(.4,0,.2,1)`.
- Hero accent shimmer: 4s linear infinite.
- Background aura: 8s ease-in-out infinite.
- Scroll hint: 2.2s ease-in-out infinite.
- Skills marquee: 48s linear infinite.
- Nav button gentle shake: 4.2s ease-in-out infinite.
- `prefers-reduced-motion` turns all of it off.

## Components
Header (sticky, blurred), pill buttons (primary / outline), eyebrow label, chips, hero card with floating tag and 3 stats, scroll hint, skills marquee, project cards, feature cards, stats cards, CTA panel, footer.
States for every interactive part: default, hover (lift), focus-visible (3px blue ring), active (scale .97).

## Do
- Reference tokens by name, not raw values.
- Use the spacing and radius scale only.
- Keep content in sentence case.
- Test at phone width and desktop width.
- Keep both languages in sync: `<span data-e>English</span><span data-g>ગુજરાતી</span>`.

## Don't
- Don't add colours outside the palette.
- Don't mix other border radii.
- Don't nest buttons inside links.
- Phone numbers are public on the Contact section because Darshankumar asked for them (WhatsApp +91 87996 15978, call +91 94284 64677). The resume PDF is not on the site.
- Don't claim apps were tested on devices they were not (macOS and iPhone apps ran only on GitHub's build servers).

## Writing tone
Concise, confident, friendly. Short sentences.

## Definition of done (for a new section or card)
- Uses only tokens above.
- Hover, focus-visible and active states work.
- Works at 390px and 1200px width, light and dark.
- English and Gujarati text both present.
- Reduced-motion respected.
