# DESIGN.md — GreenAtlas Design System v2.1

One file. Drop it in every project root. Read it first. Build to it exactly. Last updated: June 2026

---

## Brand & Voice

**What GreenAtlas is:** Climate and sustainability intelligence infrastructure for NGOs, governments, and businesses in East Africa. We help organisations understand and demonstrate their contribution to NDCs, ESG reporting, climate finance, and carbon markets.

**Who reads our work:** NGO programme directors, government climate officers, ESG leads, carbon market buyers (Japan, Singapore, Switzerland, South Korea), and humanitarian donors. People who are pressed for time, operate on evidence, and will dismiss anything that feels like marketing.

**Three words:** Authoritative. Editorial. Grounded.

**Voice register — deliberate mix by audience:**

| Context | Register | Example |
| :---- | :---- | :---- |
| Handbooks / Reports | Authoritative \+ editorial — confident claims, structured argument, data-first | "East Africa faces a financing gap of $X billion. This chapter maps where the money is, and how to reach it." |
| NGO outreach / Pitch decks | Direct \+ confident — practitioner-to-practitioner, no jargon for its own sake | "Your next funding cycle may depend on your ability to report on climate contribution. We make that measurable." |
| Platform UI / Dashboards | Plain and precise — label what it does, active voice, no filler | "Download report", "View indicators", "Update baseline" |
| Social / External comms | Editorial \+ human — one sharp insight per post, grounded in East Africa | "Kenya has 11 projects in the UNFCCC carbon pipeline. Most NGOs operating here don't know it." |

**Copy rules:**

- Lead with the finding, not the topic. ("Deforestation accelerated in Q1" not "This section covers deforestation trends")  
- Make the "so what" explicit — data without consequence is decoration  
- Never open with "We are GreenAtlas..." — open with the problem or the insight  
- One idea per sentence in UI copy. One finding per paragraph in reports.  
- Active voice as default. "Download" not "Available for download."  
- No em dashes. Use commas, colons, or full stops.  
- No "leverage", "holistic", "synergy", "impactful" — plain verbs only  
- No exclamation marks in formal documents

---

## Colour

**Strategy: Committed palette — one strong deep green carries the brand.** Forest green is the primary surface. Lime is the signal. Amber is the human moment.

### Named roles

| Token | Hex | Role |
| :---- | :---- | :---- |
| `--forest` | `#1a3d2e` | Primary surface: dark panels, covers, chapter openers, callout headers, nav |
| `--brand-green` | `#1a7a4a` | Headings, icon strokes, borders, section accents, logo on light BG |
| `--secondary-green` | `#2aad6a` | Sub-headings, links, arrows, secondary accents |
| `--sage` | `#dce8c8` | Light page BG, data card fills, table row alternates, subtle dividers |
| `--lime` | `#b5ff47` | ONE hero stat per document. Score highlights only. Signal, not decoration. |
| `--cream` | `#f7f8f1` | Body BG, body text on dark panels, neutral page backgrounds |
| `--charcoal` | `#2a2a2a` | All body copy, table text on light backgrounds |
| `--muted-green` | `#6b7d63` | Captions, metadata, secondary labels |
| `--amber-light` | `#fef3e2` | "In Simple Terms" callout fills |
| `--amber-dark` | `#c97c1a` | Amber callout labels and borders |
| `--white` | `#ffffff` | Card overlays on dark panels, icon backgrounds |

### Proportion rule

70%  —  Sage / Cream neutrals (breathing room dominates)

20%  —  Forest panels (\#1a3d2e)

 8%  —  Brand green accents (\#1a7a4a)

 2%  —  Lime (\#b5ff47) — hero statistics ONLY

### Hard colour rules

- Lime appears on maximum ONE element per document or view — not per section, per document  
- Never lime on sage without a dark separator between them  
- Never black text on dark green — always cream or sage text on forest panels  
- Never gradient text — solid colour only; use weight or size for emphasis  
- Tint all neutrals toward the brand — never pure `#000` or `#fff` except white overlays on dark panels  
- No rainbow palettes. No multiple competing accent colours.  
- Logo icon always in `--brand-green` on light backgrounds, white on dark panels

---

## Typography

**Maximum 3 font families. No exceptions.**

| Font | Role | Never |
| :---- | :---- | :---- |
| **Bebas Neue** | Display: covers, chapter openers, large stats, eyebrow labels | Body copy, captions, tables, UI labels |
| **DM Sans** | Body: all body text, UI labels, data tables, captions, card titles | Display titles on covers |
| **Playfair Display Italic** | Editorial accent: mission statements, pull quotes | Body text, headings, data, UI |

Playfair Display is a **signature device** — maximum 2 uses per document. Never in UI.

### Size scale

| Level | Font | Print | Screen | Notes |
| :---- | :---- | :---- | :---- | :---- |
| H1 / Cover | Bebas Neue | 48–72pt | 48–80px | Tracking \+2%, line height 90% |
| Editorial Quote | Playfair Display Italic | 28–40pt | 32–44px | Signature moment — use once |
| Eyebrow Label | Bebas Neue / Mono ALL CAPS | 8–11pt | 11–13px | Wide tracking, green underline bar |
| H2 Section | DM Sans Bold | 24–32pt | 26–34px | Line height 110% |
| H3 Card title | DM Sans SemiBold ALL CAPS | 10–14pt | 12–16px | Wide tracking |
| H4 Subhead | DM Sans Medium | 13–16pt | 14–18px | Line height 130% |
| Body | DM Sans Regular | 9.5–11pt | 15–17px | Line height 140–150%, max 65–72 char/line |
| Data / Table | DM Sans Regular | 9–10pt | 13–15px | — |
| Caption | DM Sans Regular | 7.5–9pt | 12–13px | Line height 130%, muted-green |

### Type rules

- Bebas Neue is display only — never below 24pt/px  
- Body line length: 65–75 characters maximum (use `max-width: 65ch` on screen)  
- Each heading level must be clearly larger than the level below — no ambiguous hierarchy  
- Heading steps must read as jumps, not increments

---

## Spacing & Layout

### Screen (px) — HTML/React/Dashboard

XS   4px     SM   8px     MD   16px    LG   24px

XL   40px    XXL  64px    XXXL 96px

### Print (pt) — PDF/Reports

XS   3pt     SM   6pt     MD   12pt    LG   18pt

XL   30pt    XXL  48pt    XXXL 72pt

**Only use these tokens. No arbitrary pixel values.**

### Grid

- **Documents:** 12-column editorial grid. Margins: Top 20mm / Bottom 25mm / Outside 20mm / Inside 25mm  
- **Screen / React:** 12-column CSS grid. Container max-width: 1280px. Gutter: 24px. Side padding: 40px.  
- **Dashboard panels:** 4–6 column inner grid. Card gutter: 16px.  
- Every element aligns to the grid. No floating objects.

### Whitespace rule

Generous. When unsure, add space not remove it. Dense data pages must be balanced by light pages.

### Page composition (documents)

- One dark panel \+ one light panel per spread, OR full-bleed image \+ text panel  
- Never two dense dark panels facing each other  
- Alternate density: dense data → light/image → dense data

---

## Shape & Elevation

**Corner radius:**

- Cards / callout boxes: 4–6px / 4–6pt  
- Buttons (screen): 4px — not pill-shaped, not sharp  
- Stat blocks: 4px  
- Full-panel elements (chapter openers, hero panels): 0px — flush to edge

**Borders:**

- Callout boxes: 1px solid using the box's accent colour  
- Dividers: 1px `--sage` or `--brand-green` depending on panel colour  
- Table rows: 0.5px `--sage` rule between rows — no heavy borders  
- No double borders

**Shadow / Elevation:**

- Print / PDF: No shadows. Fills and borders only.  
- Screen / UI: One shadow level only — `box-shadow: 0 2px 8px rgba(26, 61, 46, 0.10)` for cards on light BG  
- Never stacked shadows, never coloured shadows, never glassmorphism

---

## Motion (Screen / HTML / React only)

**Philosophy: Motion is editorial punctuation, not decoration. Every animation must do a job.**

**Allowed:**

- Scroll-triggered fade-in: `opacity 0→1, translateY 12px→0` over `300ms ease-out`  
- Hover micro-interactions on buttons and cards: `200ms ease`  
- Chart/data load: values count up from zero on first render — one time only  
- Page transitions (if applicable): fade `200ms ease`  
- Subtle indicator pulse on live data: `opacity 0.6→1` loop, `2s ease-in-out`

**Timing:**

- Fast (hover): 150–200ms  
- Standard (reveal): 280–320ms  
- Slow (page-level): 400ms max

**Easing:** `ease-out` for reveals, `ease` for hover, `ease-in-out` for loops. No `linear` except loaders.

**Hard rules:**

- `prefers-reduced-motion` must be respected — wrap all animations in the media query  
- No animation on body text blocks — only structural elements, stats, and charts  
- No parallax  
- No auto-playing video backgrounds

---

## Logo & Wordmark

**Icon mark:** Globe form with interlocking leaf/calligraphy lines. Single-weight stroke. Organic, precise, distinctive.

**Wordmark:** "GreenAtlas" — or two-line "GREEN / ATLAS" for compact formats.

**Usage rules:**

| Background | Logo version |
| :---- | :---- |
| Dark panel (`--forest`) | White icon \+ white wordmark |
| Light page (`--cream`, `--sage`) | `--brand-green` icon \+ `--charcoal` wordmark |
| Brand green panel | White icon \+ white wordmark |
| Photography overlay | White version only, on darkened area |

**Clear space:** Minimum clear space around logo \= height of the "G" in wordmark on all sides.

**Never:**

- Recolour the icon in lime, amber, or any non-brand colour  
- Stretch or distort the icon  
- Place on busy photographic backgrounds without a scrim  
- Use the icon at less than 24px / 18pt height

---

## Components

### Callout Boxes

| Type | BG | Label colour | Use for |
| :---- | :---- | :---- | :---- |
| KEY TERM | `--forest` | `--lime` | First use of important technical term |
| IN SIMPLE TERMS | `--amber-light` | `--amber-dark` | Plain-language explanations |
| DID YOU KNOW? | `--sage` | `--brand-green` | Surprising stat or fact |
| EAST AFRICA CONTEXT | `--forest` | `--lime` | Regional application of global data |
| CHAPTER SUMMARY | `--forest` | `--secondary-green` | Chapter takeaways |
| INFO PANEL | `--sage` or `--cream` | `--brand-green` | General callout, case study context |

All boxes: labelled header row (Mono ALL CAPS), 4–6pt radius, 10–12pt vertical padding, 14–16pt horizontal padding. No shadows.

### Icon Card Grid

- 3 or 4 equal-height cards per row  
- Card BG: `--sage` on dark panel / `--cream` on light page  
- Content: line icon (single stroke, same family) → bold ALL CAPS title → 2–3 line body  
- `--brand-green` 1px divider between rows  
- Equal padding (MD) on all cards  
- Card title: DM Sans SemiBold ALL CAPS

### Stat / Fact Card Row

- `--forest` panel background  
- White or `--sage` rounded-rect fact blocks (4px radius)  
- Large number: Bebas Neue 24–34pt / 28–40px  
- Lime: ONE hero stat per document only  
- Label beneath: DM Sans small-caps, `--cream`  
- One row per section — never stacked

### Buttons (screen)

- Primary: BG `--brand-green`, text `--cream`, hover BG `--forest` — transition 200ms  
- Secondary: BG `--sage`, text `--charcoal`, border 1px `--brand-green`, hover BG `--brand-green` text `--cream`  
- Destructive / Alert: BG `--amber-light`, border `--amber-dark`, text `--amber-dark`  
- Border-radius: 4px. Padding: 10px 20px. DM Sans Medium 14px.  
- Never pill buttons. Never gradient buttons.

### Data Tables

- Header: `--forest` BG, white text, DM Sans Bold 8–9pt  
- Data rows: alternate `--cream` / `--white`  
- Row rules: 0.5px `--sage`  
- Column text: DM Sans Regular, `--charcoal`  
- Section labels above: `--brand-green`, DM Sans Bold small-caps

### Navigation (screen)

- BG `--forest`. Logo left. Links in DM Sans Medium 14px `--cream`.  
- Active link: `--secondary-green`. Hover: `--sage`. Transition 150ms.  
- No drop shadows on nav. No glassmorphism.

---

## Bans

These patterns are never shipped. When Claude builds without this file, these are what it defaults to. Ban them here so they never appear.

**Visual bans:**

- ✗ Gradient text — solid colour only; vary weight or size for emphasis  
- ✗ Glassmorphism — no blur backgrounds, no frosted panels  
- ✗ Left-border stripe callouts (coloured left bar on cards) — use full border or background tint  
- ✗ Identical card grids — same icon, same text structure, same size, repeated n times  
- ✗ Hero metric block with gradient accent — the standard SaaS layout (huge number, tiny label, gradient)  
- ✗ Pill-shaped buttons  
- ✗ Coloured drop shadows  
- ✗ Dark mode blue — GreenAtlas dark is forest green, never navy or near-black blue  
- ✗ Tech-green / neon green as the primary accent — the Solarix pattern works for energy tech; GreenAtlas is warmer, more organic  
- ✗ Pure `#000000` or pure `#ffffff` except as white overlays on dark panels  
- ✗ Multiple competing accent colours — lime is the signal; amber is the exception; there is no third accent  
- ✗ Decorative diagonal slashes or background geometric noise — texture is in the typography, not the background  
- ✗ Auto-scrolling carousels or hero sliders  
- ✗ Progress bars as decorative elements — only if they encode real data  
- ✗ Emoji in formal documents or dashboards

**Copy bans:**

- ✗ Em dashes — use commas, colons, or full stops  
- ✗ "Leverage", "holistic", "synergy", "impactful", "stakeholders" (unless quoting a client)  
- ✗ Opening any document with "We are pleased to present..."  
- ✗ Exclamation marks in any document longer than a social post  
- ✗ Passive voice as default — active verbs only

**Structure bans:**

- ✗ Two dense dark panels facing each other (documents)  
- ✗ Floating elements not aligned to the grid  
- ✗ Playfair Display Italic more than twice per document  
- ✗ Lime on more than one element per document  
- ✗ Bebas Neue in body text at any size

---

## The Two-Part Slop Test

Run this before shipping anything:

**Test 1 — The glance test:** Could someone look at this for three seconds and say "AI made that"? If yes, identify which banned pattern crept in and remove it.

**Test 2 — The category test:** Could someone guess GreenAtlas's colours from the category alone? "Climate NGO" should not force forest green — it should feel like a specific deliberate choice, not the first reflex. If the palette looks like generic sustainability green, push it further toward the specific: more cream, more contrast, tighter lime restraint.

---

## Reuse Instructions

**Every build:**

1. Drop this file in the project root before writing any code  
2. Tell the agent: "Read DESIGN.md first, then build \[deliverable\]. Follow colours, fonts, spacing, shapes, and bans exactly — don't improvise. If anything is unclear, ask."  
3. Ask for 2–3 variations before locking one in

**When to update this file:**

- After you see a pattern appear in builds that belongs in the bans list  
- After a new component is locked and approved  
- After a colour is refined following real-world use  
- Never mid-project — update between projects only

---

*GreenAtlas Design System v2.1 — Climate & Sustainability Intelligence, East Africa* *Maintained by LMD Consulting Group / Wanjama Benson*  
