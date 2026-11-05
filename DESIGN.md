# DESIGN.md — Darshankumar Savsani portfolio

Design language inspired by the layout and typography feel of ingeniousmindslab.com (big confident headlines, soft backgrounds, rounded cards, pill buttons, mono labels).
Only the *style approach* is borrowed. All text, images, colours and code are original to this site.

## 1. Principles
1. One big idea per screen. Huge headline first, one line of support, two buttons.
2. Soft and airy. White (or deep plum in dark mode), faint colour glow, lots of space.
3. Rounded everywhere. Cards 20px, hero card 26px, buttons fully pill-shaped.
4. One accent colour, used sparingly. Maroon for brand, gold for small highlights.
5. Bilingual by default. Every visible text has English and Gujarati versions.
6. Honest content. Apps not yet run on a real device say so.

## 2. Colour tokens (light / dark)
| Token | Light | Dark | Use |
|---|---|---|---|
| --bg | #FFFFFF | #120A10 | page |
| --bg2 | #FFF6F2 | #1A0F16 | hero glow |
| --ink | #1E1826 | #F6ECEE | text |
| --mut | #6A6275 | #B7A8B3 | secondary text |
| --line | #EEE7EC | #2D1D26 | borders |
| --card | #FFFFFF | #1D1119 | cards |
| --ac | #7B1E3A (maroon) | #FF6B8B | buttons, links, numbers |
| --ac2 | #C0392B | #F7B500 | gradient end |
| --gold | #F7B500 | #F7B500 | version badges, CTA button |
| --soft | #FBEEF0 | #2A1620 | icon tiles |

## 3. Typography
- Headings: **Sora** 800, tight tracking (-0.02em), line-height 1.08, size clamp(40px, 6.4vw, 72px) for the hero.
- Accent line in headings: **Instrument Serif** italic ("on every screen you own.").
- Body: **DM Sans** 400/500/700, 15–19px.
- Labels: **JetBrains Mono** 11px, uppercase, wide tracking (.14em), with a small dot before it.
- Gujarati: **Noto Sans Gujarati** (fallback for all of the above).
- The hero's second line is a maroon to red gradient text.

## 4. Layout
- Container 1140px, 22px side padding. Sections 78px top/bottom, separated by a 1px line.
- Hero: 2 columns (text 1.1fr, photo card 0.9fr), one column under 860px.
- Card grids: `repeat(auto-fit, minmax(250px, 1fr))`, 16px gap.
- Sticky header, 68px high, blurred translucent background.

## 5. Components
- **Header**: logo tile (gradient "DS") + wordmark, links, language toggle, theme toggle, Contact pill.
- **Eyebrow**: mono label with dot. Introduces every section.
- **Chips**: small mono rounded-8px labels (Est. 2024, Diploma CE).
- **Pill buttons**: primary (maroon, soft shadow, lifts 2px on hover) and outline.
- **Hero card**: photo on a soft gradient, floating tag top-left, three mini stats below.
- **Cards**: 1px border, 20px radius, soft shadow, lift 4px on hover. Icon tile, title, text, tags, link.
- **Version badge**: gold mono badge (v2.0).
- **CTA block**: maroon gradient panel, serif gold accent, gold primary button.

## 6. Behaviour
- Theme: follows the device, toggle remembers the choice.
- Language: Gujarati phones open in Gujarati, the toggle remembers the choice.
- No frameworks, a single `index.html` plus two images. Fonts load from Google Fonts.

## 7. Content rules
- No phone number and no resume PDF on the public page.
- Keep claims you can prove: macOS and iPhone apps were built and tested on GitHub's servers only.

## 8. How to change things
- Brand colour: edit `--ac` / `--ac2` at the top of the style block.
- New project card: copy one `.card` in the Work section.
- Add a language string: wrap it as `<span data-e>English</span><span data-g>ગુજરાતી</span>`.
