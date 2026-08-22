---
version: alpha
name: IBM-design-analysis
description: "An enterprise-marketing canvas faithful to Carbon Design System: white surfaces, charcoal type, IBM Blue (#0f62fe) as the single confident accent, and a deliberately flat-square aesthetic where corners stay at 0–4px. Type runs IBM Plex Sans at light weight 300 for display sizes (a brand signature) and 400/600 for body and emphasis. Cards live as thin-bordered tiles with no shadow; sections separate via subtle gray rows. The chrome is square, the typography is light, and the only color in the system is one assertive blue — the result reads as old-world enterprise gravitas reframed for the cloud era."

colors:
  primary: "#0f62fe"
  on-primary: "#ffffff"
  ink: "#161616"
  ink-muted: "#525252"
  ink-subtle: "#8c8c8c"
  canvas: "#ffffff"
  surface-1: "#f4f4f4"
  surface-2: "#e0e0e0"
  inverse-canvas: "#161616"
  inverse-surface-1: "#262626"
  inverse-ink: "#ffffff"
  inverse-ink-muted: "#c6c6c6"
  hairline: "#e0e0e0"
  hairline-strong: "#161616"
  blue-60: "#0043ce"
  blue-80: "#002d9c"
  blue-hover: "#0050e6"
  semantic-success: "#24a148"
  semantic-warning: "#f1c21b"
  semantic-error: "#da1e28"
  semantic-info: "#0f62fe"

typography:
  display-xl:
    fontFamily: IBM Plex Sans
    fontSize: 76px
    fontWeight: 300
    lineHeight: 1.17
    letterSpacing: -0.5px
  display-lg:
    fontFamily: IBM Plex Sans
    fontSize: 60px
    fontWeight: 300
    lineHeight: 1.17
    letterSpacing: -0.4px
  display-md:
    fontFamily: IBM Plex Sans
    fontSize: 42px
    fontWeight: 300
    lineHeight: 1.20
    letterSpacing: 0
  headline:
    fontFamily: IBM Plex Sans
    fontSize: 32px
    fontWeight: 400
    lineHeight: 1.25
    letterSpacing: 0
  card-title:
    fontFamily: IBM Plex Sans
    fontSize: 24px
    fontWeight: 400
    lineHeight: 1.33
    letterSpacing: 0
  subhead:
    fontFamily: IBM Plex Sans
    fontSize: 20px
    fontWeight: 400
    lineHeight: 1.40
    letterSpacing: 0
  body-lg:
    fontFamily: IBM Plex Sans
    fontSize: 18px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0
  body:
    fontFamily: IBM Plex Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.50
    letterSpacing: 0.16px
  body-sm:
    fontFamily: IBM Plex Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.29
    letterSpacing: 0.16px
  body-emphasis:
    fontFamily: IBM Plex Sans
    fontSize: 14px
    fontWeight: 600
    lineHeight: 1.29
    letterSpacing: 0.16px
  caption:
    fontFamily: IBM Plex Sans
    fontSize: 12px
    fontWeight: 400
    lineHeight: 1.33
    letterSpacing: 0.32px
  button:
    fontFamily: IBM Plex Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.29
    letterSpacing: 0.16px
  eyebrow:
    fontFamily: IBM Plex Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.29
    letterSpacing: 0.16px

rounded:
  none: 0px
  xs: 2px
  sm: 4px
  md: 6px
  lg: 8px
  pill: 9999px
  full: 9999px

spacing:
  xxs: 4px
  xs: 8px
  sm: 12px
  md: 16px
  lg: 24px
  xl: 32px
  xxl: 48px
  section: 96px

components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.none}"
    padding: 12px 16px
  button-primary-pressed:
    backgroundColor: "{colors.blue-80}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.none}"
  button-secondary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.inverse-ink}"
    typography: "{typography.button}"
    rounded: "{rounded.none}"
    padding: 12px 16px
  button-tertiary:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.primary}"
    typography: "{typography.button}"
    rounded: "{rounded.none}"
    padding: 12px 16px
  button-ghost:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.primary}"
    typography: "{typography.button}"
    rounded: "{rounded.none}"
    padding: 12px 16px
  button-danger:
    backgroundColor: "{colors.semantic-error}"
    textColor: "{colors.on-primary}"
    typography: "{typography.button}"
    rounded: "{rounded.none}"
    padding: 12px 16px
  feature-card:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 24px
  feature-card-elevated:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 24px
  product-card:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 32px
  hero-card:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.display-md}"
    rounded: "{rounded.none}"
    padding: 48px
  cta-banner:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.on-primary}"
    typography: "{typography.headline}"
    rounded: "{rounded.none}"
    padding: 48px
  text-input:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 11px 16px
  text-input-focused:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 11px 16px
  text-input-error:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 11px 16px
  newsletter-input:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: 11px 16px
  product-tab:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink-muted}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.none}"
    padding: 16px 20px
  product-tab-selected:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-emphasis}"
    rounded: "{rounded.none}"
    padding: 16px 20px
  resource-tile:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.none}"
    padding: 16px
  customer-logo-tile:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink-muted}"
    typography: "{typography.caption}"
    rounded: "{rounded.none}"
    padding: 24px
  top-nav:
    backgroundColor: "{colors.canvas}"
    textColor: "{colors.ink}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.none}"
    height: 48px
  utility-bar:
    backgroundColor: "{colors.surface-1}"
    textColor: "{colors.ink-muted}"
    typography: "{typography.caption}"
    rounded: "{rounded.none}"
    height: 32px
  footer:
    backgroundColor: "{colors.inverse-canvas}"
    textColor: "{colors.inverse-ink-muted}"
    typography: "{typography.body-sm}"
    rounded: "{rounded.none}"
    padding: 64px 32px
---

## DESIGN

---

IBM's marketing system is a faithful application of **Carbon Design System** — IBM's open-source enterprise design system. The dominant surface is `{colors.canvas}` pure white with `{colors.surface-1}` light gray for elevation, charcoal `{colors.ink}` (#161616) for text, and IBM Blue `{colors.primary}` (#0f62fe) as the single brand accent.

The defining choice is **flat geometry**: every CTA, every card, every input, every container uses square corners (`{rounded.none}` 0px) with thin 1px borders. There are no rounded pills, no soft shadows, no atmospheric gradients. The system is engineered, not stylized.

**IBM Plex Sans** carries the entire type hierarchy. Display sizes (76 / 60 / 42px) run at weight **300** — IBM's signature light display treatment that makes 76px feel calmer than competing brands' 700-weight display. Body type sits at weight 400 with `letter-spacing: 0.16px` (a Carbon precision detail) and line-height 1.50. The voice reads as careful, technical, and trustworthy.

The system reaches for color rarely — IBM Blue marks links, primary CTAs, and the rare full-bleed CTA banner. Charcoal carries every other surface that isn't white. The result is enterprise gravitas without the enterprise stiffness: rigorous, light-weighted, and intentionally restrained.

**Key Characteristics:**
- **Carbon Design System** — IBM's marketing chrome IS Carbon. Buttons are square, inputs are square-with-bottom-rule, corners stay at 0px.
- **Light-weight display type**: Plex Sans at weight 300 for 42–76px headlines is the brand's typographic signature.
- **One accent color**: `{colors.primary}` IBM Blue carries every link, primary CTA, and CTA banner. There is no second brand color.
- White canvas + light gray (`{colors.surface-1}`) + charcoal (`{colors.ink}`) cover 95% of surfaces.
- Footer inverts to charcoal (`{colors.inverse-canvas}` #161616) — the only dark surface above the page break.
- Card hierarchy is carried by 1px hairlines and surface change, never by drop shadow.
- `letter-spacing: 0.16px` on body is a Carbon precision detail — the small positive tracking is part of the brand voice.
- Page rhythm: utility bar → top nav → hero with light-weight headline → feature card grid → customer logo marquee → enterprise feature row → training section → newsletter / sign-in CTA → dark footer.


Build UIs conforming to IBM's Carbon Design System v11. Carbon provides a token-based, accessible, enterprise-grade component library.

## Tokens

## Color Palette

### Core Blues (Primary Action Family)

| Token | Hex | Use |
|-------|-----|-----|
| blue-10 | `#edf5ff` | Light backgrounds |
| blue-20 | `#d0e2ff` | Hover bg (light) |
| blue-30 | `#a6c8ff` | |
| blue-40 | `#78a9ff` | Link (dark themes) |
| blue-50 | `#4589ff` | |
| blue-60 | `#0f62fe` | **Primary action** |
| blue-70 | `#0043ce` | Active state (light) |
| blue-80 | `#002d9c` | |
| blue-90 | `#001d6c` | |
| blue-100 | `#001141` | |

### Grays (Neutral)

| Token | Hex |
|-------|-----|
| gray-10 | `#f4f4f4` |
| gray-20 | `#e0e0e0` |
| gray-30 | `#c6c6c6` |
| gray-40 | `#a8a8a8` |
| gray-50 | `#8d8d8d` |
| gray-60 | `#6f6f6f` |
| gray-70 | `#525252` |
| gray-80 | `#393939` |
| gray-90 | `#262626` |
| gray-100 | `#161616` |

### Support Colors

| Family | 10 | 20 | 30 | 40 | 50 | 60 | 70 | 80 |
|--------|----|----|----|----|----|----|----|----|
| Red | `#fff1f1` | `#ffd7d9` | `#ffb3b8` | `#ff8389` | `#fa4d56` | `#da1e28` | `#a2191f` | `#750e13` |
| Green | `#defbe6` | `#a7f0ba` | `#6fdc8c` | `#42be65` | `#24a148` | `#198038` | `#0e6027` | `#044317` |
| Yellow | `#fcf4d6` | `#fddc69` | `#f1c21b` | `#d2a106` | `#b28600` | `#8e6a00` | `#684e00` | `#483700` |
| Purple | `#f6f2ff` | `#e8daff` | `#d4bbff` | `#be95ff` | `#a56eff` | `#8a3ffc` | `#6929c4` | `#491d8b` |
| Teal | `#d9fbfb` | `#9ef0f0` | `#3ddbd9` | `#08bdba` | `#009d9a` | `#007d79` | `#005d5d` | `#004144` |
| Cyan | `#e5f6ff` | `#bae6ff` | `#82cfff` | `#33b1ff` | `#1192e8` | `#0072c3` | `#00539a` | `#003a6d` |
| Magenta | `#fff0f7` | `#ffd6e8` | `#ffafd2` | `#ff7eb6` | `#ee5396` | `#d02670` | `#9f1853` | `#740937` |

## Theme Tokens

### Background & Layer Tokens

| Token | White | g10 | g90 | g100 |
|-------|-------|-----|-----|------|
| `$background` | `#ffffff` | `#f4f4f4` | `#262626` | `#161616` |
| `$layer-01` | `#f4f4f4` | `#ffffff` | `#393939` | `#262626` |
| `$layer-02` | `#ffffff` | `#f4f4f4` | `#525252` | `#393939` |
| `$layer-accent-01` | `#e0e0e0` | `#e0e0e0` | `#525252` | `#393939` |
| `$field-01` | `#f4f4f4` | `#ffffff` | `#393939` | `#262626` |
| `$field-02` | `#ffffff` | `#f4f4f4` | `#525252` | `#393939` |
| `$border-subtle-00` | `#e0e0e0` | `#c6c6c6` | `#525252` | `#393939` |
| `$border-strong-01` | `#8d8d8d` | `#8d8d8d` | `#8d8d8d` | `#6f6f6f` |

### Text Tokens

| Token | White | g10 | g90 | g100 |
|-------|-------|-----|-----|------|
| `$text-primary` | `#161616` | `#161616` | `#f4f4f4` | `#f4f4f4` |
| `$text-secondary` | `#525252` | `#525252` | `#c6c6c6` | `#c6c6c6` |
| `$text-placeholder` | `#a8a8a8` | `#a8a8a8` | `#6f6f6f` | `#6f6f6f` |
| `$text-on-color` | `#ffffff` | `#ffffff` | `#ffffff` | `#ffffff` |
| `$text-helper` | `#6f6f6f` | `#6f6f6f` | `#a8a8a8` | `#a8a8a8` |
| `$text-error` | `#da1e28` | `#da1e28` | `#ff8389` | `#ff8389` |
| `$text-inverse` | `#ffffff` | `#ffffff` | `#161616` | `#161616` |

### Interactive Tokens

| Token | White | g10 | g90 | g100 |
|-------|-------|-----|-----|------|
| `$interactive` | `#0f62fe` | `#0f62fe` | `#4589ff` | `#4589ff` |
| `$link-primary` | `#0f62fe` | `#0f62fe` | `#78a9ff` | `#78a9ff` |
| `$link-secondary` | `#0043ce` | `#0043ce` | `#a6c8ff` | `#a6c8ff` |
| `$link-visited` | `#8a3ffc` | `#8a3ffc` | `#be95ff` | `#be95ff` |
| `$link-inverse` | `#78a9ff` | `#78a9ff` | `#0f62fe` | `#0f62fe` |
| `$focus` | `#0f62fe` | `#0f62fe` | `#ffffff` | `#ffffff` |
| `$icon-primary` | `#161616` | `#161616` | `#f4f4f4` | `#f4f4f4` |
| `$icon-secondary` | `#525252` | `#525252` | `#c6c6c6` | `#c6c6c6` |

### Button Tokens

| Token | White/g10 | g90/g100 |
|-------|-----------|----------|
| `$button-primary` | `#0f62fe` | `#0f62fe` |
| `$button-primary-hover` | `#0050e6` | `#0050e6` |
| `$button-primary-active` | `#002d9c` | `#002d9c` |
| `$button-secondary` | `#393939` | `#6f6f6f` |
| `$button-secondary-hover` | `#474747` | `#606060` |
| `$button-secondary-active` | `#6f6f6f` | `#393939` |
| `$button-tertiary` | `#0f62fe` | `#ffffff` |
| `$button-danger-primary` | `#da1e28` | `#da1e28` |
| `$button-danger-secondary` | `#da1e28` | `#ff8389` |
| `$button-disabled` | `#c6c6c6` | `#525252` |

### Support / Status Tokens

| Token | White/g10 | g90/g100 |
|-------|-----------|----------|
| `$support-error` | `#da1e28` | `#ff8389` |
| `$support-success` | `#198038` | `#42be65` |
| `$support-warning` | `#f1c21b` | `#f1c21b` |
| `$support-info` | `#0043ce` | `#4589ff` |

## Typography Tokens

All use **IBM Plex Sans** unless noted.

### Utility Styles

| Token | Size | Line Height | Weight | Letter Spacing |
|-------|------|-------------|--------|----------------|
| `label-01` | 12px | 16px | 400 | 0.32px |
| `label-02` | 14px | 18px | 400 | 0.16px |
| `helper-text-01` | 12px | 16px | 400 | 0.32px |
| `helper-text-02` | 14px | 18px | 400 | 0.16px |
| `legal-01` | 12px | 16px | 400 | 0.32px |
| `legal-02` | 14px | 18px | 400 | 0.16px |

### Body Styles

| Token | Size | Line Height | Weight | Letter Spacing |
|-------|------|-------------|--------|----------------|
| `body-compact-01` | 14px | 18px | 400 | 0.16px |
| `body-compact-02` | 16px | 22px | 400 | 0px |
| `body-01` | 14px | 20px | 400 | 0.16px |
| `body-02` | 16px | 24px | 400 | 0px |

### Heading Styles (Productive)

| Token | Size | Line Height | Weight | Letter Spacing |
|-------|------|-------------|--------|----------------|
| `heading-compact-01` | 14px | 18px | 600 | 0.16px |
| `heading-compact-02` | 16px | 22px | 600 | 0px |
| `heading-03` | 20px | 28px | 400 | 0px |
| `heading-04` | 28px | 36px | 400 | 0px |
| `heading-05` | 32px | 40px | 400 | 0px |
| `heading-06` | 42px | 50px | 300 | 0px |
| `heading-07` | 54px | 64px | 300 | 0px |

### Code Style

| Token | Family | Size | Line Height | Weight |
|-------|--------|------|-------------|--------|
| `code-01` | IBM Plex Mono | 12px | 16px | 400 |
| `code-02` | IBM Plex Mono | 14px | 20px | 400 |

## Spacing Tokens

### Component Spacing (mini-unit scale)

| Token | Value |
|-------|-------|
| `$spacing-01` | 2px |
| `$spacing-02` | 4px |
| `$spacing-03` | 8px |
| `$spacing-04` | 12px |
| `$spacing-05` | 16px |
| `$spacing-06` | 24px |
| `$spacing-07` | 32px |
| `$spacing-08` | 40px |
| `$spacing-09` | 48px |

### Layout Spacing

| Token | Value |
|-------|-------|
| `$spacing-10` | 64px |
| `$spacing-11` | 80px |
| `$spacing-12` | 96px |
| `$spacing-13` | 160px |

### Container Sizes

| Token | Value | Use |
|-------|-------|-----|
| `$container-01` | 24px | Small containers |
| `$container-02` | 32px | Default input height (sm) |
| `$container-03` | 40px | Default input height (md) |
| `$container-04` | 48px | Default input height (lg) |
| `$container-05` | 64px | Large containers |

## Icon Sizes

Carbon icons come in four sizes: 16×16, 20×20, 24×24, 32×32.

| Size | Use |
|------|-----|
| 16px | Inline, UI chrome, table actions |
| 20px | Default for most UI contexts |
| 24px | Navigation icons, larger UI |
| 32px | Feature icons, empty states |

## Layer Model

Carbon v11 uses a layering model to handle elevation. Instead of shadows, Carbon uses background-color shifts between layers.

| Layer | Light Themes | Dark Themes |
|-------|-------------|-------------|
| Background (base) | White or g10 | g100 or g90 |
| Layer 01 | One step lighter/darker than bg | One step lighter than bg |
| Layer 02 | One step from layer 01 | One step from layer 01 |
| Layer 03 | One step from layer 02 | One step from layer 02 |

## Motion

| Token | Duration | Use |
|-------|----------|-----|
| fast-01 | 70ms | Micro-interactions |
| fast-02 | 110ms | Toggle, expand |
| moderate-01 | 150ms | Buttons, fields |
| moderate-02 | 240ms | Modal, dropdown |
| slow-01 | 400ms | Page transitions |
| slow-02 | 700ms | Complex choreography |

Standard easing: `cubic-bezier(0.2, 0, 0.38, 0.9)`. Entrance: `cubic-bezier(0, 0, 0.38, 0.9)`. Exit: `cubic-bezier(0.2, 0, 1, 0.9)`.


## Colors

> Source pages: ibm.com (home), /software/ai-productivity, /consulting, /products/cloud-pak-for-aiops, /products/bare-metal-servers, community.ibm.com.

### Brand & Accent
- **IBM Blue** ({colors.primary}): The single brand accent. Links, primary CTAs, CTA banner backgrounds, focus rings.
- **Blue 60** ({colors.blue-60}): Hovered link state.
- **Blue 80** ({colors.blue-80}): Pressed primary button.
- **Blue Hover** ({colors.blue-hover}): Hover state for primary buttons.

### Surface
- **Canvas** ({colors.canvas}): Default page background.
- **Surface 1** ({colors.surface-1}): Light gray (#f4f4f4) — input fields, alternate-row stripes, subtle section bands.
- **Surface 2** ({colors.surface-2}): Slightly darker gray (#e0e0e0) — disabled fields, hairline-as-fill for separators.
- **Hairline** ({colors.hairline}): 1px borders on cards, inputs, dividers.
- **Hairline Strong** ({colors.hairline-strong}): 1px charcoal underline on focused inputs (Carbon's signature focus treatment).
- **Inverse Canvas** ({colors.inverse-canvas}): Charcoal #161616 — footer surface.
- **Inverse Surface 1** ({colors.inverse-surface-1}): One step lighter than inverse canvas — footer column dividers, hovered footer items.

### Text
- **Ink** ({colors.ink}): All headlines and emphasized body type — charcoal #161616.
- **Ink Muted** ({colors.ink-muted}): Secondary type at #525252 — meta, sub-headlines, footer body.
- **Ink Subtle** ({colors.ink-subtle}): Tertiary type at #8c8c8c — disabled, helper text, captions.
- **Inverse Ink** ({colors.inverse-ink}): White on charcoal — footer headings.
- **Inverse Ink Muted** ({colors.inverse-ink-muted}): Light gray on charcoal — footer body.

### Semantic
- **Success Green** ({colors.semantic-success}): Carbon green-50 — success states.
- **Warning Yellow** ({colors.semantic-warning}): Carbon yellow-30 — warning states.
- **Error Red** ({colors.semantic-error}): Carbon red-60 — error states; danger button background.
- **Info Blue** ({colors.semantic-info}): Identical to primary — informational badges.

## Typography

### Font Family

- **IBM Plex Sans** — IBM's open-source proprietary typeface (free for any use). Geometric, slightly humanist, designed specifically for enterprise UI. Fallback: `Helvetica Neue, Arial, sans-serif`.

The same family carries display, body, and caption — there is no display + body pairing. Hierarchy is carried by **size + weight** rather than by family change. Plex Sans is also free / open-source under the SIL Open Font License — making it the easiest custom face on this list to substitute for in implementation.

### Hierarchy

| Token | Size | Weight | Line Height | Letter Spacing | Use |
|---|---|---|---|---|---|
| `{typography.display-xl}` | 76px | 300 | 1.17 | -0.5px | Largest hero headline |
| `{typography.display-lg}` | 60px | 300 | 1.17 | -0.4px | Section opener headlines |
| `{typography.display-md}` | 42px | 300 | 1.20 | 0 | Sub-section headlines, hero card title |
| `{typography.headline}` | 32px | 400 | 1.25 | 0 | Card collection heading, FAQ category |
| `{typography.card-title}` | 24px | 400 | 1.33 | 0 | Feature card title |
| `{typography.subhead}` | 20px | 400 | 1.40 | 0 | Lead body next to display headlines |
| `{typography.body-lg}` | 18px | 400 | 1.50 | 0 | Hero subhead, lead paragraphs |
| `{typography.body}` | 16px | 400 | 1.50 | 0.16px | Default body |
| `{typography.body-sm}` | 14px | 400 | 1.29 | 0.16px | Card body, footer columns |
| `{typography.body-emphasis}` | 14px | 600 | 1.29 | 0.16px | Selected tab label, emphasized body line |
| `{typography.caption}` | 12px | 400 | 1.33 | 0.32px | Captions, meta, utility bar |
| `{typography.button}` | 14px | 400 | 1.29 | 0.16px | All button labels |
| `{typography.eyebrow}` | 14px | 400 | 1.29 | 0.16px | Section eyebrows (Carbon avoids strong eyebrows; uses sentence case 14px) |

### Principles

- **Light-weight display is the brand voice.** Plex Sans at weight 300 for 76px headlines reads as quietly authoritative — switching to 700 would make it look like every other enterprise site.
- **Carbon's `letter-spacing: 0.16px`** on body sizes is a precision detail. Don't remove it.
- **No mono** on marketing surfaces (Plex Mono exists but lives in product surfaces only).
- **Eyebrow typography uses sentence case 14px** — Carbon resists the all-caps tracked eyebrow common to other enterprise brands.
- **Line-heights tighten on display, relax on body**: 1.17 at display-xl, 1.50 at body — proportional to size.

### Note on Font Substitutes

IBM Plex Sans is **free and open-source** (SIL OFL license) and available on Google Fonts. It is the recommended implementation. The Plex family also includes Plex Mono and Plex Serif if expanded typographic needs arise.

## Layout

### Spacing System

- **Base unit**: 4px (Carbon's signature 4-pixel grid).
- **Tokens (front matter)**: `{spacing.xxs}` 4px · `{spacing.xs}` 8px · `{spacing.sm}` 12px · `{spacing.md}` 16px · `{spacing.lg}` 24px · `{spacing.xl}` 32px · `{spacing.xxl}` 48px · `{spacing.section}` 96px.
- Card interior padding: `{spacing.lg}` 24px on feature cards; `{spacing.xl}` 32px on product cards; `{spacing.xxl}` 48px on hero cards and CTA banners.
- Button padding: 12px vertical · 16px horizontal — Carbon spec.
- Form input padding: 11px vertical · 16px horizontal.

### Grid & Container

- Carbon's 16-column grid at desktop, scaling to 8 / 4 columns at tablet / mobile.
- Max content width sits around 1584px (Carbon's max-grid breakpoint).
- Card grids are 4-up at desktop, 2-up at tablet, 1-up at mobile.
- The customer logo marquee uses fixed-width tiles in a flex row, scrolling horizontally on smaller viewports.

### Whitespace Philosophy

Carbon uses precise alignment to a 4-pixel grid as its whitespace system. Sections separate via thin gray rows (`{colors.surface-1}`) rather than via large vertical gaps. Content is dense by design — IBM's customers expect to see a lot on a page, not a lot of air.

## Elevation & Depth

| Level | Treatment | Use |
|---|---|---|
| 0 (flat) | No shadow, no border | Default for body type, hero text, footer body |
| 1 (hairline) | 1px `{colors.hairline}` border on canvas | Feature cards, inputs, list items |
| 2 (surface lift) | `{colors.surface-1}` background on canvas | Alternate-row banners, hovered cards |
| 3 (focus ring) | 2px `{colors.primary}` outline + 1px `{colors.hairline-strong}` underline | Focused input, focused button |

Carbon resists drop shadows on marketing — depth is carried by surface change and 1px hairlines. The exception is product / app surfaces (Carbon documents shadow tokens for elevated panels), but the marketing site barely uses them.

### Decorative Depth

- **Soft blue gradient backdrops** appear behind some hero illustrations — a faint blue-to-white wash that warms the canvas without competing with the headline.
- **No atmospheric depth.** No spotlight cards, no pastel section blocks, no gradient panels.

## Shapes

### Border Radius Scale

| Token | Value | Use |
|---|---|---|
| `{rounded.none}` | 0px | Default — every button, card, input, container |
| `{rounded.xs}` | 2px | Small badges (rare exception) |
| `{rounded.sm}` | 4px | Avatar circles squared, dropdown menus |
| `{rounded.md}` | 6px | (Used rarely; documented for completeness) |
| `{rounded.lg}` | 8px | (Used rarely; documented for completeness) |
| `{rounded.pill}` | 9999px | Status pills, badges in product UI (rare on marketing) |

The brand commits to flat 0px corners. The other tokens exist for product / mobile surfaces but rarely surface on marketing.

### Photography & Illustration Geometry

- IBM uses photography (people, hardware, sports cars) and abstract illustration (geometric mesh, dotted patterns) interchangeably.
- Image frames are flat — no rounded corners.
- Customer logo tiles sit on `{rounded.none}` 0px tiles with thin 1px borders.

## Components

### Buttons

**`button-primary`** — Blue solid CTA. The default primary across all pages.
- Background `{colors.primary}`, text `{colors.on-primary}`, type `{typography.button}`, padding 12px 16px, rounded `{rounded.none}`.
- Pressed state lives in `button-primary-pressed` (background shifts to `{colors.blue-80}`).

**`button-secondary`** — Charcoal solid button — Carbon's "secondary" treatment.
- Background `{colors.ink}`, text `{colors.inverse-ink}`, type `{typography.button}`, padding 12px 16px, rounded `{rounded.none}`.

**`button-tertiary`** — White button with blue 1px border + blue text. Used for tertiary CTAs.
- Background `{colors.canvas}`, text `{colors.primary}`, type `{typography.button}`, rounded `{rounded.none}`, padding 12px 16px. (Border in implementation: 1px `{colors.primary}`.)

**`button-ghost`** — Plain text + chevron, no background until hover.
- Background `{colors.canvas}`, text `{colors.primary}`, type `{typography.button}`, rounded `{rounded.none}`, padding 12px 16px.

**`button-danger`** — Carbon's destructive variant.
- Background `{colors.semantic-error}`, text `{colors.on-primary}`, type `{typography.button}`, rounded `{rounded.none}`, padding 12px 16px.

### Cards & Containers

**`feature-card`** — Default feature highlight tile on the home and product pages.
- Background `{colors.canvas}`, text `{colors.ink}`, type `{typography.body}`, rounded `{rounded.none}`, padding 24px. Stroked with 1px `{colors.hairline}`.

**`feature-card-elevated`** — Same shape on `{colors.surface-1}` ground — used for "Recommended" cards in the latest-content carousel.
- Background `{colors.surface-1}`, otherwise identical structure.

**`product-card`** — Larger product showcase tile.
- Background `{colors.canvas}`, text `{colors.ink}`, type `{typography.body}`, rounded `{rounded.none}`, padding 32px.

**`hero-card`** — Hero composition card with light-weight title, body, and CTA.
- Background `{colors.canvas}`, text `{colors.ink}`, type `{typography.display-md}`, rounded `{rounded.none}`, padding 48px.

**`cta-banner`** — Full-width blue CTA panel near the bottom of the page.
- Background `{colors.primary}`, text `{colors.on-primary}`, type `{typography.headline}`, rounded `{rounded.none}`, padding 48px.

**`resource-tile`** — Smaller article / case-study tile.
- Background `{colors.canvas}`, text `{colors.ink}`, type `{typography.body-sm}`, rounded `{rounded.none}`, padding 16px.

**`customer-logo-tile`** — Single tile in the customer marquee on the home page (Ferrari, Pfizer, etc.).
- Background `{colors.canvas}`, text `{colors.ink-muted}`, type `{typography.caption}`, rounded `{rounded.none}`, padding 24px. 1px hairline border.

### Inputs & Forms

**`text-input`** + **`text-input-focused`** + **`text-input-error`** — Carbon's input chrome.
- Background `{colors.surface-1}`, text `{colors.ink}`, type `{typography.body}`, rounded `{rounded.none}`, padding 11px 16px.
- Focus state replaces the bottom 1px hairline with a 2px `{colors.primary}` underline (Carbon's signature focus treatment).
- Error state adds 2px `{colors.semantic-error}` bottom underline.

**`newsletter-input`** — The "Stay connected" newsletter capture on the home page.
- Background `{colors.surface-1}`, text `{colors.ink}`, type `{typography.body}`, rounded `{rounded.none}`, padding 11px 16px. Adjacent submit is `button-primary`.

### Tabs

**`product-tab`** + **`product-tab-selected`** — The horizontal tab strip on product pages and the home "Recommended" carousel.
- Default: `{colors.canvas}` background, `{colors.ink-muted}` text, rounded `{rounded.none}`, padding 16px 20px. Bottom 1px hairline.
- Selected: `{colors.canvas}` background, `{colors.ink}` text, `{typography.body-emphasis}` weight, bottom 2px `{colors.primary}` underline. Same padding / rounding.

### Navigation

**`top-nav`** — Sticky white bar with the IBM logomark left, nav categories center, and search / sign-in icons right.
- Background `{colors.canvas}`, text `{colors.ink}`, type `{typography.body-sm}`, height 48px. 1px bottom hairline.

**`utility-bar`** — Slim gray ribbon above the top nav with location switch, contact, search shortcuts.
- Background `{colors.surface-1}`, text `{colors.ink-muted}`, type `{typography.caption}`, height 32px.

### Footer

**`footer`** — Charcoal footer (`{colors.inverse-canvas}`) with the IBM wordmark left and 5–6 columns of caption-sized links. The only inverted surface above the page break.
- Background `{colors.inverse-canvas}`, text `{colors.inverse-ink-muted}`, type `{typography.body-sm}`, padding 64px 32px.

## Do's and Don'ts

### Do

- Use `{rounded.none}` 0px on every CTA, card, input, and container. The flat-square aesthetic is the brand.
- Pair Plex Sans weight 300 for display sizes (42px+) with weight 400 for body. Resist the urge to bold the headline.
- Reserve `{colors.primary}` IBM Blue for primary CTAs, links, focused-input underlines, and CTA banner. Do not use it as a card background or eyebrow color.
- Apply `letter-spacing: 0.16px` to body sizes. It's a Carbon precision detail and part of the typographic voice.
- Use surface change (`canvas` → `surface-1`) and 1px hairlines for card hierarchy. Skip drop shadows.
- Stick to sentence case for eyebrows and section labels — Carbon resists all-caps tracking.
- Invert to `{colors.inverse-canvas}` only at the footer; the rest of the page stays light.

### Don't

- Don't bold display headlines. Plex Sans at weight 300; weight 700 makes it look generic.
- Don't add atmospheric depth (gradient backdrops, drop shadows, atmospheric overlays) outside the documented soft-blue hero gradient.
- Don't introduce a second brand color. IBM Blue is the only chromatic accent; status semantics use the documented green / yellow / red.
- Don't replace IBM Plex Sans with Inter or Helvetica without preserving the `letter-spacing: 0.16px` and weight-300 display treatment.
- Don't use pill-shaped buttons. Carbon uses square corners; pills read as a different brand.
- Don't write all-caps tracked eyebrows. Carbon's eyebrows are sentence case at 14px.

### Anti-Patterns

- Non-IBM Plex fonts
- `bx--` prefix (v10; use `cds--` for v11)
- Arbitrary border-radius (Carbon: 0px default, 4px for tags/pills only)
- Drop shadows on components that lack them in spec
- Overriding focus ring styles
- Colors outside the Carbon palette
- Spacing values not on the scale


## Responsive Behavior

### Breakpoints

| Name | Width | Key Changes |
|---|---|---|
| Max | 1584px | Carbon max grid; gutters expand |
| Desktop-XL | 1312px | Default desktop layout |
| Desktop | 1056px | Card grid 4-up maintained |
| Tablet | 672px | Card grid 4-up → 2-up; nav becomes hamburger |
| Mobile | 320px | Single-column; display-xl scales 76px → ~32px |

### Touch Targets

- Carbon spec: 48px minimum tap target. Buttons and inputs hold 48px on touch viewports.
- Top-nav links grow from 36px to 48px tap height on touch.
- Tab strip rows hold 48px tap height.

### Collapsing Strategy

- **Top nav**: links collapse to a hamburger overlay below 672px. Logomark and search icon stay on the bar.
- **Utility bar**: hides below 672px to reclaim vertical space.
- **Card grid**: 4-up → 2-up at 1056px → 1-up below 672px.
- **Display type**: `{typography.display-xl}` 76px scales toward 42px on mobile while preserving the weight-300 treatment.
- **Footer**: 6-column link grid → 3-column at tablet → 1-column at mobile.

### Image Behavior

- Customer logos in the marquee maintain aspect ratio and may collapse to 2-row scroll below 672px.
- Hero illustrations scale proportionally; below 672px they may stack above the headline rather than sit beside it.

## Implementation Checklist

1. Focus on ONE component at a time and reference it by its `components:` token name.
2. Default body to `{typography.body}` at weight 400 with `letter-spacing: 0.16px`. Don't remove the tracking.
3. When introducing a new section, decide whether it sits on `{colors.canvas}` (default) or on `{colors.surface-1}` (alternate band). The two-surface rhythm is the rhythm.
4. Add new variants as separate component entries (`button-primary-pressed`, `text-input-error`, `text-input-focused`).
5. Treat IBM Blue as scarce: links, primary CTA, CTA banner, focus underline. Anything beyond that is drift.
6. Resist rounded corners. If a designer pushes for 4px rounding, the brand is shifting away from Carbon.

