---
version: alpha
name: GOTAP
title: GOTAP Design System (DESIGN.md)
description: Machine-readable design tokens and human-readable rationale for the GOTAP visual identity. Built to the google-labs-code/design.md spec so coding agents can produce on-brand UI, and written so the whole GOTAP team (product, social, email, sales, customer service, performance marketing) can apply the brand consistently.
entity: GOTAP
document_type: Design System
classification: Internal
brand_component: Visual Identity
edition: v1.0 (2026)
created: 2026-07-27
dependencies: GOTAP-Brand-Guidelines.md, GOTAP-Tone-of-Voice-Playbook.md, New Brandbook GOTAP - MAY 2026.pptx, gotap.id (live site)
tags: [gotap, design-system, design-md, visual-identity, colors, typography, components, layout, brand]
colors:
  primary: "#000000"
  on-primary: "#FFFFFF"
  background: "#FFFFFF"
  on-background: "#000000"
  surface: "#F7F7F7"
  on-surface: "#000000"
  surface-dark: "#1A1A1A"
  on-surface-dark: "#FFFFFF"
  accent: "#0077B5"
  on-accent: "#FFFFFF"
  neutral: "#BBBBBB"
  highlight: "#F55C5B"
  on-highlight: "#000000"
typography:
  display:
    fontFamily: Michroma
    fontSize: 64px
    fontWeight: 400
    lineHeight: 1.1
  h1:
    fontFamily: Michroma
    fontSize: 36px
    fontWeight: 400
    lineHeight: 1.2
  h2:
    fontFamily: Michroma
    fontSize: 28px
    fontWeight: 400
    lineHeight: 1.25
  h3:
    fontFamily: Michroma
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.3
  label:
    fontFamily: Michroma
    fontSize: 14px
    fontWeight: 400
    letterSpacing: 0.06em
  body:
    fontFamily: Montserrat
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.5
  body-sm:
    fontFamily: Montserrat
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  caption:
    fontFamily: Montserrat
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.4
rounded:
  none: 0px
  sm: 3px
  md: 8px
  lg: 20px
  xl: 24px
  full: 999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 40px
  2xl: 80px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    padding: 16px 28px
  button-primary-hover:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.on-primary}"
    rounded: "{rounded.md}"
    padding: 16px 28px
  button-secondary:
    backgroundColor: "{colors.background}"
    textColor: "{colors.on-background}"
    rounded: "{rounded.md}"
    padding: 16px 28px
  button-accent:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.on-accent}"
    rounded: "{rounded.md}"
    padding: 16px 28px
  link:
    textColor: "{colors.accent}"
  card:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.on-surface}"
    rounded: "{rounded.lg}"
    padding: 24px
  card-dark:
    backgroundColor: "{colors.surface-dark}"
    textColor: "{colors.on-surface-dark}"
    rounded: "{rounded.lg}"
    padding: 24px
  input:
    backgroundColor: "{colors.background}"
    textColor: "{colors.on-background}"
    rounded: "{rounded.md}"
    padding: 12px 16px
  badge-highlight:
    backgroundColor: "{colors.highlight}"
    textColor: "{colors.on-highlight}"
    rounded: "{rounded.sm}"
    padding: 4px 10px
  divider:
    backgroundColor: "{colors.neutral}"
    height: 1px
---

## Overview

GOTAP is Modern. Professional. The visual identity is premium and minimal, built on a high-contrast black and white core with restrained accent color. White space is the luxury. Nothing tries too hard.

This file has two jobs. The tokens above give coding agents exact values to build on-brand interfaces. The prose below tells the whole team, product, social, email, sales, customer service, and performance marketing, how and why to apply them. Same identity everywhere, different application per channel.

**Source legend used throughout:**

- *(source)* comes directly from the May 2026 brandbook.
- *(observed)* was measured on the live gotap.id site.
- *(inferred)* is a sensible extension, not stated anywhere, confirm before treating as final.

## Colors

The palette is black and white first. Accents organize content and draw attention without overpowering the core.

<color_roles>
| Token | HEX | Origin | Role |
|-------|-----|--------|------|
| `primary` | #000000 | source | Core ink. Headlines, primary buttons, dark surfaces. |
| `on-primary` | #FFFFFF | source | Text and icons on black. |
| `background` | #FFFFFF | source | Base surface and negative space. |
| `on-background` | #000000 | source | Default text on white. |
| `surface` | #F7F7F7 | observed | Subtle light section background to separate blocks. |
| `on-surface` | #000000 | source | Text on the light surface. |
| `surface-dark` | #1A1A1A | observed | Elevated dark panels, hero blocks, button hover. |
| `on-surface-dark` | #FFFFFF | source | Text on dark panels. |
| `accent` | #0077B5 | source | Links and professional or network cues. |
| `on-accent` | #FFFFFF | source | Text on the accent (passes WCAG AA at 4.8:1). |
| `neutral` | #BBBBBB | source | Borders, dividers, disabled states. |
| `highlight` | #F55C5B | source | Coral. Sparing attention on a single element. |
| `on-highlight` | #000000 | source | Text on coral (use black, 6.5:1, not white which fails AA). |
</color_roles>

### Contrast and accessibility

- Black and white pairings are maximum contrast and safe everywhere.
- `accent` #0077B5 carries white text at 4.8:1. It passes AA for normal text, but only just. Do not tint it lighter.
- `highlight` #F55C5B and `neutral` #BBBBBB **fail WCAG AA as text on white**. Never set body copy in coral or gray. Use coral as a fill behind black text, or for large display only. Use gray for structure, not reading text.

## Typography

Two families. Michroma for anything that acts as a title. Montserrat for everything read in sentences.

<type_system>
- **Michroma** *(source, observed)* is the display face. It ships in a single weight (400). It is wide and geometric, so it works at large sizes and short lines, never for paragraphs. Live site uses it at 64px for H1 and 36px for H2, both weight 400, no letter spacing.
- **Montserrat** *(source, observed)* is the body face. Full weight range from Thin to Black. Body runs 16px at 1.5 line height on the live site. Use Medium and above for small captions so they hold up.
</type_system>

| Token | Family | Size | Origin | Use |
|-------|--------|------|--------|-----|
| `display` | Michroma | 64px | observed | Hero and cover lines. |
| `h1` | Michroma | 36px | observed | Page and section titles. |
| `h2` | Michroma | 28px | source | Main titles inside a page. |
| `h3` | Michroma | 20px | inferred | Sub-section titles. |
| `label` | Michroma | 14px | source | Eyebrows, buttons, small caps labels. |
| `body` | Montserrat | 16px | observed | Default reading text. |
| `body-sm` | Montserrat | 14px | inferred | Secondary and dense text. |
| `caption` | Montserrat | 12px | inferred | Metadata, captions, footnotes. |

## Layout

Space is the primary design tool. Give elements room. A GOTAP layout looks unhurried and expensive because it is not crowded.

<layout_rules>
- **Spacing scale** *(inferred, 8px base)*: `xs` 4, `sm` 8, `md` 16, `lg` 24, `xl` 40, `2xl` 80. Compose spacing from these steps only.
- **Rhythm:** pair a large title with generous space around it. Let single ideas stand alone. This mirrors the copy rule from the tone playbook, short beats long, confidence does not fill every pixel.
- **Alignment:** left align by default for text blocks. Center only short hero statements.
- **Measure:** keep body line length near 60 to 75 characters for readability.
</layout_rules>

## Elevation & Depth

*(inferred, guided by the live site)* GOTAP is close to flat. Depth is created by contrast and space, not heavy shadows.

- Prefer separation by color block (white next to `surface` #F7F7F7 or `surface-dark` #1A1A1A) over drop shadows.
- When a shadow is needed, keep it soft and low: a small blur at low opacity black. No hard or colored shadows.
- Overlays on imagery use black or white at partial opacity to seat text, matching the translucent overlays seen on the site.

## Shapes

*(observed)* GOTAP mixes sharp interactive elements with softly rounded media.

- **Buttons and inputs:** `md` 8px. Enough to feel modern, restrained enough to stay premium.
- **Cards and images:** `lg` 20px to `xl` 24px. Media blocks carry the larger radius.
- **Small chips and tags:** `sm` 3px.
- **Avatars and icon circles:** `full`.
- Keep radius consistent within a component type. Do not mix 8px and 20px on the same element.

## Components

Core components below. Interaction variants (hover, active) are separate entries with a related name, per the DESIGN.md spec. All background and text pairs meet WCAG AA.

<component_notes>
- **button-primary** *(source default)*: solid black, white label, 8px radius. The everyday action.
- **button-primary-hover**: shifts to #1A1A1A. Subtle, no color change.
- **button-secondary** *(observed hero CTA)*: white fill, black label. Used on dark or photographic backgrounds. On the live site this is the main hero button. A translucent white ghost version (white text on a 30 percent white fill) is the paired secondary on dark heroes.
- **button-accent** *(source)*: blue #0077B5 fill, white label. Reserve for professional or network actions, not every button.
- **link**: blue #0077B5. See the discrepancy note below, the live site currently renders links in magenta.
- **card** and **card-dark**: light #F7F7F7 or dark #1A1A1A panels at 20px radius.
- **input**: white field, black text, 8px radius, `neutral` 1px border (border is described here rather than tokenized, since the spec component schema has no border property).
- **badge-highlight**: the only common use of coral. Black text on coral, small radius, tight padding. One per view at most.
- **divider**: 1px `neutral` line.
</component_notes>

## Do's and Don'ts

<dos_donts>
**Do**

- Lead with black, white, and space. Treat color as a guest.
- Use exactly one accent per view. One coral highlight or one blue action, not both fighting.
- Keep Michroma for titles and Montserrat for reading. Never set paragraphs in Michroma.
- Hold generous margins. When unsure, add space, not elements.
- Pair every colored surface with an AA-safe text color from the tokens.

**Don't**

- Do not put body text in coral #F55C5B or gray #BBBBBB. They fail contrast.
- Do not add gradients, heavy shadows, or colored glows. GOTAP is matte and flat.
- Do not stack accents or fill a layout with color. That reads cheap, the opposite of the brand.
- Do not stretch, recolor, or crowd the logo (see Brand Guidelines section 4.3).
- Do not mix corner radii within one component.
</dos_donts>

## Channel Application

Same tokens, different dial per team. This section is for everyone, not only engineers. Pair it with the Tone of Voice Playbook for the words.

<channel_guidance>
- **Product and web:** the full token set applies directly. White base, #F7F7F7 section blocks, black `button-primary`, blue for links and network actions.
- **Social (Instagram, TikTok):** black or white canvases. Michroma for the one hook line, Montserrat for support text. One accent maximum. Generous margins, safe area respected. No emoji used as bullets.
- **Email:** white background, black text, blue #0077B5 links, one `button-primary` (black) or a single coral `badge-highlight` for one offer. One CTA per message.
- **Sales decks and one-pagers:** black and white. Michroma titles at `h1` or `h2`, Montserrat body. Coral only to mark a single number or word.
- **Performance marketing creative:** high-contrast black and white. Coral #F55C5B as the single attention driver on the key element. Headline in Michroma, minimal text, strong margins. Test the accent, but keep only one per creative.
- **Customer service:** plain and calm. Montserrat, black text, blue links. No heavy styling. Match the warm, human tone from the playbook.
</channel_guidance>

## Sources & Discrepancies

<sources>
- **Canonical brand:** New Brandbook GOTAP, May 2026. Colors, fonts, and the premium-minimal direction come from here.
- **Practical values:** measured on the live gotap.id site (type scale, radii, surfaces, button geometry, body line height).
- **Companion files:** GOTAP-Brand-Guidelines.md and GOTAP-Tone-of-Voice-Playbook.md.
</sources>

<discrepancies>
Resolve these before locking v1.0. The live site predates the May 2026 brandbook, so it diverges in color.

1. **Accent color mismatch.** The brandbook specifies blue #0077B5 and coral #F55C5B. The live site uses magenta #CC3366 for links and accents. This file follows the brandbook. Decide whether the site should be updated to match, or whether magenta stays and the brandbook is revised.
2. **CTA color.** The live site's main call to action is white-on-black, not coral or blue. If coral or blue should become the primary action color, the site needs updating.
3. **Body text color.** The brandbook implies pure black. The live site softens body text to #333333. Pick one. #333333 is easier on the eyes for long copy and still passes AA.
</discrepancies>
