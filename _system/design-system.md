# Atlas Design System — Complete Reference

> Source: [github.com/Tripletex-AS/tripletex-frontend/tree/main/design-system](https://github.com/Tripletex-AS/tripletex-frontend/tree/main/design-system)
> This file is a local copy of the Atlas design-system directory for use in HTML/CSS prototyping.

---



---

# FOUNDATIONS

---

## colors.md

# Color Foundation

Atlas uses a two-layer colour system: **global palette** (raw values, named by hue and shade) and **semantic tokens** (named by purpose, mapped to global palette values). Components and patterns always use semantic tokens; global palette values appear only when defining a new semantic token. For the broader token model see [`tokens.md`](tokens.md).

Light mode only. Dark mode is a future addition — see *Open Questions*.

**Figma reference:** [Atlas Library — Color Styles](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=8517-4614&p=f&t=a5rsetCbVeluqKNi-11)

---

## Global palette

### Misc

| Token | Value |
|---|---|
| `--global-misc-white` | #ffffff |
| `--global-misc-background` | #f7f8fc |
| `--global-misc-contrast` | #010a59 |
| `--global-misc-transparent` | #ffffff00 |

### Grey

| Token | Value |
|---|---|
| `--global-grey-05` | #f4f5f6 |
| `--global-grey-10` | #e9eaed |
| `--global-grey-20` | #d5d7db |
| `--global-grey-40` | #abafb7 |
| `--global-grey-60` | #818794 |
| `--global-grey-71` | #6b7280 |
| `--global-grey-80` | #51596a |
| `--global-grey-100` | #2e384d |
| `--global-grey-120` | #0f131a |
| `--global-grey-100-30` | #2e384d4d |

### Blue

| Token | Value |
|---|---|
| `--global-blue-05` | #f2f5ff |
| `--global-blue-10` | #e6ebff |
| `--global-blue-20` | #ced9fe |
| `--global-blue-40` | #9db3fd |
| `--global-blue-60` | #6c8dfc |
| `--global-blue-80` | #3b67fb |
| `--global-blue-100` | #0a41fa |
| `--global-blue-120` | #0834c7 |
| `--global-blue-130` | #002992 |

### Turquoise

| Token | Value |
|---|---|
| `--global-turquoise-05` | #f4fafa |
| `--global-turquoise-10` | #e8f5f5 |
| `--global-turquoise-20` | #d4ebeb |
| `--global-turquoise-40` | #abd6d6 |
| `--global-turquoise-60` | #80c1c2 |
| `--global-turquoise-80` | #57adae |
| `--global-turquoise-100` | #30999b |
| `--global-turquoise-120` | #206768 |

### Green

| Token | Value |
|---|---|
| `--global-green-05` | #f4fbf4 |
| `--global-green-10` | #eaf7e9 |
| `--global-green-20` | #d6eed5 |
| `--global-green-40` | #addeab |
| `--global-green-60` | #84cd81 |
| `--global-green-80` | #5bbc57 |
| `--global-green-100` | #33ac2e |
| `--global-green-120` | #247820 |

### Red

| Token | Value |
|---|---|
| `--global-red-05` | #fef4f5 |
| `--global-red-10` | #fdeaec |
| `--global-red-20` | #fbd6da |
| `--global-red-40` | #f6aeb4 |
| `--global-red-60` | #f1868f |
| `--global-red-80` | #ec5e6a |
| `--global-red-100` | #e83645 |
| `--global-red-120` | #b52a36 |

### Yellow

| Token | Value |
|---|---|
| `--global-yellow-05` | #fffcf5 |
| `--global-yellow-10` | #fff9ea |
| `--global-yellow-20` | #fef3d7 |
| `--global-yellow-40` | #fce6af |
| `--global-yellow-60` | #fada87 |
| `--global-yellow-80` | #f8cd5f |
| `--global-yellow-100` | #f7c137 |
| `--global-yellow-120` | #c4992c |

### Purple

| Token | Value |
|---|---|
| `--global-purple-05` | #f9f6ff |
| `--global-purple-10` | #f3eeff |
| `--global-purple-20` | #e8ddff |
| `--global-purple-40` | #d1bbff |
| `--global-purple-60` | #ba98ff |
| `--global-purple-80` | #a376ff |
| `--global-purple-100` | #8c54ff |
| `--global-purple-120` | #7043cc |

---

## Brand and illustration colours

Logo, Sparcle accent, and illustration colours are defined in Figma for brand and illustration work. They are **not part of the colour system** and must not be used in components or patterns.

---

## Semantic tokens

### Text

| Token | Value | Use |
|---|---|---|
| `--text-primary` | #2e384d | Body text |
| `--text-muted` | #6b7280 | Secondary / supporting text |
| `--text-disabled` | #51596a | Text on disabled elements |
| `--text-placeholder` | #abafb7 | Input placeholder text |
| `--text-link` | #0a41fa | Hyperlinks |
| `--text-active` | #0a41fa | Active state text |
| `--text-action` | #0a41fa | Action labels |
| `--text-on-action` | #ffffff | Text on filled action buttons |
| `--text-footer-primary` | #f2f5ff | Primary text in footer |
| `--text-footer-link` | #9db3fd | Links in footer |

### Surface

| Token | Value | Use |
|---|---|---|
| `--surface-background` | #f7f8fc | Page background |
| `--surface-default` | #ffffff | Default card / panel surface |
| `--surface-nav` | #d4ebeb | Navigation background |
| `--surface-disabled` | #e9eaed | Disabled element background |
| `--surface-tooltip` | #2e384d | Tooltip background |
| `--surface-footer` | #010a59 | Footer background |
| `--surface-modal` | #2e384d4d | Modal overlay |

#### Surface state variants

Each semantic state (info, warning, error, success, automation) has four surface levels. **CSS variable names are formed as `--surface-{state}-{suffix}`** — e.g. `--surface-error-rest`, `--surface-warning-hover`, `--surface-info-active`. The table below is the authoritative source for the values; component rule files reference the variable names directly.

| Suffix | Use |
|---|---|
| `-rest` | Default background |
| `-hover` | Hover state |
| `-highlight` | Emphasised or selected |
| `-active` | Pressed or filled accent |

| State | `-rest` | `-hover` | `-highlight` | `-active` |
|---|---|---|---|---|
| Info | #f2f5ff | #e6ebff | #ced9fe | #0a41fa |
| Warning | #fffcf5 | #fff9ea | #fef3d7 | #f7c137 |
| Error | #fef4f5 | #fdeaec | #fbd6da | #e83645 |
| Success | #f4fbf4 | #eaf7e9 | #d6eed5 | #33ac2e |
| Automation | #f9f6ff | #f3eeff | #e8ddff | #7043cc |
| Neutral active | — | — | — | #abafb7 |

### Border

| Token | Value | Use |
|---|---|---|
| `--border-primary` | #818794 | Default border |
| `--border-secondary` | #abafb7 | Softer border |
| `--border-muted` | #d5d7db | Subtle divider |
| `--border-faint` | #e9eaed | Barely visible border |
| `--border-disabled` | #abafb7 | Disabled element border |
| `--border-hover` | #9db3fd | Hover state border |
| `--border-active` | #0a41fa | Active / focused border |
| `--border-focus` | #6c8dfc | Focus ring |
| `--border-underline` | #e6ebff | Underline accent |
| `--border-info` | #6c8dfc | Info state |
| `--border-warning` | #f7c137 | Warning state |
| `--border-error` | #ec5e6a | Error state |
| `--border-success` | #5bbc57 | Success state |
| `--border-automation` | #a376ff | Automation state |

#### Border interaction variants

| Token | Value |
|---|---|
| `--border-error-hover` | #f6aeb4 |
| `--border-error-focus` | #b52a36 |
| `--border-warning-hover` | #fce6af |
| `--border-warning-focus` | #c4992c |
| `--border-automation-hover` | #d1bbff |
| `--border-automation-focus` | #7043cc |

### Action

| Token | Value | Use |
|---|---|---|
| `--action-primary-rest` | #0a41fa | Primary button default |
| `--action-primary-hover` | #0834c7 | Primary button hover |
| `--action-primary-active` | #002992 | Primary button pressed |
| `--action-secondary-rest` | #e6ebff | Secondary button default |
| `--action-secondary-hover` | #ced9fe | Secondary button hover |
| `--action-secondary-active` | #9db3fd | Secondary button pressed |
| `--action-tertiary-rest` | #ffffff00 | Tertiary button default (transparent) |
| `--action-tertiary-hover` | #ced9fe | Tertiary button hover |
| `--action-tertiary-active` | #9db3fd | Tertiary button pressed |
| `--action-neutral-rest` | #f7f8fc | Neutral button default |
| `--action-neutral-hover` | #ced9fe | Neutral button hover |
| `--action-neutral-active` | #9db3fd | Neutral button pressed |

---

## Chart and graph colours

Defined in Figma; not yet tokenised in code. Reference Figma directly until tokens land — see *Open Questions*.

[Figma — Chart & Graph Colours](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=17437-4987)

---

## Rule: Use semantic tokens, never raw values or global tokens

**Description**

Components and patterns reference colour exclusively through semantic tokens (`--text-*`, `--surface-*`, `--border-*`, `--action-*`). Global palette tokens (`--global-*`) appear only inside semantic token definitions. Hex values are never hardcoded.

**Violations**

- Global palette token used directly in a component (e.g. `--global-blue-100` instead of `--action-primary-rest`) — error
- Hex value hardcoded instead of referenced via a token — error
- Brand, Sparcle, or illustration colour used in a component or pattern — error

---

## Related Rules

- [`tokens.md`](tokens.md) — token system this file's tokens slot into.
- [`typography.md`](typography.md) — text styles that pair with text colour tokens.

---

## Open Questions

- **Dark mode tokens** — file covers light mode only. A separate token set will be added when dark mode is scoped.
- **Chart and graph tokens** — defined in Figma but not yet in code. Coordinate with Astro for `--chart-*` token names.
- **Purpose-based text token naming** — Atlas uses appearance-based names like `--text-muted`. Many modern design systems lean toward purpose-based names (e.g. naming by role — body, secondary, supporting — rather than by appearance). Worth a coordinated rename pass during dark-mode scoping; do not invent purpose-based aliases ad-hoc.


---

## typography.md

# Typography Foundation

Atlas uses Rubik as the base font family. Typography is defined in two layers: **base tokens** (raw values for font family, size, weight, line height, letter spacing) and **text styles** (named styles built on top of base tokens, defined in Figma). For the broader token model see [`tokens.md`](tokens.md).

**Figma reference:** [Typography Styles](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library)

---

## Base tokens

| Token | Value |
|---|---|
| `--font-family-base` | "Rubik", sans-serif |
| `--font-size-base` | 14px |
| `--font-weight-regular` | 400 |
| `--line-height-base` | 1.4 |
| `--letter-spacing-base` | 0 |

---

## Text styles

Defined in Figma; not yet tokenized in code. Reference Figma directly until text-style tokens land (see *Open Questions*).

Each style ships in regular and medium weights except Paragraph, Tabular, and Decoration (regular only).

| Style | Size | Weights |
|---|---|---|
| Text 2XL | 30px | Regular, Medium |
| Text XL | 20px | Regular, Medium |
| Text LG | 16px | Regular, Medium |
| Text Base | 14px | Regular, Medium |
| Paragraph | 14px | Regular |
| Tabular | 14px | Regular |
| Decoration | 12px | Regular |

---

## Rule: Font family

**Description**

All text uses Rubik via `--font-family-base`. No other font families.

**Violations**

- Font family other than Rubik — error
- Hardcoded font family instead of `--font-family-base` — error

---

## Rule: Font smoothing

**Description**

Rubik renders thinner in browsers than in Figma because Figma uses subpixel antialiasing by default. Apply this CSS globally so web and Figma match.

**How to Apply**

```css
body {
  -webkit-font-smoothing: antialiased;  /* Chrome, Safari */
  -moz-osx-font-smoothing: grayscale;   /* Firefox on macOS */
}
```

**Violations**

- Font smoothing applied only to some components instead of globally — error
- Font smoothing not applied at all — error

---

## Rule: Font sizing

**Description**

Component and layout text uses one of the text styles in the table above. Until styles are tokenized, reference the Figma style directly.

**Violations**

- Font size not in the text-style scale — warning
- Hardcoded font size instead of the text-style scale — error

---

## Rule: Font weights

**Description**

Use Regular (400) or Medium (500). No other weights.

**Violations**

- Font weight other than 400 or 500 — error

---

## Rule: No italics

**Description**

Atlas products do not use italic text. Italic styling reduces readability for users with dyslexia or low vision, and Rubik's italic forms render unevenly across browsers. Use Medium weight for emphasis instead.

**Violations**

- `font-style: italic` applied to UI text — error
- Italic used for emphasis instead of Medium weight — error
- `<em>` or `<i>` rendered as italic — warning (the element is fine for semantic emphasis; override the visual to upright + Medium weight)
- Italic used for "secondary" or "quoted" treatment instead of `--text-muted` or proper block-quote styling — error

**Examples**

✓ "Click **Save** to confirm." — emphasis via Medium weight.

✗ "Click *Save* to confirm." — italic.

---

## Rule: Ligatures stay enabled

**Description**

Rubik ships with ligatures (multi-character glyphs like `fi`, `fl`, `ff`) that are part of the font's designed rendering. Disabling them — via `font-variant-ligatures: none` or `text-rendering: optimizeSpeed` — visibly breaks the typography.

**Violations**

- `font-variant-ligatures: none` (or any value that disables common ligatures) — error
- `text-rendering: optimizeSpeed` on UI text — error (disables ligatures and kerning)
- Disabling ligatures globally as a "performance optimisation" without measurement — warning

---

## Rule: No emojis

**Description**

Atlas products do not use emoji glyphs in UI strings — labels, buttons, titles, navigation, system messages, alerts, banners, table content, and any other product surface. Emojis are allowed only in **sales / marketing body copy** (Product Spotlight Banner body, news posts, in-product promotional messages) where they support tone and emphasis.

User-generated content (customer names, comment text, free-form fields the user types) is out of scope of this rule — that's user data, not Atlas UI.

Emojis render inconsistently across operating systems and browsers (different vendor designs), can be verbalised unexpectedly by screen readers, and carry cultural ambiguity. None of that fits the product-UI consistency standard. For meaning conveyed by a small glyph in UI, use an icon from the Atlas icon library — see [`icons.md`](icons.md).

**Violations**

- Emoji glyph in any product UI string (label, button, title, navigation item, system message, alert, banner heading, table cell content, status component, etc.) — error
- Emoji glyph in a Product Spotlight Banner heading — warning (emojis belong in the body copy if anywhere)

**Examples**

✓ Sales / marketing body copy inside a Product Spotlight Banner uses a small emoji decoration to mark tone (allowed in this context).

✗ Page header alert text leads with an emoji glyph — use the alert's built-in icon system.

✗ Button label includes an emoji glyph — chrome stays plain text.

✗ Table column header includes an emoji glyph.

---

## Related Rules

- [`tokens.md`](tokens.md) — token system that the base tokens slot into.
- [`colors.md`](colors.md) — text colour tokens that pair with text styles.
- [`spacing.md`](spacing.md) — spacing scale that composes with text styles.

---

## Open Questions

- **Usage rules per text style** — when to use Text Base vs Paragraph vs Tabular vs Text LG / XL / 2XL. UX team to define.
- **Paragraph vs Tabular distinction** — both 14px regular; Tabular is likely optimised for numeric / data alignment, but the boundary with Text Base is undefined.
- **Text-style tokens** — Figma defines the styles but no `--text-style-*` tokens exist in code. Coordinate with Astro.
- **Global font smoothing implementation** — not yet applied globally in the codebase. Assigned to @kennetvu and @Khado.


---

## spacing.md

# Spacing Foundation

Atlas uses a single spacing scale across all components, layouts, and patterns. Token values live in [`tokens.md`](tokens.md); this file documents the rules for using them.

**Figma reference:** [Atlas Library — Spacing](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library)

---

## The scale

`0, 1px, 2px, 4px, 8px, 12px, 16px, 20px, 24px, 28px, 32px, 36px, 40px, 44px, 48px, 52px, 56px, 60px, …`

Two hairline values (1px, 2px), then steps of 4px with no upper bound.

---

## Rule: Use only spacing scale values

**Description**

Every `gap`, `margin`, `padding`, `top`, `left`, `width`, and `height` that represents space between or inside UI elements uses a value from the scale. Off-scale values erode visual rhythm even when each looks fine in isolation.

**How to Apply**

- Use spacing tokens from [`tokens.md`](tokens.md) in CSS, or the spacing styles attached to Auto Layout in Figma.
- Don't type pixel values directly into a component's spacing properties.

**Violations**

- Spacing value not on the scale (5px, 10px, 14px, 18px, 30px, etc.) — warning (flagged at warning level because legitimate exceptions exist — see *Exceptions* below; off-scale needs human confirmation, not auto-rejection)

**Examples**

✓ Correct

```css
.card {
  padding: 16px;          /* on scale */
  gap: 8px;               /* on scale */
  border-bottom: 1px solid var(--border-default); /* hairline */
}
```

✗ Wrong

```css
.card {
  padding: 18px;          /* off scale — flag as warning */
  gap: 10px;              /* off scale — flag as warning */
  margin-top: 30px;       /* off scale — flag as warning */
}
```

---

## Exceptions

Off-scale values are not a violation in these cases:

- **Illustrations** — illustration sizes and internal proportions follow their own rules, not the spacing scale.
- **Optical icon alignment** — components may use off-scale padding to visually align an icon with adjacent text (for example icon buttons and chips, where mathematically correct padding looks visually off).

---

## Related Rules

- [`tokens.md`](tokens.md) — underlying token values for each step on the scale.
- [`patterns/button-placement.md`](../../patterns/button-placement.md) — canonical spec for which spacing value applies in each button-placement context (12px / 16px / 24px form-and-button rules; 8px between buttons in a group).


---

## tokens.md

# Tokens Foundation

Atlas tokens are defined in two layers: **global tokens** (raw values, named by category and scale, e.g. `--global-grey-20`) and **semantic tokens** (named by purpose, mapped to global tokens, e.g. `--surface-background`). Components and patterns always use semantic tokens; global tokens appear only when defining a new semantic token.

For colour and typography tokens see [`colors.md`](colors.md) and [`typography.md`](typography.md). For the spacing scale with usage guidance see [`spacing.md`](spacing.md).

---

## Element heights

| Token | Value | Use |
|---|---|---|
| `--element-height-tiny` | 20px | Smallest interactive elements |
| `--element-height-small` | 24px | Small interactive elements |
| `--element-height-medium` | 32px | Medium interactive elements, small buttons |
| `--element-height-large` | 40px | Large interactive elements, medium buttons |

Button heights map to element heights: Medium button = `--element-height-large` (40px); Small button = `--element-height-medium` (32px). See [`buttons.md`](../components/buttons.md) for button sizing rules.

---

## Icon sizes

| Token | Value | Use |
|---|---|---|
| `--icon-size-small` | 20px | Inline icons, dense layouts |
| `--icon-size-medium` | 24px | Default icon size |
| `--icon-size-large` | 48px | Not yet tokenised — reference only |

---

## Illustration sizes

| Name | Size | Use |
|---|---|---|
| Small | 100×100px | Not yet tokenised — reference only |
| Medium | 200×200px | Not yet tokenised — reference only |
| Large | 400×400px | Not yet tokenised — reference only |

---

## Border radius

| Token | Value | Use |
|---|---|---|
| `--radius-default` | 4px | Default border radius for all components |
| `--radius-full` | 99999px | Fully rounded elements (chips, badges, pills) |

---

## Spacing scale

`0, 1px, 2px, 4px, 8px, 12px, 16px, 20px, 24px, 28px, 32px, 36px, 40px, 44px, 48px, 52px, 56px, 60px, …`

Two hairline values (1px, 2px), then steps of 4px with no upper bound. For when to use which value, see [`spacing.md`](spacing.md).

---

## Rule: Use tokens, never raw values

**Description**

Components and patterns reference design values through tokens. Hex, hardcoded pixels, and global tokens used directly in a component are not allowed.

**Violations**

- Hardcoded pixel or hex value instead of a token — error
- Global token used directly in a component (e.g. `--global-grey-20` instead of `--surface-disabled`) — error
- Tailwind class that maps to a global token instead of the semantic equivalent — warning
- Off-scale spacing value (5px, 10px, 14px, etc.) — warning
- Icon size other than 20px, 24px, or 48px — warning

**Exceptions**

- Illustrations don't follow the spacing scale.
- Components may use off-scale padding for optical alignment of icons (icon buttons, chips). Flag as warning, not error — assume good intent and confirm it's intentional.

---

## Related Rules

- [`colors.md`](colors.md) — colour tokens (global palette + semantic).
- [`typography.md`](typography.md) — typography tokens (base + text styles).
- [`spacing.md`](spacing.md) — spacing scale with usage guidance.
- [`icons.md`](icons.md) — icon source-of-truth (Atlas library, selection process); the icon-size tokens defined in this file live there in context.
- [`buttons.md`](../components/buttons.md) — button heights map to element-height tokens.

---

## Open Questions

- **Tailwind semantic token mapping** — Tailwind has partial global token coverage but no semantic token mapping. Developers use `var(--surface-background)` in CSS rather than `bg-surface-background` Tailwind classes. On the Astro roadmap, no deadline.
- **`--icon-size-large` token** — 48px size is referenced but not tokenised.
- **Illustration size tokens** — Small / Medium / Large illustration sizes documented but no `--illustration-size-*` tokens exist.


---

## icons.md

# Icon Foundation

Atlas has its own icon library. Atlas icons are largely based on the Material Design library but include custom icons and customised Material variants — Material Design is inspiration and a fallback starting point, not Atlas's canonical icon source.

**References:**

- [Atlas Library — Icons](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=3-190&p=f&t=a5rsetCbVeluqKNi-11) — full icon set, naming, variants (Figma).
- [Atlas Storybook — Icons](https://atlas.tripletex.dev/#/Icons/IconStory) — browseable, ready-to-use components.

For icon **sizes** see [`tokens.md`](tokens.md) (`--icon-size-small` 20px, `--icon-size-medium` 24px, `--icon-size-large` 48px not yet tokenised). Icons **inherit their colour from the label, text, or component they sit next to** — Atlas has no icon-specific colour tokens. For cross-product **consistency** rules and icon-to-action mappings see [`patterns/icon-usage.md`](../../patterns/icon-usage.md).

---

## Rule: Icon source — Atlas first

**Description**

Every icon rendered in an Atlas-built UI comes from the Atlas icon library. When a designer or team needs an icon that isn't in Atlas yet, the path is: check Atlas → if missing, find a suitable Material Design icon as a starting point → coordinate with the Astro design system team to add it to Atlas centrally. Don't unilaterally inline a Material icon. Don't paste in icons from other sources.

Without this discipline the product ends up with different icons for the same actions — a confusing, hard-to-learn UX. Maintaining one canonical Atlas icon per action is collective responsibility.

**How to Apply**

1. **Check the Atlas icon library first** — Figma and Storybook references above. If a canonical Atlas icon fits the use case, use it.
2. **If no Atlas icon fits** — find a suitable Material Design icon as a *starting point*. Material is inspiration; the icon doesn't enter the Atlas system until step 3.
3. **Coordinate with the Astro design system team in Slack** before introducing the icon to product code. The team adds the new icon to the Atlas library (possibly customising the Material original) so every team uses the same canonical version.
4. Don't inline a non-Atlas icon as a one-off *"we'll fix it later"* move. The fix-it-later doesn't happen; the divergence stays.

**Violations**

- Icon used in product UI that isn't in the Atlas icon library — error
- Atlas icon substituted with a non-Atlas equivalent (custom SVG, Material original, third-party icon) — error
- New icon added to product code without coordinating with the Astro design system team — error

**Examples**

✓ A search field renders the Atlas magnifying-glass icon from the Atlas icon library.

✓ A new product flow needs a *barcode* icon. Atlas doesn't have one; the team finds Material's `qr_code_scanner` as a starting point and pings `#astro_reception` to add a customised Atlas version.

✗ A team inlines Material's `edit` icon directly into a component because *"Atlas's edit icon doesn't quite fit our use case"* — coordinate with the design system team instead.

✗ A custom SVG icon shipped without Atlas-team review, producing the fifth *feedback* icon variant in the product.

---

## Related Rules

- [`tokens.md`](tokens.md) — icon size tokens.
- [`colors.md`](colors.md) — text colour tokens that icons inherit from in context (e.g. `--text-on-action`, `--text-action`, `--text-primary`, `--text-muted`).
- [`patterns/icon-usage.md`](../../patterns/icon-usage.md) — icon-to-action mappings and cross-product consistency.


---

## number-formats.md

# Number Formats Foundation

> **Status: DRAFT — pending team review.** Drafted from the Atlas Library Figma `Number Formats` and `Date Formats` panels — Figma is the design source of truth for this foundation per decision #38, so the rules below are a verbatim transcription of what Figma prescribes, organised into the canonical rule template. Promote to ✅ once the wider team has signed off.

This page defines how to format dates, numbers, currencies, percentages, units, abbreviations, time, and digit-grouped identifiers across Tripletex products. Tripletex serves Norwegian businesses, so **Norwegian locale conventions are the default**; an English fallback exists for explicitly-English surfaces. Where Norwegian and English disagree on a format (separator, percent spacing, month-name capitalisation, etc.), the rule names both variants.

For input-side number alignment (right-aligned numeric values, left-aligned text-entry), see `design-rules/components/forms/input.md` § "Input alignment by input type". This file owns *what the value looks like*; `forms/input.md` owns *which side of the field it sits on*.

For chart axis labels and how surrounding components must accommodate compact-number widths, see `charts.md` *(not yet documented — see `TODO.md`)*. The compact-number formats themselves are owned by this file (Rule 5).

Canonical Figma reference for every rule in this file: [Atlas Library — Number Formats](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=9050-13178).

---

## Rule: Formatted numbers stay on one line

**Description**

A formatted number is a single semantic unit — "NOK 25 000,00" reads as one value, not as four words that may be broken across a line. If layout pressure causes "NOK 25 000,00" to wrap to "NOK 25" on one line and "000,00" on the next, the user has to re-parse the value, and at a glance the wrapped halves can read as two separate numbers. The rule: every formatted number, date, currency value, percentage, unit value, abbreviation, and digit-grouped identifier sits on a single line.

**Date ranges are the explicit exception.** A date range like `01.11.2024 – 31.12.2024` may wrap, **provided each side stays whole on its own line and the two halves are vertically aligned**. The wrapping happens between the start date and the end date (around the dash), never inside a single date.


**How to Apply**

1. Wrap the value in a span with `white-space: nowrap`:
   ```html
   <span style="white-space: nowrap">NOK 25 000,00</span>
   ```
   Set in CSS at the component or utility-class level when possible rather than inline.
2. **For date ranges**: don't wrap individual dates. If the range needs to wrap to fit the available width, wrap *between* the start and end dates (typically by stacking the dates vertically with the dash on its own line or at the end of the first line):
   ```
   01.11.2024
   – 31.12.2024
   ```
   ```
   nov. – des.
        2024
   ```
   Vertically align the two dates so the user can read them as a pair.
3. In tables, set `white-space: nowrap` on the relevant cell — not just on the value span — so the table cell doesn't fold mid-value when columns are squeezed.
4. Group similar data (same column type, same row context) so the eye reads the formatted values as a series rather than as scattered fragments.

**Violations**

- A formatted number wrapping mid-value (e.g. `NOK 25` on one line, `000,00` on the next) — error
- A date wrapping mid-value (e.g. `16. jan.` on one line, `2025` on the next) — error
- A unit value wrapping between the number and the unit (e.g. `2` on one line, `stk` on the next) — error
- A date range wrapping mid-date instead of between the start and end dates — error
- A wrapped date range where the two dates are not vertically aligned — warning
- Number cells in a table missing `white-space: nowrap` such that values fold under column pressure — warning

**Examples**

✓ Correct: `<span style="white-space: nowrap">NOK 25 000,00</span>` renders as a single inline block, even in a narrow table cell.

✓ Correct: A date range that wrapped to two lines as `01.11.2024 / – 31.12.2024` with the dates vertically aligned and the dash leading the second line.

✗ Wrong: `NOK 25` on one line and `000,00` on the next — the user reads two separate numbers.

✗ Wrong: `01.11` on one line and `.2024 – 31.12.2024` on the next — the first date itself is broken.

---

## Rule: Norwegian locale defaults

**Description**

Norwegian uses **comma as decimal separator** and **space as thousands separator**: `25 000,00`. English uses **period as decimal separator** and **space as thousands separator** (Tripletex convention — not the comma-thousands of US English): `25 000.00`. The space-as-thousands is shared across both locales in Tripletex; only the decimal separator differs.

The locale of the value follows the locale of the surface it appears on. A Norwegian-language page renders values with comma decimal; an English-language page renders the same numeric value with period decimal. The thousands-separator-space stays the same in both.


**How to Apply**

| Locale | Decimal | Thousands | Example |
|---|---|---|---|
| Norwegian (default) | `,` (comma) | ` ` (space) | `25 000,00` |
| English | `.` (period) | ` ` (space) | `25 000.00` |

Use `Intl.NumberFormat` or an equivalent locale-aware utility — never concatenate strings to produce these manually, because Tripletex switches locale based on user preference and hand-built strings drift.

**Violations**

- Norwegian value using period as decimal separator (`25 000.00` on a Norwegian-language page) — error
- English value using comma as decimal separator (`25 000,00` on an English-language page) — error
- Either locale using comma or other character as thousands separator instead of space — error (no `25,000.00` US-style)
- Hand-rolled string formatting that bypasses locale-aware utilities — warning (the value may be correct today but drifts on locale switch)

**Examples**

✓ Correct (Norwegian page): `25 000,00`, `1 234,56`, `0,5`

✓ Correct (English page): `25 000.00`, `1 234.56`, `0.5`

✗ Wrong: `25,000.00` (comma thousands — US-style, not Tripletex)

✗ Wrong: `25000,00` (no thousands separator on a four-digit-plus value)

---

## Rule: Currency formatting

**Description**

Tripletex displays currency values in three context-driven patterns. The pattern is chosen by *what surface the value sits on* — not by the value itself. Decimal places default to **two**, even in narrow tables. The currency code (NOK / SEK / USD) appears or is omitted depending on whether the surface mixes currencies.


**How to Apply**

| Context | Format (NO) | Format (EN) | When |
|---|---|---|---|
| **Single-currency page** | `25 000,00` | `25 000.00` | If the page only displays values in Norwegian kroner (the most common case), the currency code is **omitted**. |
| **Multi-currency page** | `NOK 25 000,00` / `EUR 5 000,00` | `NOK 25 000.00` / `EUR 5 000.00` | If the page displays values in more than one currency, a **currency indicator appears as a prefix before each value**. |
| **No-decimal case** (sentence / dashboard) | `NOK 25 000` | `NOK 25 000` | When the currency appears inside running text or on a dashboard summary card, decimals may be omitted to improve readability. |
| **In-text price with kr suffix** | `49 kr per month` | (use `NOK 49 per month` or `49 NOK per month`) | When a price appears as part of a sentence, the `kr` suffix is the in-text form. See Rule "Percentages and units" for the underlying `kr` unit. |

Decimal places are **two by default** — even in narrow tables — except for the no-decimal case above. Don't strip decimals to save width; let the cell wrap-protect the value (per Rule "Formatted numbers stay on one line") and keep the decimals.

**Higher-precision exceptions** apply to specific value types — unit prices, exchange rates, weighed quantities — that need 3 or more decimals to preserve meaningful detail. See Rule "Decimal precision by value type" for the full breakdown.

**Violations**

- Currency code shown on a single-currency page (`NOK 25 000,00` when every value on the page is NOK) — warning (redundant noise; omit the code)
- Currency code missing on a multi-currency page (`25 000,00` next to `5 000,00` with no way to tell which is NOK vs EUR) — error
- Currency code appearing after the value (`25 000,00 NOK`) — error (always prefix, per Figma)
- Currency value rendered with one decimal or no decimals in a context that should show two (table, detail view, form value, anywhere except the documented sentence/dashboard no-decimal case) — warning
- Mixed decimal counts in the same column or list (some `25 000,00`, some `25 000`) — error

**Examples**

✓ Correct (single-currency NO page, invoice list): `25 000,00`, `1 250,50`, `0,00`

✓ Correct (multi-currency page): `NOK 25 000,00` next to `EUR 5 000,00`, both with the code as prefix.

✓ Correct (dashboard summary card): "Total revenue this quarter: **NOK 25 000**" — decimals dropped because it's a summary in running context.

✓ Correct (in-text price): "This plan costs 49 kr per month."

✗ Wrong: `NOK 25 000,00` repeated across an entire NO-only invoicing page — the code is noise where every line is in NOK.

✗ Wrong: `25 000,00` next to `5 000,00` on a page that mixes NOK and EUR — the user can't tell what each value is.

---

## Rule: Decimal precision by value type

**Description**

The default decimal precision in Tripletex is **two decimals**, used for booked currency amounts and most financial line items (per Rule "Currency formatting"). Several specific value types need higher precision because the value carries meaningful detail beyond two decimals — typically because the value will be multiplied by a quantity, summed across many rows, or used in a calculation where rounding errors compound. This rule defines per-context precision requirements so contributors don't strip precision to save column width or apply two-decimal rendering to a value that needs more.


**How to Apply**

| Value type | Precision | Rationale |
|---|---|---|
| **Booked currency amount** (invoice line, ledger entry, salary) | 2 decimals | Standard accounting precision. Matches external documents and tax submissions. |
| **Currency total / dashboard summary** | 0 or 2 decimals | 0 in running text or summary cards (`NOK 25 000`); 2 in any context where the value will be summed or compared against booked amounts. |
| **Unit price** (stykkpris, hourly rate, price-per-kg) | 3-4 decimals | Unit prices are multiplied by quantity. A two-decimal rate (`0,75 kr/h`) loses fractional accuracy that compounds across rows. The canonical form is `0,7500 kr/h` (4 decimals) or `0,750 kr/h` (3 decimals). |
| **Exchange rate** | 4-6 decimals | Exchange rates carry significant precision (`NOK/USD 10,4523` or `10,452345`). Rounding to 2 decimals would lose meaningful value for any non-trivial conversion. |
| **Weighed quantity** | 3+ decimals | Weight or volume measured in kg or l often has 3 or more decimals (`1,250 kg`, `0,750 l`). Don't round to 2 unless the source data is itself two-decimal precision. |
| **Percentage** | 0-2 decimals depending on context | VAT rates and discount percentages are typically integer (`25 %`, `15 %`, `10 %`); allocation percentages may need 2 (`33,33 %`). Don't show more than 2 decimals on a percentage unless specifically required. |

**Don't strip precision to save column width.** If a unit price needs 4 decimals, the column needs to be wide enough — applying `white-space: nowrap` (Rule "Formatted numbers stay on one line") keeps the value intact, and the column auto-sizes. Stripping precision because a column is "too narrow" is a column-design problem, not a value-precision problem.

**Don't add precision the source data doesn't have.** If a customer's hourly rate is stored as `0,75`, render it as `0,75` (or `0,7500` if a fixed precision is required for the column) — but be careful not to fabricate trailing zeros that misrepresent the source precision in contexts where the user might read precision as accuracy.

**Column-wide consistency.** Every value in a single column uses the same precision. A unit-price column showing some rows at 2 decimals and others at 4 is a sorting and reading hazard.

**Violations**

- Unit price rendered with 2 decimals when 3-4 is the canonical precision (`0,75 kr/h` in a unit-price column where every other row has 4 decimals) — error
- Exchange rate rendered with 2 decimals (`10,45` instead of `10,4523`) — error (the rate's actual precision is lost)
- Weighed quantity rendered with 0 decimals when the source has more (`1 kg` for a value stored as `1,250`) — warning
- Percentage rendered with 4+ decimals when 0-2 is sufficient (`33,3333 %` for an integer one-third allocation) — warning (excessive precision is its own form of false precision)
- A single column rendering some rows at 2 decimals and others at 4 decimals — error (column-wide consistency required)

**Examples**

✓ Correct (invoice line, NO): `1 250,00 kr` — 2 decimals, booked amount.

✓ Correct (unit-price column, NO): `0,7500 kr/h` — 4 decimals, column convention.

✓ Correct (exchange-rate display, NO): `NOK/USD 10,4523` — 4 decimals, rate precision preserved.

✓ Correct (VAT rate, NO): `25 %` — 0 decimals, integer rate.

✗ Wrong: A unit-price column showing `0,75`, `0,7500`, `0,750` in different rows — column-wide consistency lost; user can't sort or compare reliably.

✗ Wrong: An exchange rate rendered as `10,45` in a currency-conversion summary — implies precision the value doesn't actually have when used in real conversions.

---

## Rule: Negative number conventions

**Description**

Negative numbers in Tripletex appear in two distinct forms depending on context. **In running app UI** (live ledgers, refund amounts, debit/credit entries, dashboard summaries), use a **minus prefix**: `-1 234,50`. **In printed financial statements and statutory exports** (resultatregnskap, balanse, kontantstrømoppstilling, PDF year-end reports), use **accounting parentheses**: `(1 234,50)`. The two forms come from different traditions — minus prefix is the digital-UI convention; parentheses are the accounting / IFRS / GAAP / Norwegian Regnskapsloven printed-statement convention. **Never combine the two**: `(-1 234,50)` is always wrong.

The rule applies regardless of locale — accounting parentheses are shared between Norwegian Regnskapsloven / NRS and IFRS / GAAP, so they work on both NO and EN financial-statement surfaces.


**How to Apply**

| Context | Format | Example |
|---|---|---|
| In-app live ledgers, transaction lists, refund amounts, dashboard summaries | Minus prefix | `-1 234,50` |
| Debit/credit columns where the sign indicates direction | Minus prefix on the signed column, **or** split into separate Debit / Credit columns where each value is positive and the column carries the sign meaning | `-1 234,50` (signed) **or** `1 234,50` in the Debit column with the Credit column blank (split) |
| Printed financial statements (PDF resultatregnskap, balanse, kontantstrømoppstilling) | Accounting parentheses, **without** minus sign | `(1 234,50)` |
| Statutory exports (PDF year-end reports, government submissions) | Accounting parentheses | `(1 234,50)` |

**The split-column variant.** Some accounting tables split the sign into separate Debit / Credit columns rather than rendering a sign on the value itself. Both columns are positive; the column the value appears in carries the sign meaning. Allowed and preferred when the account context calls for it (general ledger displays, T-account views).

**Never combine.** Don't render a negative number as `(-1 234,50)` — pick one convention. Parentheses **without** minus sign, or minus sign **without** parentheses.

**Document-wide consistency.** A single financial statement uses one negative-number convention end-to-end. Don't render some negative values as `-1 234,50` and others as `(1 234,50)` on the same page.

**Visual reinforcement.** In-app, negative currency amounts often appear in red (`--text-error` or equivalent) as a secondary cue. Colour is reinforcement, not the only signal — the minus prefix or parentheses carry the meaning. Per WCAG 1.4.1 (Use of Color), the sign convention must remain readable without colour.

**Violations**

- Negative number rendered as `(-1 234,50)` (parentheses + minus combined) — error
- A printed financial statement (resultatregnskap, balanse) using minus prefix instead of accounting parentheses — error (Norwegian accounting convention requires parentheses for printed statements)
- An in-app ledger using accounting parentheses instead of minus prefix — warning (technically valid in some accounting traditions but breaks digital-UI convention; minus prefix is the expected form)
- A single document mixing minus-prefix and parenthesis conventions for different rows — error
- A debit/credit table where one column has the sign on values (`-1 234,50`) and the other doesn't — error (pick split-column or signed, not both)
- Negative value relying only on red colour with no minus sign or parentheses — error (WCAG 1.4.1 violation; colour alone is not sufficient)

**Examples**

✓ Correct (in-app refund list, NO): `-1 250,00 kr`, displayed in red as a visual reinforcement on top of the minus sign.

✓ Correct (PDF resultatregnskap, NO expense line): `(1 250,00)` — parentheses, no minus, no red.

✓ Correct (split-column general ledger, NO): Debit column shows `1 250,00`, Credit column shows blank; the direction is in which column the value sits.

✗ Wrong (in-app): `(-1 250,00 kr)` — combining parentheses and minus.

✗ Wrong (PDF year-end report): `-1 250,00` — minus prefix is for in-app, not printed statements.

✗ Wrong: A refund amount rendered in red as `1 250,00 kr` with no minus sign — colour alone can't carry the negative meaning (WCAG 1.4.1).

---

## Rule: Percentages and units

**Description**

Numeric values that carry a unit (`kg`, `l`, `stk`, `%`, `kr`, etc.) sit next to the unit with a **single space between number and unit** — except for percentage in English, which has *no* space (`50%`). The space pairing is a Norwegian-typography rule that Tripletex follows on Norwegian surfaces; the English surface follows the EN convention of no space before `%`. Norwegian uses a non-breaking space before the unit so the number and unit cannot wrap apart (already covered by Rule "Formatted numbers stay on one line").


**How to Apply**

| Type | NO | EN | Notes |
|---|---|---|---|
| Items | `2 stk` | `2 each` | Space between the number and the unit. |
| Weight | `120 kg` | `120 kg` | Space. |
| Volume | `8 l` | `8 l` | Space. |
| Percent | `50 %` | `50%` | NO has a space before `%`; EN does **not**. |
| Krones (suffix form, in text) | `4,00 kr` | `NOK 4,00` | NO uses `kr` suffix; EN uses `NOK` prefix. Decimal follows the locale rule (Rule "Norwegian locale defaults"). |
| Recurring cost (shorthand) | `99/mnd` | `99,- per month` / `99/month` | Shorthand for `99 kr per month`. EN `99/month` is not wrong but is unusual. |

For prices that appear as part of a sentence (e.g. *"This plan costs 49 kr per month"*), prefer the suffix form in NO (`49 kr`) per the Currency rule.

**Violations**

- Percent in NO without a space before `%` (`50%` on a NO page) — warning (Figma rule, but a soft violation since some legacy surfaces have it the other way)
- Percent in EN with a space before `%` (`50 %` on an EN page) — warning
- Unit value without a space between number and unit (`2stk`, `120kg`, `8l`) — error
- Currency suffix on a NO page rendered without the space (`4,00kr`) — error
- Krones written as `kr` prefix in NO running text (`kr 4,00 per month`) instead of suffix (`4,00 kr per month`) — warning (the multi-currency-page case is different — see Rule "Currency formatting")

**Examples**

✓ Correct: `2 stk`, `120 kg`, `8 l`, `50 %` (NO), `50%` (EN), `4,00 kr` (NO sentence), `NOK 4,00` (EN sentence).

✓ Correct (in-text NO): "Du har **49 kr** igjen på saldoen din."

✗ Wrong: `50%` on a NO page where every other percent has a space.

✗ Wrong: `2stk` in a table cell — Norwegian typography requires the space.

---

## Rule: Number abbreviations

**Description**

For very large numbers in **data visualisations only** (chart axes, sparkline labels, summary tiles), use the abbreviated short forms below. Outside data visualisations — in tables, lists, detail views, forms, invoices, anywhere else — write the full number, even if it's seven digits long. The abbreviations save horizontal space where a chart axis cannot widen; they cost precision, which is unacceptable in any context where the exact value is what the user needs.

**When to Use**

In data visualisations where the rendered width is constrained and an exact number wouldn't fit. Never in tables. Never in detail views. Never in invoices or financial documents.

**How to Apply**

| Magnitude | NO | EN |
|---|---|---|
| Thousand (1 000) | `1 k` | `1K` |
| Million (1 000 000) | `1 mill.` | `1M` |
| Billion (1 000 000 000) | `1 mrd.` | `1B` |

Norwegian uses a space between the digit and the abbreviation (`1 k`, `1 mill.`, `1 mrd.`); English does not (`1K`, `1M`, `1B`). Norwegian abbreviations have a trailing period for `mill.` and `mrd.` but not for `k`.

When chart axis labels render at the locale's compact format, the **surrounding component must accommodate the abbreviation's width** — including up to the longest Norwegian form, `14,0 mill.` (8 characters plus a space). Components that under-size their axis-label area (e.g. defaulting to 60px on Rubik 14px) truncate the label and break the rule. The compact format itself is documented here; the component-side accommodation rule is `charts.md`'s problem *(not yet documented — see `TODO.md`)*.

**Violations**

- Abbreviated number in a table (`1,2 mill.` instead of `1 234 567`) — error
- Abbreviated number in a detail view, invoice, or financial document — error
- Norwegian abbreviation without space (`1k`, `1mill.`) — error
- English abbreviation with space (`1 K`, `1 M`) — error
- `mill.` or `mrd.` written without the trailing period in NO — warning
- Chart axis using an abbreviation but the surrounding component truncates it — warning (the abbreviation is correct; the component sizing is the bug — see `charts.md`)

**Examples**

✓ Correct (NO chart axis): `1 k`, `14,0 mill.`, `1,2 mrd.`

✓ Correct (EN chart axis): `1K`, `14.0M`, `1.2B`

✗ Wrong: A salary table column showing `15 mill.` instead of `15 000 000` — exact value matters in a table.

✗ Wrong: A summary tile showing `1mill.` (missing space, missing period in NO).

---

## Rule: Time formats

**Description**

Time is rendered in **24-hour Norwegian convention** with a **colon separator** between hours and minutes (and optionally seconds). The colon is what visually distinguishes a time from a date (which uses period or hyphen separators) at a glance — never substitute another separator for the colon. Count-down values use a different pattern (`2 t 38 m`) — that's a duration, not a time-of-day, and the units are explicit because the user reads them as "two hours, thirty-eight minutes" rather than as a clock value.


**How to Apply**

| Type | Format | NO | EN | Notes |
|---|---|---|---|---|
| Time | `hh:mm` | `11:11` | `11:11` | 24-hour clock. Colon separator. |
| Time with seconds | `hh:mm:ss` | `11:11:05` | `11:11` (EN omits seconds by default) | Use when sub-minute precision matters. |
| Duration (hours+minutes) | `Nt Mm` | `2 t 38 m` | `2 t 38 m` | "t" for timer/hours, "m" for minutter/minutes. Same in both locales. |
| Duration (with seconds) | `Nt Mm Ss` | `2 t 38 m 42 s` | `2 t 38 m 42 s` | Add `Ss` when sub-minute precision matters. |
| Duration (days) | `N dager` (NO) / `N days` (EN) | `3 dager` | `3 days` | When the magnitude is days, use the word form. |

**Tabular numbers (`tabular-nums`)** must be applied to any time or duration value that updates in real time (a count-down clock, a stopwatch, a live "saved X seconds ago" indicator). Without `tabular-nums`, each digit takes its proportional width and the value shifts horizontally as numbers change — `1:11` to `1:12` to `1:13` causes the number to dance. Tabular numbers fix-width every digit so the value updates in place.

**Violations**

- Time using a separator other than colon (`11.11`, `11-11`) — error
- Time using 12-hour AM/PM (`11:11 AM`) — error (Tripletex is 24-hour everywhere)
- Duration using a colon instead of unit letters (`2:38` to mean two hours thirty-eight minutes) — error (the colon is reserved for time-of-day; durations use unit letters)
- Auto-updating time or duration rendered without `tabular-nums` such that the value shifts horizontally on each update — warning
- Norwegian duration using English unit abbreviations (`2 h 38 min` instead of `2 t 38 m`) — warning

**Examples**

✓ Correct: A delivery timestamp on an invoice — `15.05.2024 09:30` (date and time separated by space, both in canonical format).

✓ Correct: A countdown to a scheduled report — `2 t 38 m 42 s` rendered with `tabular-nums` so the seconds digit updates in place.

✗ Wrong: A live "session expires in" indicator showing `1:59:33` that visibly shifts as the digits tick down — needs `tabular-nums`.

✗ Wrong: A meeting time written as `9.30 AM` — both the separator and the AM are off.

---

## Rule: Date formats

**Description**

Tripletex is moving toward modern, common date formats that align with user expectations and Norwegian standards. The standard date format in Tripletex is **`dd.mm.yyyy`** for absolute numeric dates; textual dates (with the month spelled out) are preferred when the date sits inside a sentence. The legacy **ISO 8601 (`yyyy-mm-dd`) format is technically correct but is not commonly used in Norwegian user interfaces**, and mixing ISO 8601 dates with `dd.mm.yyyy` in the same workflow forces users to mentally convert dates — increasing cognitive load and the risk of errors. ISO 8601 is therefore restricted to legacy JSP tables; it must not be introduced in new user-facing UI.

This rule covers numeric and textual absolute dates. **Relative dates** (`i dag`, `i går`, `for 2 dager siden`) are a separate concern — see the "Relative dates" rule. **Date ranges** are also separate — see the "Date ranges" rule.


**How to Apply — numeric formats**

| Type | Format | NO example | EN example | Use it in |
|---|---|---|---|---|
| **Numeric Date Full** | `dd.mm.yyyy` | `20.05.2025` | `20.05.2025` | The **standard** format. Invoices, financial documents, forms and inputs, detail views, filters, summaries — any user-facing content where dates are read or compared. |
| **Numeric Date Short** | `dd.mm.yy` | `03.05.25` | `03.05.25` | Alternative to full dates, generally used in narrow tables where the column width can't fit `dd.mm.yyyy`. |
| **ISO 8601** | `yyyy-mm-dd` | `2024-05-17` | `2024-05-17` | **Tables across the product** (including tables on new pages — see the next rule for the consistency rationale), and any **machine-readable surface** (CSV exports, URL parameters, log lines, file names, API payloads). **Not** for non-table user-facing UI like forms, summaries, detail views, or running text. |

The choice between `dd.mm.yyyy` and `yyyy-mm-dd` — and the current product-wide reality that all user-facing surfaces render ISO today regardless of context — is governed by Rule "Date format migration state" immediately below. The format definitions here only describe what each format *looks like*; the migration state and where teams have flexibility live in the next rule.

**How to Apply — textual formats**

| Type | NO example | EN example | Notes |
|---|---|---|---|
| **Textual Date Full** | `3. januar 2025` | `3 January 2025` | Preferred over numeric when the date is read within a sentence. |
| **Textual Date Full (no year)** | `3. januar` | `3 January` | When the year is clear from context. |
| **Textual Year + Month** | `januar 2025` | `January 2025` | When the day is irrelevant. |
| **Textual Date Short (full year)** | `16. jan. 2025` | `16 Jan. 2025` | Three-letter month abbreviation. |
| **Textual Date Short (short year)** | `16. jan. 25` | `16 Jan. '25` | Two-digit year for narrow contexts. |
| **Textual Date Short (no year)** | `16. jan.` | `16 Jan` | When year is irrelevant. |
| **Textual Date with Day** | `torsdag 16. januar 2025` | `Thursday 16 January 2025` | Full day name. |
| **Textual Date with Day (short)** | `to. 16. jan. 2025` | `Thurs./Th. 16 Jan. 2025` | Two-letter day abbreviation in NO. |
| **Textual Date Today** | `i dag, 16. januar 2025` / `i dag, 16. jan.` | `today, 16 January 2025` / `today, 16 Jan 2025` | If the date is today and the date must still be shown, use `today` (`i dag`) instead of the day name. |

Spelling and capitalisation rules:

- **Month abbreviations** are three letters in both locales: `jan.` / `Jan.`, `feb.` / `Feb.`, etc.
- **NO has a period after the abbreviated month**; **EN does not** in the short form (`Jan`, `Feb` — though the older `Jan.` form is also seen and acceptable).
- **EN capitalises month names** (`January`, `Jan.`); **NO does not** (`januar`, `jan.`).
- **Day abbreviations** are two letters in both locales: `to.` (torsdag), `Th.` (Thursday).

**Violations**

- `dd.mm.yyyy` introduced into a table (any table, anywhere in the product) — error (consistency override; see Rule "Date format migration state")
- A workflow that mixes `dd.mm.yyyy` and `yyyy-mm-dd` for the same date across steps — error (see Rule "Date format migration state")
- Date inside a sentence rendered numerically when a textual form would have read more naturally — note
- Month abbreviation that's not three letters (e.g. `janu`, `Ja`) — error
- NO month abbreviation without the trailing period (`jan ` instead of `jan.`) — warning
- EN month name not capitalised (`january`) — error
- Two-letter day abbreviation that doesn't match the canonical (e.g. `tor.` for torsdag instead of `to.`) — warning

**Examples**

✓ Correct (invoice header, NO): `Faktura: 12345 — 17.05.2024`

✓ Correct (sentence, NO): "Vi mottok bestillingen din **3. januar 2025**."

✓ Correct (narrow table column header, NO): `16. jan. 25`, `17. jan. 25`, `18. jan. 25`

✓ Correct (today reference, NO): "Du har 2 oppgaver i dag, 16. januar 2025."

✗ Wrong (new table on new dashboard): A new dashboard's "Created" column renders dates as `15.05.2024` — tables stay on `yyyy-mm-dd` across the product, regardless of how new the page is. See Rule "Date format migration state".

✗ Wrong (EN): `3 january 2025` — month not capitalised.

---

## Rule: Date format migration state

**Description**

Tripletex's product currently renders dates as **`yyyy-mm-dd` (ISO 8601) everywhere** — tables, forms, summaries, detail views, exports. This is the customer-facing reality, documented by the [help-centre article *"Hvordan endrer jeg format på dato?"*](https://hjelp.tripletex.no/hc/no/articles/19824603945489) ("Datoformat i Tripletex er ÅÅÅÅ-MM-DD ... vi støtter kun formatet ÅÅÅÅ-MM-DD") and confirmed by the Atlas date-component implementation: `DateField`, `<Input type="date">`, `DateSelector`, and `formatDate` all hardcode ISO output, normalising any user-typed value to `yyyy-mm-dd` on blur.

The **long-term design direction is `dd.mm.yyyy`** (the Norwegian convention) for non-table user-facing surfaces — forms, summaries, detail views, running text. Tables stay on `yyyy-mm-dd` even post-migration for sortability and cross-table comparison. The migration is acknowledged-but-pending: the `@tlx/intl/formatDate` deprecation comment ("Until we have a company-wide strategy for replacing ISO 8601 with localized date format, use `formatISODate` instead") is the internal marker that localised render is unfinished work.

This rule captures the current pattern as the working default, names the aspiration, and clarifies where teams have flexibility to adopt `dd.mm.yyyy` ahead of the Atlas migration versus where they must hold for consistency.


**How to Apply**

**Default — use `yyyy-mm-dd` via Atlas date components.** Every Atlas date primitive produces ISO output. Using `DateField` / `<Input type="date">` / `DateSelector` gives the team this format automatically. The components accept multiple input forms (`15.05.2024`, `15/05/2024`, `150524`, `2024-05-15`) and normalise to ISO on blur — users can type Norwegian, but the rendered value is ISO. This is the current product-wide pattern and the canonical input behaviour. Don't override it.

**Aspiration — `dd.mm.yyyy` for non-table user-facing surfaces, eventually.** When Atlas ships a localised render mode for the date components, non-table surfaces will migrate to `dd.mm.yyyy`. Tables stay on ISO regardless. The migration trigger is Atlas-side: there is nothing for product teams to do today to advance the migration except (a) help with the Atlas localisation work if they can, or (b) not ship rendering that would have to be undone when the migration lands.

**Teams may use `dd.mm.yyyy` today, in genuinely isolated greenfield surfaces.** If a team is building a new, isolated surface that does *not* render through Atlas date primitives, does *not* appear in a workflow alongside legacy `yyyy-mm-dd` surfaces, and does *not* invite cross-comparison with other Tripletex dates, rendering `dd.mm.yyyy` is allowed. The friction with banks, government portals, and external documents is real — for a genuinely standalone feature, the Norwegian-convention format may serve users better than ISO. **The isolated case is rarer than it looks**: most "new" features in Tripletex compose with existing data and surfaces, and that composition tends to surface the format mismatch. Review carefully before assuming a surface qualifies.

**Sections where consistency requires holding to `yyyy-mm-dd`:**

- **Tables, always.** Tables across the product use ISO. A new table on a new page rendering `dd.mm.yyyy` next to existing tables in ISO defeats sortability and forces the user to mentally convert across rows or pages. Tables don't migrate.
- **Surfaces rendered through Atlas date primitives.** The Atlas components hardcode ISO; rendering `dd.mm.yyyy` from one of them would require a bypass that breaks parity with every other Atlas-using surface.
- **Workflows that include legacy `yyyy-mm-dd` surfaces.** If a user follows the same date through form → submit → confirmation → email/PDF, every step in the chain uses the same format. If any step is on legacy ISO, the chain holds.
- **Machine-readable surfaces** — CSV exports, URL parameters, log lines, file names, API payloads. ISO 8601 unconditionally; these don't have a user-facing locale, and ISO is locale-independent and sortable.

**Migration approach for legacy pages.** When updating a legacy page that currently uses `yyyy-mm-dd` everywhere:

1. **Full migration is preferred** when feasible — migrate the entire page in one change.
2. **Partial migration is forbidden.** If only part of the page can migrate to `dd.mm.yyyy` (e.g. forms can but the table can't because of legacy code), leave the entire page on `yyyy-mm-dd` until the rest can also migrate. Half-migration creates exactly the mixed-format workflow the rule is trying to prevent.
3. **Document intent.** When a page is held back at `yyyy-mm-dd` because a partial migration would violate this rule, leave a code comment so future contributors know it's an intentional hold, not an oversight.

**Violations**

- A new table on a new page using `dd.mm.yyyy` instead of `yyyy-mm-dd` — error (tables stay on ISO across the product regardless of page age)
- An Atlas date input forced into `dd.mm.yyyy` display via a workaround that bypasses the component's normalise-on-blur — error (the Atlas components are the canonical input behaviour; don't override)
- A workflow that mixes `dd.mm.yyyy` and `yyyy-mm-dd` for the same date as the user follows it through the flow — error
- A surface rendering `dd.mm.yyyy` in a workflow with existing legacy `yyyy-mm-dd` surfaces — error
- An isolated greenfield feature shipping `dd.mm.yyyy` without documenting the isolation rationale in code review — note (allowed by the flexibility clause, but worth a deliberate check that the surface really is isolated)
- A machine-readable surface (CSV, URL param, log line) using `dd.mm.yyyy` — warning (ISO is locale-independent and sortable; `dd.mm.yyyy` complicates downstream parsing)
- Half-migrating a legacy page (forms moved to `dd.mm.yyyy`, tables left at `yyyy-mm-dd` mid-flight) — error

**Examples**

✓ Correct (default path): A new "Order date" form filter renders dates as `2024-05-15`. The user types `15.05`, the Atlas date input normalises to ISO on blur. Consistent with every other Tripletex form.

✓ Correct (legacy detail view): A customer-overview page on legacy code shows the "Sist endret" timestamp as `2024-05-15 14:32`. Stays on ISO until the page migrates.

✓ Correct (isolated greenfield): A new HR-side "Birthday" field on a standalone benefits-management feature renders `15.05.2024`. The team documented in code review that the feature has no other Tripletex date comparison anywhere in its workflow. Genuinely isolated; rule allows it.

✓ Correct (new table in workflow with legacy tables): An invoice list on a new dashboard renders the "Created" column as `2024-05-15`. The table joins the rest of the Tripletex invoice ecosystem; ISO is the right choice.

✗ Wrong: A new table on a new dashboard renders the "Created" column as `15.05.2024` — tables stay on `yyyy-mm-dd` across the product, regardless of how new the page is.

✗ Wrong: A team bypasses Atlas's `DateField` to render the input value as `15.05.2024` in their custom form — the bypass renders ahead of the migration and creates a mixed-format experience the moment the user navigates to any other Tripletex surface.

✗ Wrong: A workflow where a new form shows `15.05.2024` and the confirmation table on the next page shows `2024-05-15` for the same submitted date. Two formats, one workflow, one date — the failure mode this rule exists to prevent.

✗ Wrong: A legacy customer page where forms have been migrated to `dd.mm.yyyy` but the contact-history table on the same page is still on `yyyy-mm-dd`. Either migrate the table too or hold the form at ISO until the migration lands fully.

---

## Rule: Relative dates

**Description**

Relative dates (`i dag`, `i går`, `for 2 dager siden`) adapt to how long ago an event occurred and help users understand recency at a glance. They are appropriate where the user is browsing recent activity and the exact date matters less than "how new is this". They are **inappropriate** where precision matters, where dates are sorted or filtered, or where the user needs to compare dates across rows. **If you are unsure, do not use relative dates** — the absolute date is always safe; a wrong relative date is confusing.

**When to Use**

Use relative dates in:

- In-app chat
- Comments
- Activity feeds and event logs

Do **not** use relative dates in:

- Invoices
- Legal or financial records
- Filters or sortable date columns
- Data tables
- If you are unsure, don't use relative dates

**How to Apply**

The format for the relative-date *value* depends on how long ago the event occurred:

| Time since event | Format | Example |
|---|---|---|
| Less than 24 hours | `hh:mm` (24-hour clock) | `18:11` |
| ≥ 24 hours and less than 1 year | `dd.mmm.` | `17. aug.` |
| ≥ 1 year | `dd.mmm.yy` | `17. aug. 25` |

Relative dates should always be:

- **Localised** to the user's surface language (Norwegian / English).
- **Consistent within the same context** — don't mix relative `i dag` with absolute `16. januar 2025` in the same activity feed row.

**Grouping multiple relative dates.** When a list of events is grouped by day, label the group with a date label that combines a relative-or-absolute prefix with the day's date:

| Group |
|---|
| `i dag, 11. mars 2025` |
| `i går, 10. mars 2025` |
| `03. mars 2025` |
| `tidligere år, 03. mars 2025` |

Today and yesterday get a relative prefix (`i dag`, `i går`). Days within the current year use the absolute date alone (`03. mars 2025`). Days in earlier years are prefixed with `tidligere år` (literally "earlier year") plus the absolute date.

**Violations**

- Relative date used in an invoice, legal record, or financial document — error
- Relative date used in a filter or sortable date column — error (sorting by a localised relative string is broken — sorts by alphabet, not by chronology)
- Relative date used in a data table — error (per the Figma rule)
- Relative-date format mixed with absolute-date format inside the same context (e.g. one row says `i dag`, the next says `16. januar 2025`) — warning
- Group label that omits the absolute date and shows only the relative prefix (`i dag` without `11. mars 2025`) — warning (the absolute date is what makes the group label unambiguous when revisited later)

**Examples**

✓ Correct (in-app chat): A message timestamp shows `14:32` because the message was sent earlier today.

✓ Correct (activity feed): A grouping `i dag, 11. mars 2025` heads the day's entries, each entry showing only `14:32`, `09:15`, `08:00`.

✗ Wrong: An invoice filter offers "Sent in the last week" as a sortable column showing `for 2 dager siden`, `for 5 dager siden`, etc. — sortable date columns must use absolute dates.

✗ Wrong: A comment feed mixes `i går` on one comment and `10. mars 2025` on another, both from the same day — inconsistent within context.

---

## Rule: Date ranges

**Description**

Date ranges have their own canonical forms — numeric short / numeric full / multi-month / textual with day / named relative ranges (`Siste 7 dager`) / quarter labels — each with NO and EN variants. The dash between the two dates is an en-dash or hyphen; whitespace around it is allowed (some Figma examples use `-` flush, some use ` – ` with spaces — both are acceptable provided the line-wrapping rule from Rule "Formatted numbers stay on one line" holds).


**How to Apply**

| Type | NO example | EN example | Notes |
|---|---|---|---|
| Numeric Date Range Full | `01.11.2024-31.12.2024` | `01.11.2024-31.12.2024` | Default for absolute date ranges. |
| Numeric Date Range Short | `01.11.24-31.12.24` | `01.11.24-31.12.24` | Narrow tables. |
| Multiple Months (same year) | `nov.-des. 2024` | `Nov.-Dec. 2024` | When start and end are different months in the same year, share the year. |
| Multiple Months (different years) | `nov. 2024-jan. 2025` | `Nov. 2024-Jan. 2025` | When start and end straddle years, repeat the year on each side. |
| Multiple Months (short year, different years) | `nov. 24-jan. 25` | `Nov. '24-Jan. '25` | Narrow contexts. EN uses an apostrophe before the two-digit year. |
| Textual with Day (full year) | `01. nov. 2024-31. des. 2024` | `01. Nov. 2024-31. Dec. 2024` | Long form for documents where each date is read individually. |
| Textual with Day (short year) | `01. nov. 24-07. apr. 25` | `01. Nov. '24-07. Apr. '25` | Narrow contexts. |

**Named relative ranges** — fixed-period shortcuts often used in period selectors:

| NO | EN | Meaning |
|---|---|---|
| `Siste 7 dager` | `Last 7 days` | Rolling 7-day window ending today. |
| `Neste 7 dager` | `Next 7 days` | Rolling 7-day window starting today. |
| `Forrige år` | `Last year` | The previous calendar year. |

**Range until today** — the "year-to-date / month-to-date" pattern:

| NO | EN | Meaning |
|---|---|---|
| `Hittil i år` | `So far this year` | From 01. januar of the current year up to and including today. |
| `Hittil i januar` | `So far in January` | From 01. of the current month up to and including today (substitute the current month name). |

**Quarter labels** — calendar quarters, used in financial reporting:

| Type | NO | EN | Notes |
|---|---|---|---|
| Quarter Full | `1. kvartal 2025` | `First quarter 2025` | Full form. |
| Quarter Short | `1. kv. 2025` | `Q1 2025` | Compact form for narrow contexts. |
| Term (alternative) | `1. termin 2025` | `First period 2025` | "Termin" is the Norwegian accounting term for a tax/reporting period. |

Quarter boundaries: **Q1 (jan. - mar.), Q2 (apr. - jun.), Q3 (jul. - sep.), Q4 (okt. - des.)**. The boundaries are calendar quarters; Tripletex doesn't currently support fiscal quarters that diverge from calendar quarters.

**Wrapping.** Per the rule "Formatted numbers stay on one line", date ranges may wrap *between* the two dates (with vertical alignment), never *within* a single date. Stacking the two dates one above the other with the dash leading the second line is the canonical wrap pattern.

**Violations**

- Date range with the start date wrapping mid-value (e.g. `01.11.2024-31.12` on one line, `.2024` on the next) — error
- Multi-year range with the year shared instead of repeated (`nov.-jan. 2024` for a range that spans 2024 to 2025) — error
- Quarter label that uses an arbitrary boundary instead of the canonical Q1-Q4 calendar quarters — error
- Named range with the wrong direction (`Siste 7 dager` rendered as "Next 7 days") — error
- Compact quarter form on a non-narrow context where the full form would have fit (`1. kv. 2025` in a wide column) — note

**Examples**

✓ Correct (invoice period filter, NO): `01.11.2024-31.12.2024`

✓ Correct (multi-month overview, NO): `nov.-des. 2024`

✓ Correct (period selector preset, NO): `Hittil i år`

✓ Correct (quarterly report header, NO): `1. kvartal 2025` rendered in a heading, `1. kv. 2025` in the corresponding tab label.

✗ Wrong: `nov.-jan. 2024` for a range that runs November 2024 → January 2025 — needs the year on each side.

✗ Wrong: `Last 7 weeks` invented as a new named range — Atlas only documents `Last 7 days`, `Next 7 days`, `Last year`, `Hittil i år`, `Hittil i [month]`.

---

## Rule: Identifier formats

**Description**

Identifiers (bank accounts, personal ID numbers, organisasjonsnummer, MVA-nummer, KID-nummer, phone numbers, credit card numbers, IBAN, SWIFT/BIC, postnummer + poststed) are **structured strings, not numeric values** — the grouping (or deliberate lack of grouping) is what makes them readable. Each identifier type has a canonical format that this rule documents. The format is the same in Norwegian and English surfaces; only display contexts may vary (e.g. bank accounts use a period separator in tables; personal-number portion of fødselsnummer is masked for non-essential display).

Although these patterns sit in the Number Formats foundation, conceptually they're closer to *identifier formatting* than to *numeric-value formatting* — they don't have decimals, locales don't change them, and arithmetic operations don't apply. The grouping convention is structural, picked to match how the identifier is spoken or hand-written, or to satisfy a check-digit algorithm. Tracked as a possible future split into `foundations/identifiers.md` if more identifier types accumulate.


**How to Apply**

| Identifier | Format (NO/EN identical) | Pattern | Notes |
|---|---|---|---|
| **Bank accounts** (inline) | `1030 17 38765` | 3 groups (4-2-5), space-separated | Default rendering everywhere except tables. |
| **Bank accounts** (in tables) | `1030.17.38765` | 3 groups (4-2-5), period-separated | When displaying account numbers in tables, use a period (.) for compactness. |
| **Personal ID number** (fødselsnummer) | `180690 12345` | 2 groups (6-5), space-separated | Date-of-birth (6) + personal number (5). **Mask the personal-number portion (last 5) for non-essential display** — render as `180690 *****` — per Datatilsynet's sensitivity guidance. Show full only when functionally essential (user verifying their own record, payroll processing, statutory submissions). |
| **Organisasjonsnummer** | `123 456 789` | 3 groups (3-3-3), space-separated | 9-digit Norwegian business ID. Brønnøysund convention. Used pervasively in Tripletex — customer pages, supplier pages, tax submissions, A-melding, MVA-melding. |
| **MVA-nummer** | `123 456 789 MVA` (domestic) / `NO 123 456 789 MVA` (cross-border) | Orgnr + space + `MVA` suffix; cross-border form prefixes country code `NO` | Skatteetaten convention for VAT-registered businesses. The cross-border `NO`-prefix form is required on EU-facing invoices and documents. |
| **KID-nummer** | `12345678901234` (no grouping) | Single unbroken sequence, variable length 2–25 digits | Payment reference with Mod 10 / Mod 11 check digit. **No grouping** — the check-digit algorithm operates on the raw digit string, and visual grouping introduces copy-paste ambiguity. Render with `font-variant-numeric: tabular-nums` for legibility on invoice and giro lines. |
| **Phone numbers** (8-digit standard, fixed-line) | `22 22 22 22` | 4 groups (2-2-2-2), space-separated | Norwegian fixed-line 8-digit phone numbers. |
| **Phone numbers (≤5 digits)** | `1881` | 1 sequence, no grouping | Short numbers (directory enquiries, etc.). |
| **Phone numbers in 8xx range** | `812 34 890` | 3 groups (3-2-3), space-separated | Premium-rate / service numbers in the 8xx range have a different cadence. |
| **Credit card numbers** | `1234 5678 9012 3456` | 4 groups (4-4-4-4), space-separated | Standard 16-digit format. |
| **IBAN / BBAN** | `NO8330001234567` | 1 sequence, no grouping | Country prefix + check digits + account, run together. Tripletex / Atlas Library convention is single-sequence; ISO 13616 and Norwegian banks display IBAN in 4-character groups (`NO93 8601 1117 947`). The Tripletex single-sequence choice is **flagged for review** with the text department — see "Flagged for Review" at the foot of this file. |
| **SWIFT / BIC** | `NBHKNOKK030` | 1 sequence, no grouping | Bank identifier code (8 or 11 characters), no spaces. |
| **Postnummer + poststed** | `0150 OSLO` | 4-digit postnummer + single space + uppercase poststed | Posten convention. Norwegian addresses always pair these — postnummer and poststed appear together as a unit. Never display the postnummer alone or the poststed alone in an address context. |

For bank accounts specifically, the in-tables period-separated form (`1030.17.38765`) is a layout-driven variant — the period takes less width than the space and reads as a single visual unit, which works better in narrow columns. Outside tables, the space-separated form (`1030 17 38765`) is the default.

**Fødselsnummer masking detail.** Treat fødselsnummer as sensitive personal data per Datatilsynet's guidance and Personopplysningsloven. The full 11-digit form should only render when the user is verifying their own record, an authorised payroll/accounting user is processing payroll, or a statutory submission requires the full identifier. In every other display context — list rows, summary cards, customer-detail panes where the full ID isn't load-bearing — render the masked form `180690 *****`. The masked form keeps the date-of-birth portion (which is less sensitive on its own) and hides the personal-number portion (which together with the date-of-birth uniquely identifies a person).

**Postnummer + poststed pairing.** Norwegian postal addresses always render postnummer and poststed together as a single line: `0150 OSLO`. Don't split them across visual elements (e.g. postnummer in one field and poststed in another with a line break between) — they read as a unit. The poststed is conventionally rendered in **uppercase**, even when the surrounding text is mixed case.

**Violations**

- Bank account rendered without any grouping (`10301738765`) — error
- Bank account using a non-canonical grouping (`10 30 17 38 765`, `1030 1738 765`) — error
- Bank account using period separator outside a table (`1030.17.38765` on a detail view or in body copy) — warning (period separator is reserved for the in-table variant)
- Personal ID rendered with the wrong grouping (`18 06 90 12345`, `180 690 12345`) — error
- Fødselsnummer rendered in full on a non-essential display surface (list row, summary card, search result) — error (Datatilsynet sensitivity violation)
- Fødselsnummer masking that hides the date-of-birth portion instead of the personal-number portion (`****** 12345`) — error (mask the last 5, not the first 6)
- Organisasjonsnummer rendered without 3-3-3 grouping (`123456789`, `12 34 56 789`) — error
- MVA-nummer rendered without the `MVA` suffix on a Norwegian invoice or tax document — error
- MVA-nummer on a cross-border (EU) document without the `NO` country prefix — error
- KID-nummer rendered with grouping (`1234 5678 9012 3456`) — error (the check-digit algorithm and copy-paste behaviour both require single sequence)
- Phone number rendered without grouping (`22222222`) — error
- 8xx-range phone number using the standard 2-2-2-2 grouping instead of 3-2-3 (`81 23 48 90`) — warning
- Credit card number with grouping other than 4-4-4-4 — error
- IBAN/BBAN rendered with 4-character grouping (`NO83 3000 1234 567`) — note (matches ISO 13616 / Norwegian bank convention; pending text-department review of whether to switch the rule)
- SWIFT/BIC rendered with spaces — warning
- Postnummer rendered without the poststed pairing in an address context — error
- Postnummer + poststed where the poststed is not uppercase (`0150 Oslo`) — warning

**Examples**

✓ Correct (inline bank account, NO): "Konto: **1030 17 38765**"

✓ Correct (bank account in a payment table column, NO): `1030.17.38765`

✓ Correct (fødselsnummer on a non-essential surface, NO): `180690 *****`

✓ Correct (fødselsnummer on a payroll-essential surface, NO): `180690 12345`

✓ Correct (organisasjonsnummer on a customer card, NO): "Org.nr: **123 456 789**"

✓ Correct (MVA-nummer on a Norwegian invoice): `123 456 789 MVA`

✓ Correct (MVA-nummer on an invoice to an EU customer): `NO 123 456 789 MVA`

✓ Correct (KID-nummer on a payment line): `12345678901234` rendered in `tabular-nums`.

✓ Correct (phone number): `22 22 22 22` for a standard number, `812 34 890` for a premium-rate number.

✓ Correct (IBAN): `NO8330001234567` — no spaces (per current Atlas convention; pending review).

✓ Correct (address line): `Storgata 5, 0150 OSLO`

✗ Wrong: A bank account written as `1030.17.38765` in a customer-detail page body — period separator is for tables only.

✗ Wrong: Personal ID written as `18 06 90 12345` — the canonical grouping is (6-5).

✗ Wrong: A search-result row showing `180690 12345` for every contact — the personal-number portion should be masked unless the surface needs the full ID.

✗ Wrong: An invoice to a German customer with the supplier MVA-nummer rendered as `123 456 789 MVA` — needs the `NO` prefix for cross-border.

✗ Wrong: A KID-nummer rendered as `1234 5678 9012 3456` for legibility — the algorithm requires single-sequence, and the spaces are a copy-paste hazard.

✗ Wrong: An address rendered as `0150` on one line and `Oslo` on another — postnummer and poststed pair; render as `0150 OSLO` on the same line.

---

## Related Rules

- `design-rules/components/forms/input.md` § "Input alignment by input type" — right-alignment for numeric input types (number, amount, money, percentage); left-alignment for text-entry types including date.
- `design-rules/foundations/typography.md` — Rubik font family. Tabular-number variants are particularly relevant for any auto-updating numeric or time value (this file requires `tabular-nums` for those cases).
- `design-rules/components/forms/period-selectors/date-picker.md` — date-picker component (calendarMin vs typed-input behaviour, preset shortcuts, etc.) *(not yet documented — see `TODO.md`)*.
- `design-rules/components/forms/period-selectors/date-range-picker.md` — date-range-picker component, especially the named-range presets that match the patterns in Rule "Date ranges" *(not yet documented — see `TODO.md`)*.
- `charts.md` — chart axes must auto-size to fit locale-formatted compact-number labels (`14,0 mill.` needs more than 60px on Rubik 14px). This file owns the format; the surrounding-component accommodation rule is `charts.md`'s problem *(not yet documented — see `TODO.md`)*.
- `foundations/identifiers.md` — possible future split of Rule "Identifier formats" if the identifier list grows further (D-nummer, DUF-nummer, foreign VAT numbers, etc.) *(does not yet exist)*.

---

## Flagged for Review

Items pending follow-up — captured here so they don't get lost between drafting and team sign-off:

- **IBAN spacing.** Rule "Digit grouping for identifiers" specifies single-sequence IBAN (`NO8330001234567`), matching the Figma source. ISO 13616, Bits AS, and every Norwegian bank UI (DNB, Sparebank 1, Nordea, Handelsbanken) display IBAN in 4-character groups (`NO93 8601 1117 947`). Olivier is checking with the Tripletex text department to confirm whether the single-sequence form is a deliberate Tripletex choice (e.g. for copy-paste reliability in payment forms) or a Figma transcription error. Pending that conversation, the rule follows Figma. **If the text department confirms the spacing should follow ISO 13616, update the rule and flag the Figma source for correction.**
- **EN locale space-thousands separator.** Rule "Norwegian locale defaults" specifies space as the thousands separator in both NO (`25 000,00`) and EN (`25 000.00`). The EN choice diverges from idiomatic Anglophone conventions (`25,000.00` US/UK style); it matches international SI style. This is either a deliberate "SI-style English for a multi-locale product" choice or an oversight propagated from the NO rule. **Worth a deliberate decision and a rationale paragraph.** Pending review, the rule keeps space-thousands across both locales for internal consistency.
- **Atlas date-component localisation.** Rule "Date format migration state" captures the current product-wide pattern of `yyyy-mm-dd` everywhere and the long-term aspiration of `dd.mm.yyyy` for non-table user-facing surfaces. The migration trigger is Atlas-side work — `DateField`, `<Input type="date">`, `DateSelector`, and `formatDate` need a localised render mode. Owned by the Astro team. **Add to `TODO.md` as a prerequisite for the date-format migration**; until that ships, the rule's current-pattern guidance is the working default.

---

## Out of Scope of This File

- **Locale switching mechanics** — *how* a user switches the surface language, and how product code picks up the new locale, is out of scope. This file documents *what each locale renders*.
- **Multi-currency math** — currency conversion, exchange-rate display, foreign-currency rounding rules. This file documents how a currency value is *displayed*; not how it's computed.
- **Form input parsing** — what the user is allowed to *type* into a number / amount / date input. The input rules for amount/money/percentage live in `forms/input.md`; date inputs live in `forms/period-selectors/date-picker.md` (stub).
- **Compact-number truncation in components** — when a chart axis is too narrow for `14,0 mill.` and truncates it to `4,0 mill.`, that's a component sizing bug, not a number-format issue. See `charts.md` for the component-side rule.
- **D-nummer / DUF-nummer** — identity numbers for non-residents and asylum seekers. Same 11-digit structure as fødselsnummer with masking convention; not currently called out separately because the masking rule applies. Future addition if the team finds need for a dedicated entry.
- **Privacy / consent-to-display logic** — *when* a fødselsnummer may be displayed in full versus masked is a product-policy decision documented elsewhere (the GDPR / Personopplysningsloven compliance work, owned by the platform team). This file specifies *how* to render either form; the *whether* lives outside Atlas.
- **Foreign-locale identifiers** — international VAT numbers (DE / SE / DK formats), SWIFT-routing for non-NO banks, international postal codes. Tripletex displays these as received from external sources; this file doesn't prescribe formatting for non-Norwegian identifiers. Render verbatim from the source.


---

## spacesuit.md

# Spacesuit

> **Status: REFERENCE — no rules enforced.** Reference doc only; revisit when the Spacesuit API / contract for product teams is stable enough to enforce rules.

## What is Spacesuit?

Spacesuit is the main navigation shell that wraps every Tripletex page. It is maintained by the Astro design system team and is not something product teams design or modify directly. It is documented here for context only — no design rules are enforced by Atlas.

## Structure

### Topbar
Contains (left to right):
- **Company chooser** — dropdown allowing users to switch between companies they do accounting for
- **Search** — global search
- **2FA warning** — conditional button, only shown when two-factor authentication is not enabled
- **AI Assistant** — icon button opening the AI Assistant Modal
- **In-app chat** — icon button opening the internal chat between users and accountants
- **Bookmark** — star icon saving the current page to the Favourites section in the sidebar
- **Alerts** — icon button for system alerts
- **Notifications** — icon button for notifications
- **User profile** — icon button for the logged-in user's account

### Sidebar
- Collapsible — two states: icons + labels, or icons only
- Navigation items vary by account type and purchased modules
- Contains a **Favourites section** showing pages bookmarked via the topbar star icon

## What Product Teams Need to Know

- All product team work is loaded as content inside Spacesuit
- Page headers sit directly below the topbar
- Sidebar width affects available content width in both collapsed and expanded states
- Do not design UI that conflicts with or overlaps Spacesuit chrome

## Owned By

Spacesuit is maintained by the Astro design system team. For questions or changes, contact Astro directly via Slack.


---

## layout.md

# Layout & Breakpoints Foundation

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document grid systems, breakpoints, content width, and how layouts adapt across screen sizes.


---

## elevation.md

# Elevation Foundation

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document shadow levels, z-index scale, and when to use elevation to create depth and hierarchy.


---

# COMPONENTS

---




---

## components/accordion.md

# Accordion Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Accordion component — expand/collapse behavior, header structure, spacing, and when to use accordions vs. tabs or inline content.

---

## components/alert.md

# Alert Rules

> **Status: DRAFT — quick write-up pending team review and Figma reconciliation per decision #51.** Drafted in support of `patterns/validation-feedback.md` so the form-level validation summary has a documented home component. Open questions in the footer; promote to ✅ once those are resolved.

An Alert is the in-context counterpart to a Banner. Where a Banner lives at the page level under the page header (per `design-rules/components/banner.md` § "Banner placement"), an Alert lives **inside** the form, modal, or section it relates to. Use an Alert to communicate something scoped to the surface the user is currently working in — a validation summary above a submit button, an error at the relevant point in a modal body, an information note inside a section card.

The load-bearing distinction: Banner placement is constrained, Alert placement is not. If a message is scoped to a smaller surface than the whole page, Alert is the right component.

**From the Atlas docs:** *"Alerts are meant to communicate short and clear messages. They should communicate a single item with an optional follow-up link."* This framing is the load-bearing constraint on Alert content — it's not a button-bearing surface, not a multi-paragraph explanation, not a list of unrelated items. If the message you want to convey doesn't fit "one item with an optional follow-up link", Alert is probably not the right component.

For *when* to reach for an Alert versus a Banner, Notification, or inline-field message, see `patterns/banner-usage.md` (currently covers banners; the Alert side will be folded in once this file is promoted).

**Figma reference**: [Atlas Library — Alert](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library) — specific node-id pending Figma reconciliation (per the status footer); the link opens at the library root for now, navigate to the Alert frame.

---

## Rule: Alert anatomy

**Description**

Every Alert uses the same structure: an intent icon in the upper-right corner of the Alert, a single line of message text by default, and an optional "Read more" link that lets users learn about the message in more depth without expanding the Alert's footprint. Alerts may carry multiline content when one line genuinely isn't enough, but the canonical form is one line plus an optional link. **Alerts do not contain action buttons** — Alert is a messaging surface, not an action surface; if the user needs to take action in response to an Alert, the action lives elsewhere (the form's submit button, a separate Banner that's intended to carry actions, or a different component entirely). The "Read more" link is the only inline navigation Alert supports.

**How to Apply**

1. **Intent icon** — placed in the **upper-right corner** of the Alert. Variant-specific (info / check / warning / error / sparkle), per "Alert variants" below. The icon position is fixed; it does not move with content alignment.
2. **Message text** — single line by default. Aim for the shortest message that's still clear.
3. **"Read more" link** (optional) — inline with the message text or immediately after, taking the user to fuller documentation, help, or context.
4. **Multiline content is allowed** when one line genuinely isn't enough, but always check first whether "one line + Read more link" would communicate the same thing.
5. **No action buttons.** If an action is needed (Retry, Save, Cancel, etc.), the action lives outside the Alert.

**Violations**

- Alert containing an action button (e.g. `[Retry]`, `[Save]`, `[Cancel]`) — warning (Alert is a messaging surface; actions belong in the surrounding component or in a Banner that's intended to carry actions)
- Alert with the intent icon in any position other than upper-right — error
- Alert with multi-paragraph content where a single line + Read more link would have communicated the same thing — note
- Alert with no message text — error
- Alert containing multiple unrelated items in a list (other than the validation-summary extended use below) — warning (per the "single item" framing from the docs)

**Examples**

✓ Correct: An Info Alert at the top of a section card reads "Drafts auto-save every 30 seconds." with a `Read more` link to the docs.

✓ Correct: An Error Alert above a form's submit button reads "Couldn't save — please try again." with a `Read more` link to troubleshooting.

✗ Wrong: An Alert with `[Retry] [Cancel]` action buttons inside it — actions belong outside the Alert, e.g. in the form's button group or in a Banner.

✗ Wrong: An Alert with three paragraphs of explanation where "Could not connect to bank — Read more" would have done the job.

**Extended use — form-level validation summary.** The form-level error summary documented in `patterns/validation-feedback.md` composes Alert in a way that extends the "single item with optional follow-up link" anatomy into a heading + linked list of N field errors. This is an explicit and documented extension, justified by Atlas's current lack of a dedicated `ErrorSummary` component (tracked in `TODO.md` § "Dedicated `ErrorSummary` component (Astro)"). When that component lands, the validation-summary use moves to it and Alert reverts to its canonical single-item shape. **This extension is not a precedent for using Alert as a multi-item container generally** — outside the validation-summary case, the single-item rule holds.

---

## Rule: Alert variants

**Description**

Alerts come in five semantic variants, each tied to a fixed colour and icon. The variant communicates the alert's tone at a glance and aligns with the marker contract used elsewhere in Atlas (see `design-rules/components/forms/input.md` § "Content type markers" — same semantic vocabulary, applied here at component level rather than at field level). Banners use a fuller nine-label set; Alert's set is deliberately narrower because Alert sits in-context and benefits from a tighter palette.

**How to Apply**

| Variant | Colour | Surface tokens | Border tokens | Icon | Used for |
|---|---|---|---|---|---|
| **Info** | Blue | `--surface-background` (default) | `--border-info` | Info icon | Neutral information relevant to the current surface |
| **Success** | Green | `--surface-success-*` | `--border-success` | Check icon | Positive confirmation in context (e.g. "Draft saved") |
| **Warning** | Yellow | `--surface-warning-*` | `--border-warning` | Warning icon | Something worth a second look but not blocking |
| **Error** | Red | `--surface-error-*` | `--border-error` | Error icon | Something is wrong on this surface and needs the user's action |
| **Automation** | Purple | `--surface-automation-*` | `--border-automation` | Sparkle icon | A value or action the system filled in / suggested for the user — AI-recognised value, automation feedback, suggestion accepted |

Surface tokens use the `-rest` / `-hover` / `-highlight` / `-active` suffixes from `design-rules/foundations/colors.md`. Border interaction variants (`-hover`, `-focus`) are defined there too — apply them on hover/focus when the Alert is interactive (e.g. contains a Read more link). Icon-to-variant mapping follows `patterns/icon-usage.md`. The Automation variant intentionally mirrors the Automation marker on `forms/input.md` § "Content type markers" so a sparkle on a field and a sparkle on an in-context Alert read as the same semantic family.

**Violations**

- Alert variant set without the matching surface and border tokens — error
- Alert with no variant, or a custom colour outside the five — error
- Variant icon mismatched to the variant (e.g. info icon on an Error alert) — error
- Variant colour mismatched to the variant (e.g. Warning Alert rendered red) — error

**Examples**

✓ Correct: An Error Alert above a form's submit button using `--surface-error-rest` and `--border-error` with an error icon, hosting a form-level validation summary (per the extended-use note above).

✓ Correct: A Warning Alert at the top of a modal body using `--surface-warning-rest` and `--border-warning` with a warning icon, flagging a non-blocking concern with the user's input.

✓ Correct: An Automation Alert in a section explaining "Bookkeeping suggestions are turned on for this account." with a `Read more` link.

✗ Wrong: A Success Alert rendered with `--border-error` because the team thought green was "not visible enough" — variant mismatch.

✗ Wrong: A bespoke "purple-blue" Alert variant invented for a specific surface — only the five documented variants exist.

---

## Rule: Alert placement

**Description**

Alerts can be placed anywhere their context calls for them — inside a form, inside a modal body, inside a section card, between sections of a page. This is the load-bearing distinction from Banners: a Banner must live directly under the page header; an Alert must live inside its scope. Match the Alert's width to the surface it scopes to, and place it at the natural top of that surface unless a more specific rule says otherwise.

**How to Apply**

1. Place the Alert at the natural top of its scope: top of the form, top of the modal body, top of the section card.
2. **Form-level validation summary**: place the Alert immediately above the submit button per `patterns/validation-feedback.md`. The validation-feedback rule overrides the "natural top" default for this specific case — the summary belongs near the action that triggered it, not at the top of the form.
3. **In-modal error**: place the Alert at the relevant point in the modal body per `design-rules/components/modal.md` § "Errors render inline". Banners are forbidden inside modals; Alert is the right component for any in-modal message.
4. Match the Alert's width to its containing surface — same width as the form, modal body, or section card it lives in. Alerts do not span beyond their scope.
5. **Multiple Alerts on the same surface**: order by severity, top-down: **Error → Warning → Success → Info**.

**Violations**

- Alert placed outside its scoping surface (e.g. above the page header for a form-scoped message) — error (use Banner instead)
- Alert width mismatched to its containing surface — warning
- Multiple Alerts on the same surface in arbitrary order (not severity-first) — warning

**Examples**

✓ Correct: An Error Alert hosting the form-level validation summary, placed 16px above the submit button inside a long form.

✓ Correct: A Warning Alert at the top of a modal body explaining that the user's draft will be discarded if they proceed.

✗ Wrong: An Alert rendered under the page header to communicate a system-level message — use a Banner.

✗ Wrong: An Error Alert below a Warning Alert on the same modal body — Error should be on top.

---

## Rule: Alert dismissibility

**Description**

Most Alerts can be dismissed by the user via a close button. **Error** Alerts are the exception: they describe a state the user shouldn't be allowed to ignore on the surface they're working in, so they persist until the underlying condition is resolved. This mirrors the Banner dismissibility convention — the difference is scope (page vs. in-context), not behaviour.

**How to Apply**

| Variant | Dismissable? | How it goes away |
|---|---|---|
| Info / Success / Warning / Automation | Yes | User clicks the close button (top-right of the Alert, beside the intent icon) |
| Error | No | Cleared automatically when the underlying condition resolves |

Alerts do not auto-dismiss on a timer. The user closes them or the system clears them. For time-limited messages, use a Notification instead. Note: when both the close button and the intent icon are present, the intent icon sits in the upper-right per the anatomy rule and the close button sits adjacent — typically immediately to the icon's left, with the exact arrangement deferred to Figma.

**Violations**

- Error Alert with a close button — error
- Dismissable Alert variant (Info / Success / Warning / Automation) without a close button — warning
- Alert auto-dismissing on a timer — error (use Notification for time-limited messages)

**Examples**

✓ Correct: An Error Alert hosting a validation summary persists until the user fixes the invalid fields — no close button visible.

✓ Correct: A Success Alert "Draft saved" inside a section card has a close button; once dismissed, it does not reappear on the same surface.

✗ Wrong: An Error Alert with a close button — the user can dismiss the message they need to act on.

---

## Note on usage frequency

Alert is a noticeable in-context surface, and its impact erodes when it's everywhere. Two specific concerns worth keeping in mind when reaching for an Alert — **these are guidance, not violations, and no severity is attached**:

1. **Avoid stacking unrelated Alerts on the same surface.** Multiple Alerts in close vertical proximity reduce each one's salience. If you find yourself reaching for several Alerts on one form or one section, consider whether the messages can be combined, deferred, or moved to a different component.

2. **Automation Alerts are currently overused across the product.** The purple Automation variant is appearing on many surfaces where the message either doesn't carry meaningful weight ("this was filled in automatically" on every auto-filled field becomes wallpaper) or could be communicated more lightly via the field-level Automation marker from `forms/input.md` § "Content type markers". Before reaching for an Automation Alert, ask whether the field-level marker — which is less visually loud — would do the job.

The purpose of these notes is to nudge teams toward considered use, not to gate. Track concrete cases where Alert overuse becomes a measurable problem in `research/questions.md` rather than tightening the rule pre-emptively.

---

## Open Questions (for team review)

- **Anatomy fine detail.** Variants, placement, dismissibility, and the icon-upper-right + single-line + Read-more shape are now specified, but exact icon size, padding, line-height, and the close-button-vs-intent-icon arrangement in the upper-right are deferred to the Atlas Library Figma. Reconcile against Figma during team review.
- **Stacking rules.** "Multiple Alerts on the same surface should be ordered by severity (Error → Warning → Success → Info), top-down" is the working position from the placement rule. Automation's place in that order is currently undecided — likely between Warning and Success, but worth confirming.
- **Severity-ordered stacking vs. the "don't stack unrelated Alerts" guidance** are in tension. Resolution likely: stacking is allowed when the surface genuinely has multiple unrelated messages and the messages can't be combined, but should be rare. Capture during review.
- **Surface-token coverage in `colors.md`** — **resolved**. The `--surface-{state}-{suffix}` naming convention is now explicit in [`../foundations/colors.md`](../foundations/colors.md) *Surface state variants*; the state × suffix table is the authoritative source for values, and component rule files reference the composed variable names directly. Keeping this entry for audit trail.

---

## Related Rules

- `design-rules/components/banner.md` — the page-level counterpart; Banner placement is constrained to under-the-page-header, Alert placement is not
- `patterns/banner-usage.md` — when to reach for a Banner vs. an Alert vs. inline content; the Alert side will be folded in once this file is promoted
- `design-rules/components/forms/input.md` § "Content type markers" — the field-level marker contract this file mirrors at component level (Info / Automation / Warning / Error are shared; Alert adds Success)
- `design-rules/components/modal.md` § "Errors render inline" — Alerts are how errors render inside modals (banners are forbidden there)
- `patterns/validation-feedback.md` — Alert is the canonical container for the form-level validation summary *(currently being drafted)*
- `design-rules/foundations/colors.md` — surface and border tokens for the four variants
- `patterns/icon-usage.md` — icon-to-variant mapping


---

## components/avatar.md

# Avatar Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Avatar component — sizes, fallback states (initials, placeholder icon), usage in lists and headers.

---

## components/banner.md

# Banner Rules

Banners communicate important system or product information that users need to be aware of — product updates, system errors, automations, deadlines, onboarding nudges. They are prominent and don't auto-dismiss; the user closes them or the system clears them when the underlying condition resolves. That prominence makes them powerful for critical messages and a source of fatigue if overused.

For *when* to reach for a banner versus a less intrusive component, see [`patterns/banner-usage.md`](../../patterns/banner-usage.md).

**Figma reference:** [Atlas Library — Banner](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=326-37538&t=DEKm0jloX2sZhgZk-11)

---

## Rule: Banner anatomy

**Description**

Every banner has a vertical structure: a Label at the top (load-bearing — determines type and colour), required heading and body text, and an optional button group. An optional 100×100 illustration sits in the top-left; when present, the rest of the stack shifts to its right.

**How to Apply**

Vertical order, left-aligned:

1. **Label** (required, top-left) — see *Banner labels and colour mapping* below.
2. **Heading** (required).
3. **Body text** (required, may contain links).
4. **Button group** (optional) — primary → secondary → tertiary, left-to-right per [`patterns/button-placement.md`](../../patterns/button-placement.md).

**Illustration** (optional): 100×100, placed top-left; the rest of the stack shifts to its right while remaining left-aligned within the right-side column.

**Violations**

- Banner missing a Label — error (no Label = no type / colour identity)
- Heading or body text missing — error
- Element order other than Label → heading → body → buttons — error
- Illustration not 100×100 — warning
- Illustration placed somewhere other than top-left — warning
- Button group not following the primary → secondary → tertiary order — error

**Examples**

✓ An Info banner with `[Info label]` / heading *"Annual report deadline"* / body *"File before 30 April to avoid penalties."* / `[Learn more]` button.

✗ A banner with just a heading and body text — no Label, type unclear.

✗ Illustration centred above the heading — breaks the left-aligned anatomy.

---

## Rule: Banner labels and colour mapping

**Description**

Every banner is identified by one of the nine canonical Label types defined in [`labels.md`](labels.md) *Type and colour mapping*. Choosing a Label picks the colour too — the colour communicates the banner's tone at a glance, before the user reads the words. The Label / colour mapping is canonical in `labels.md`; banner.md inherits it.

**How to Apply**

- Pick the Label type whose intent matches the banner's message — see [`labels.md`](labels.md) *Type and colour mapping* for the nine types, their colours, and what each is used for.
- The banner's background colour comes from the `--surface-{state}-{level}` token mapped to the Label's type (per `labels.md`).
- For **Error** and **Attention** banners, the body must include recovery information — what the user can do to resolve the situation.

**Violations**

- Banner colour set without a corresponding Label — error
- Label and colour mismatched (e.g. green banner with **Tips** Label) — error
- Custom Label outside the nine canonical types — error
- **Error** or **Attention** banner without recovery information in the body — error

**Examples**

✓ A purple **Automated** banner announcing a new automation the user can enable.

✗ A green banner with the **Tips** Label — green is for **Done**.

✗ An **Error** Label with the body *"Something went wrong."* — no recovery information.

---

## Rule: Banner placement

**Description**

Banners live directly under the page header and span the full content width of the page. Banners do not appear inside the page header, inside forms, inside sections, or inside modals. The page header has its own alert slot for page-or-higher scope alerts (see [`page-header.md`](page-header.md) *Alert placement*); the in-form / in-section / in-modal equivalent is the Alert component (see [`alert.md`](alert.md)).

**How to Apply**

- Place the banner immediately below the page header, before the page's primary content.
- Match the banner's width to the page's content width.
- Banners never appear inside forms, sections, modals, the page header, or any sub-container — use Alert instead.

**Violations**

- Banner placed inside the page header (any slot) — error (the page header has its own Alert slot; banners go below it)
- Banner placed inside a form, section, or modal — error (use Alert — see [`alert.md`](alert.md))
- Banner used inside a form to host a form-level validation summary — warning (transitional; migrate to Alert per [`patterns/validation-feedback.md`](../../patterns/validation-feedback.md). New work uses Alert from the start. See *Open Questions* for the migration.)
- Banner narrower or wider than the page content width — warning
- Banner placed somewhere other than directly under the page header — warning

**Examples**

✓ Banner sits between the page header and the main page content, edge-to-edge with the content area.

✗ A banner inside a form announcing a system update — system-level info belongs below the page header.

✗ A banner placed inside the page header's alert slot — banners and alerts are distinct components; that slot uses Alert.

---

## Rule: Banner dismissibility

**Description**

Most banners can be dismissed by the user via a close button — they're informational and don't need to keep occupying space once seen. **Error** and **Attention** banners are the exception: they describe a system state the user shouldn't ignore, so they persist until the condition resolves. Banners do not auto-dismiss on a timer.

**How to Apply**

| Label | Dismissable? | How it goes away |
|---|---|---|
| Info / Help / Tips / News / Get started / Automated / Done | Yes | User clicks the close button (top-right) |
| Attention / Error | No | Cleared automatically when the underlying condition resolves |

When a user dismisses a banner, **do not show that same banner to that user again**. Surfacing a dismissed banner is noise.

**Violations**

- **Error** or **Attention** banner with a close button — error
- Dismissable banner type (Info / Help / Tips / News / Get started / Automated / Done) without a close button — warning
- Same banner re-shown to a user who has already dismissed it — error
- Banner auto-dismissing on a timer — error (use the Notification component for time-limited messages)

**Examples**

✓ An **Error** banner persists until the underlying error is resolved — no close button visible.

✓ A **Tips** banner has a close button; once clicked, the banner is gone for that user and doesn't reappear on the next session.

✗ An **Attention** banner with a close button — the user can dismiss a warning they shouldn't be allowed to ignore.

✗ A **News** banner reappearing on every page load even after the user closed it.

---

## Related Rules

- [`labels.md`](labels.md) — canonical Type and colour mapping that banner Labels inherit.
- [`alert.md`](alert.md) — the in-context counterpart to Banner; used inside forms, modals, sections, and the page header's alert slot.
- [`page-header.md`](page-header.md) — the page header's alert slot is distinct from a Banner; banners sit below the page header, not inside it.
- [`product-spotlight-banner.md`](product-spotlight-banner.md) — the upsell-specific banner variant (separate component, separate rules).
- [`patterns/banner-usage.md`](../../patterns/banner-usage.md) — when to reach for a banner vs an alert vs inline content; stacking and fatigue.
- [`patterns/button-placement.md`](../../patterns/button-placement.md) — button group order inside a banner.
- [`patterns/validation-feedback.md`](../../patterns/validation-feedback.md) — form-level error summaries use Alert, not Banner.

---

## Open Questions

- **Banner-inside-form migration.** Existing Tripletex forms commonly use `Banner variant="error"` for form-level validation summaries. The canonical pattern is Alert per [`patterns/validation-feedback.md`](../../patterns/validation-feedback.md). The migration window is open; tracked as a warning-severity violation in *Banner placement* so existing usage is flagged but not auto-rejected. Close this once the migration is complete.


---

## components/buttons.md

# Button Rules

Atlas buttons come in three variants — **Primary**, **Secondary**, **Tertiary** — in two sizes (medium and small), with optional icons. Action buttons (spinner + success / error states) and icon buttons (Tertiary without a label) are *modes* of the three variants, not separate variants.

For *where* buttons live on the page (page header, form footer, section), see [`patterns/button-placement.md`](../../patterns/button-placement.md).

**Figma reference:** [Atlas Library — Buttons](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=3-193&p=f&t=DEKm0jloX2sZhgZk-11)

---

## Rule: One primary button per user goal

**Description**

A primary button signals the main action that advances the user's goal. Multiple primary buttons for the same goal split user attention and dilute the call to action. Determine which action is primary by analytics, not opinion — pick the action users actually take most.

**How to Apply**

- Define the user's goal for this step.
- Identify the action users take most often (analytics).
- Make that action Primary; alternative paths are Secondary or Tertiary.
- If users are genuinely split between equally important actions, revisit the design before adding a second Primary.

**Multi-step actions** — if users need to choose between multiple primary paths, use a drawer or modal triggered by the Primary button. A split-button component (button + dropdown) is on the roadmap for this pattern — see `TODO.md`. Contact the Astro design system team if you need it.

**Violations**

- Multiple Primary buttons visible at the same time for the same user goal — error
- Primary button used for a secondary workflow — warning
- Action analytics suggest a different action should be Primary, but it isn't — note

**Examples**

✓ Analytics show 80% of users click *Send invoice*, 15% click *Save draft*, 5% click *Schedule*. *Send invoice* is Primary; the others are Secondary.

✗ Three "important" Primary buttons on the same form.

---

## Rule: Button order in groups

**Description**

When multiple buttons appear together, their order signals priority. Atlas uses a Primary-anchored order with direction determined by the container's alignment.

**How to Apply**

- **Left-aligned groups** (form footers, dialog actions): Primary → Secondary → Tertiary, left to right.
- **Right-aligned groups** (page header actions): Primary furthest right, Secondary middle, Tertiary furthest left.
- **Overflow** (when buttons don't fit): kebab (`[⋮]`) icon button at the rightmost position. Tertiary buttons collapse into the overflow first; Primary never collapses. See [`patterns/button-placement.md`](../../patterns/button-placement.md) for the full responsive collapse order.

For placement on the page (where the button group itself lives — header, form footer, section), see [`patterns/button-placement.md`](../../patterns/button-placement.md).

**Violations**

- Cancel or any Secondary / Tertiary action rendered before Primary in a left-aligned group — error
- Primary not in the rightmost position of a right-aligned group — error
- Tertiary appearing between Primary and Secondary (mixed ordering) — warning
- Inconsistent ordering across similar contexts in the same product — warning

**Examples**

✓ Left-aligned form footer: `[Send (primary)] [Save draft (secondary)] [Cancel (tertiary)]`.

✓ Right-aligned page header: `[Cancel (tertiary)] [Save draft (secondary)] [Send (primary)] [⋮]`.

✗ `[Cancel] [Send]` — Cancel before Primary in a left-aligned group.

✗ `[Send] [Cancel] [Save draft]` — random order.

---

## Rule: Button variants

**Description**

Atlas has exactly three button variants: **Primary**, **Secondary**, **Tertiary**. Action buttons and icon buttons are *modes* of these variants, not additional variants.

**How to Apply**

- **Primary** — the main action for the current goal.
- **Secondary** — supporting action or alternative path.
- **Tertiary** — less important action (help, cancel, skip). Transparent at rest; hover and active surfaces appear on interaction.
- Never invent a fourth variant. If you feel the need, the action probably belongs in a different placement — not a different colour.

Action buttons (spinner + success / error states) and icon buttons (Tertiary without a label) are documented below in their own rules.

**Violations**

- Variant other than Primary, Secondary, or Tertiary — error
- Bespoke "danger", "success", or other coloured variant invented — error (the only place green or red appears on a button is the post-spinner result state of an Action button — see *Action buttons*)
- Secondary used when Primary is needed — warning
- Tertiary used for an important action — warning

**Examples**

✓ Send (Primary), Save draft (Secondary), Cancel (Tertiary).

✗ Send (Secondary), Cancel (Primary).

✗ A bespoke green "Confirm" button on a one-off screen.

---

## Rule: Button colours

**Description**

Each variant maps to a fixed set of semantic colour tokens. Buttons use these and only these — no custom colours, no global palette tokens, no inline hex.

**How to Apply**

| Variant | Background tokens | Text / icon token |
|---|---|---|
| Primary | `--action-primary-rest` / `-hover` / `-active` | `--text-on-action` |
| Secondary | `--action-secondary-rest` / `-hover` / `-active` | `--text-action` |
| Tertiary | `--action-tertiary-rest` (transparent) / `-hover` / `-active` | `--text-action` |

Tertiary's `-rest` is fully transparent (`#ffffff00`); the hover and active surfaces appear only on interaction. Icon buttons inherit the Tertiary tokens — see *Icon buttons*.

Green and red appear on a button **only** in the post-spinner success or error state of an Action button — see *Action buttons*.

**Violations**

- Hex value, global palette token, or any non-`--action-*` token used for a button background — error
- Colour outside the variant's mapped token group (e.g. Secondary using `--action-primary-*`) — error
- Green or red on a button outside the Action-button result state — error
- A new button colour family invented — error

**Examples**

✓ Primary button uses `var(--action-primary-rest)` for background, `var(--text-on-action)` for the label.

✗ Primary button hardcoded to `#0a41fa` even though it's the same colour as the token (must use the token).

✗ A bespoke green "Confirm" button on a one-off screen.

---

## Rule: Button sizes

**Description**

Atlas buttons come in two sizes: medium (default) and small. Both labelled and icon buttons share these sizes.

**How to Apply**

| Size | Height | Token | Use it for |
|---|---|---|---|
| Medium | 40px | `--element-height-large` | Standard actions in forms, footers, page headers |
| Small | 32px | `--element-height-medium` | Inline actions, secondary actions in tight spaces |

Use medium for all Primary and most Secondary buttons. Use small only when space is constrained or the action is clearly secondary.

**Violations**

- Button height other than 40px or 32px — error
- Hardcoded button height instead of `--element-height-large` / `--element-height-medium` — error
- Small size used for a Primary action — warning
- Mixed sizes in the same group — warning

**Examples**

✓ Form buttons are medium (40px).

✓ Inline *Edit* action is small (32px).

✗ Primary button is small.

---

## Rule: Button border radius

**Description**

All buttons use `--radius-default` (4px). No pill, no sharp corners, no per-context variation.

**Violations**

- Button border-radius other than 4px (`--radius-default`) — error
- Hardcoded `border-radius: 4px` instead of the token — error
- Pill-shaped (`border-radius: 9999px` / `50%`) or sharp-cornered (`border-radius: 0`) button — error

**Examples**

✓ `border-radius: var(--radius-default)` on every button variant and size.

✗ `border-radius: 9999px` — pill shapes aren't part of Atlas's button family.

✗ `border-radius: 4px` hard-coded — breaks if the token changes.

---

## Rule: Icon placement on labelled buttons

**Description**

Labelled buttons may include a single optional icon next to the label. The icon reinforces the action; it doesn't replace the label.

**How to Apply**

- Icon sits **to the right** of the label by default.
- One icon maximum — never both sides.
- Icon size matches button size:
  - Medium button (40px) → `--icon-size-medium` (24px).
  - Small button (32px) → `--icon-size-small` (20px).
- Icon colour inherits the variant's text token: `--text-on-action` for Primary; `--text-action` for Secondary and Tertiary.

**Exception — back buttons in multi-step flows:**

A button that navigates back to a previous step in a multi-step process (wizard, stepper, guided flow) may render with a **left-pointing arrow icon on the left** of the label, provided the button is placed in a left-aligned position. The icon's leftward direction visually reinforces the backward step. Example: `[← Previous step]`, `[← Back to step 2]`.

The carve-out is narrow — all three conditions must hold:

1. The button navigates back to a previous step in a multi-step process (wizard, stepper, guided flow). Not "previous record", "undo", or generic browser-back.
2. The icon is a left-pointing arrow from the Atlas icon library — see [`foundations/icons.md`](../foundations/icons.md) for the icon source and [`patterns/icon-usage.md`](../../patterns/icon-usage.md) for the canonical per-action mapping.
3. The button is left-aligned in its group / context. Right-aligned button groups don't get this carve-out.

**Violations**

- Icon placed to the left of the label outside the back-button carve-out above — error
- Icons on both sides of the label — error
- Icon size not matching button size — warning
- Custom icon colour diverging from the variant's text token — error
- Left-pointing arrow icon on the left of a button that isn't a back-navigation button in a multi-step flow — warning
- Back-navigation button in a multi-step flow rendered with the arrow on the right or without an arrow — warning (the leftward direction is the affordance)

**Examples**

✓ `[Download ↓]` — medium Primary, 24px icon on the right (default).

✓ `[← Previous step]` — left-aligned back button in a multi-step wizard with a left-pointing arrow on the left (carve-out).

✗ `[↓ Download]` — icon on the left without the back-navigation carve-out.

✗ `[↓ Download ↓]` — icons on both sides.

✗ A right-aligned button labelled `[← Cancel]` — the carve-out requires left-aligned placement; right-aligned button groups don't get it.

✗ A multi-step wizard's *Back* button rendered as `[Back ←]` — the carve-out applies; the arrow should be on the left, not the right.

---

## Rule: Button spacing

**Description**

Inter-button spacing within a group is **8px**. Form-to-button and section-to-button spacing are governed by [`patterns/button-placement.md`](../../patterns/button-placement.md). The Atlas spacing scale is canonical in [`spacing.md`](../foundations/spacing.md).

**Violations**

- Inter-button spacing other than 8px — warning
- Spacing values not on the Atlas spacing scale — warning (see [`spacing.md`](../foundations/spacing.md))

**Examples**

✓ 8px between `[Send]` and `[Cancel]`.

✗ 5px between buttons — off-scale.

---

## Rule: Action buttons

**Description**

Action buttons are a *mode* — not a variant — available on any standard button (Primary, Secondary, Tertiary, icon). They show a sequence of states tied to an async operation: default → spinner → success or error. The post-spinner green and red are the **only** places green or red appear on a button anywhere in Atlas.

**How to Apply**

1. Start from the underlying variant.
2. On click: replace the label / icon contents with a spinner; the variant's background colour is preserved.
3. On success: background becomes `--surface-success-active` (`#33ac2e`); contents become a success icon (plus the original label on labelled buttons).
4. On error: background becomes `--surface-error-active` (`#e83645`); contents become an error icon (plus the original label).
5. Hold the result state briefly, then return to the default state or advance the screen.

Icon buttons in Action mode follow the same flow with icons in place of labels: icon → spinner → success icon or error icon, with the same green / red background on result.

**Violations**

- Green or red on any button outside the Action-button success / error state — error
- Result colour shown before the spinner state resolves — error
- No success / error feedback after the spinner — error
- Loading state hidden from users — error
- Action mode used for an instant (non-async) action — note

**Examples**

✓ User clicks *Save* (Primary), spinner replaces the label, then a green checkmark on `--surface-success-active` background.

✓ User clicks the icon-button delete, spinner replaces the icon, then an error icon on `--surface-error-active` if it failed.

✗ A non-Action Primary button rendered with a green background to signal "go".

✗ Action button changes to loading but never shows a result.

---

## Rule: Icon buttons

**Description**

Icon buttons display only an icon — no label. They use the **Tertiary variant only** and come in the same two sizes as labelled buttons (medium 40px, small 32px). Every icon button pairs with a tooltip containing the button's label.

**How to Apply**

- Use only when the icon is immediately understandable.
- Always pair with a tooltip on hover containing only the button label (e.g. *"More actions"*, *"Close"*, *"Settings"*). For rich on-click content, use a Popover instead — see [`patterns/popover-usage.md`](../../patterns/popover-usage.md).
- Icon buttons render with the Tertiary tokens (`--action-tertiary-rest` / `-hover` / `-active`) — never Primary or Secondary.
- Sizes match labelled buttons:
  - Medium icon button (40px) → `--icon-size-medium` (24px) icon.
  - Small icon button (32px) → `--icon-size-small` (20px) icon.
- Icon buttons can run in Action-button mode — see *Action buttons*.

**Violations**

- Icon button without a tooltip — error
- Tooltip containing more than the button label — error
- Icon button rendered in Primary or Secondary tokens — error
- Icon button at a size other than 40px or 32px — error
- Ambiguous icon (user can't tell what action it triggers) — warning

**Examples**

✓ `[⋮]` with tooltip *"More actions"* (medium Tertiary icon button).

✓ `[✕]` with tooltip *"Close"* (small Tertiary icon button).

✗ Ambiguous icon with no tooltip.

✗ Icon button rendered in Primary blue.

✗ Icon button with a complex tooltip text.

For icon-to-action mappings, see [`patterns/icon-usage.md`](../../patterns/icon-usage.md).

---

## Rule: Button Typography

**Description**
Button labels inherit Atlas's standard Body text style — the same typeface, 
size, and weight used for body copy. Typography is not adjusted per variant 
or size. The distinction between medium and small buttons is communicated 
through height and padding alone, not through font size.

Regular weight is intentional. Buttons are interactive surface elements; 
the variant and colour communicate hierarchy, not the weight of the label. 
Increasing weight to semibold or bold introduces visual noise and competes 
with surrounding content.

**When to Use**
All labelled buttons in all three variants (Primary, Secondary, Tertiary) 
and both sizes (medium 40px, small 32px).

**How to Apply**

| Property | Value |
|---|---|
| Font style | Body (inherited — no button-specific token) |
| Font weight | Regular |
| Size | Same for medium and small buttons |
| Case | Sentence case |
| Lines | Always single line |
| Colour | Follows the variant's text token — see *Button Colors* |

**Label length**
Keep labels short. One to three words is the norm. 
If a label exceeds three words, treat it as a signal to review:
- Is the action ambiguous without the extra words?
- Can the label be rewritten more precisely?
- Does this action belong in a dialog or menu where there is more room for context?

Longer labels are occasionally justified, but they require a deliberate decision — not a default.

**Label writing**
1. Use sentence case — "Send invoice", not "Send Invoice" or "SEND INVOICE"
2. Start with a verb — "Save", "Delete entry", "Open report"
3. Avoid punctuation at the end
4. Avoid filler words — "Click to save" → "Save"

**Violations**
- Font weight other than Regular — error
- Title case or all-caps labels — warning
- Label longer than three words without documented justification — note
- Multi-line label — error
- Font size overridden from the Body style — error

**Examples**
✓ Correct: "Send invoice" — verb-first, sentence case, two words
✓ Correct: "Save" — single word, unambiguous in context
✗ Wrong: "Send Invoice" — title case
✗ Wrong: "Click here to send your invoice" — no verb-first, too long, filler
✗ Wrong: Bold or semibold label — weight signals hierarchy; the variant does that job

---

## Related Rules

- [`patterns/button-placement.md`](../../patterns/button-placement.md) — where buttons live on the page (page header, form footer, section); responsive collapse order.
- [`patterns/icon-usage.md`](../../patterns/icon-usage.md) — icon-to-action mappings.
- [`patterns/popover-usage.md`](../../patterns/popover-usage.md) — tooltips vs popovers (icon-button tooltips reference this).
- [`tokens.md`](../foundations/tokens.md) — element height tokens (40px / 32px), border radius (4px).
- [`colors.md`](../foundations/colors.md) — action token family (`--action-{primary,secondary,tertiary}-*`).
- [`spacing.md`](../foundations/spacing.md) — Atlas spacing scale used between buttons.


---

## components/card.md

# Card Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Card component — layout, spacing, elevation, header/footer structure, and when to use cards vs. other containers.

---

## components/chip.md

# Chip Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Chip component — variants, interactive vs. static chips, sizing, and usage. See also `patterns/chips-vs-buttons.md` for when to use chips vs. buttons.

---

## components/content-switcher.md

# Content Switcher Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Content Switcher component — when to use vs. tabs, sizing, and behavior.

---

## components/data-table.md

# Data Table Rules (Excel Style)

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Excel-style Data Table component — inline editing, cell types, column resizing, and keyboard navigation.

---

## components/drawer.md

# Drawer Rules

> **Status: DRAFT — pending team review per decision #62.**

The **drawer** is the option-list surface used by Select, Dropdown, and Combobox — a small overlay that opens from a trigger and contains a vertical list of interactive rows, optionally grouped. Atlas standardises on *drawer* throughout this Knowledge Base; the Figma library calls the same component *Popup*.

This file documents the surface itself. Picker-specific behaviour (single vs multi selection, search threshold, trigger placeholder) lives in the consuming component's file.

**Figma references:**

- [Drawer](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=427-39014)
- [Interactive list items](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=427-38885)
- [Drawer with groupings](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=11278-40821)

---

## Out of scope

- **Picker-specific behaviour** (single vs multi selection, search threshold, trigger placeholder) — owned by `forms/select.md`, `forms/dropdown.md`, `forms/combobox.md`.
- **Side panels** — the slide-in surfaces used by the PDF viewer, in-app chat, and AI Assistant are a layout concept, not a component. See `design-rules/foundations/layout.md` *(pending)*.
- **Popovers** — informational content (label-only tooltips, rich-content popovers) lives in `patterns/popover-usage.md`.

---

## Rule: Drawer anatomy

**Description**

A drawer is anchored to its trigger, opens below by default, and flips above when there's no room below.

**How to Apply**

1. Anchor below the trigger by default; flip above when there's no room below.
2. 4px gap between the trigger and the drawer.
3. 4px corner radius (`--radius-default`).
4. 1px border using `--border-primary`. No drop shadow, no scrim.
5. One drawer per trigger; opening a second closes the first.

**Violations**

- Drawer not anchored to its trigger — error
- Trigger-to-drawer gap not 4px — warning
- Corner radius not 4px (`--radius-default`) — error
- Visible arrow or tether pointing at the trigger — warning (popover behaviour, not drawer)

**Examples**

✓ A *Country* Dropdown near the viewport bottom — drawer flips above the trigger.

✗ A drawer that opens at a fixed page position regardless of where the trigger sits.

---

## Rule: Positioning and collision

**Description**

The drawer aligns its left edge with the trigger's left edge. Its width is set by content, not by the trigger. When the drawer would extend past the viewport edge, it shifts to fit with 8px breathing room.

**How to Apply**

- Drawer's left edge aligns with the trigger's left edge.
- Drawer width is set by content, bounded by `min-width: 100px` and `max-width: 500px` (per *Width and overflow*). Not stretched to the trigger.
- When the drawer would extend past the viewport's right edge, shift left until 8px from the edge.
- After shifting, the drawer must still horizontally overlap its trigger; if not, the surrounding layout is the problem.
- Tripletex ships Norwegian and English only (LTR); RTL is out of scope.

**Violations**

- Drawer extends past or touches the viewport edge — error
- Drawer shifted so far it no longer overlaps its trigger — error
- Drawer stretched to match trigger width — warning

**Examples**

✓ A trigger 60px from the right viewport edge — drawer shifts left to fit, still overlapping the trigger.

✗ Drawer clips at the viewport edge instead of shifting.

---

## Rule: Visual treatment

**Description**

Drawers are flat and silent: no shadow, no scrim, no motion. They appear and disappear instantly. The page beneath stays at full opacity and remains interactive (clicking outside dismisses the drawer).

**How to Apply**

- 1px `--border-primary` border defines the drawer's edge. No drop shadow, no blur, no other elevation cue. The border is accessibility-critical: with no shadow and no overlay, it's the only thing defining the drawer's edge for users with low vision.
- No scrim on surrounding content. The page stays at full opacity and remains interactive.
- No motion. Atlas has not specified motion tokens; drawers must not invent their own.

**Violations**

- Drop shadow, blur, or other elevation cue — error
- Scrim or overlay on surrounding content — error
- Open or close animation (fade, scale, slide) — error
- Outer border using anything other than `--border-primary` — error
- No border at all — error

**Examples**

✓ A *Country* Dropdown opens; the form, header, and sidebar remain readable behind the drawer.

✗ A drawer with a drop shadow and 50% page dim — that's modal treatment.

---

## Rule: Width and text overflow

**Description**

Width is set when the drawer opens and stays constant. Text exceeding the width truncates with an ellipsis. Wrapping is forbidden.

**How to Apply**

- Set `min-width` and `max-width` explicitly. `min-width` ≥ 100px; `max-width` ≤ 500px (wider belongs in Combobox or Modal).
- Width stays constant after opening — async loads, scrolling, and content changes happen inside the existing width.
- Long row labels truncate with `…`; no wrapping.

**Violations**

- No explicit `min-width` / `max-width` — error
- `min-width` below 100px or `max-width` above 500px — error
- Drawer width changes mid-open as content arrives — warning
- Row label wraps to a second line — warning

**Examples**

✓ A *Country* drawer at 240px stays at 240px as 195 options stream in; `United States of America` truncates to `United States of Ameri…`.

✗ A drawer that grows from 200px to 320px as async results arrive — every option causes a layout shift.

---

## Rule: Scroll behaviour

**Description**

The drawer caps at the available space between its trigger and the viewport edge, minus 8px. Content exceeding that height scrolls vertically inside the drawer.

**How to Apply**

- Max-height = available vertical space between the trigger and the viewport edge − 8px (following Material's "menu fits available space" pattern). No fixed pixel cap.
- The 8px viewport breathing room is preserved at the cap.
- The drawer's outer surface stays at the cap; only the inner list scrolls.
- Group labels are not sticky during scroll (per-design opt-in).
- Horizontal scroll is forbidden — text truncates instead (per *Width and overflow*).

**Violations**

- Drawer touches or extends past the viewport edge — error
- Fixed-pixel max-height that ignores the viewport — error
- Horizontal scrollbar — error
- Drawer chrome grows in height as content arrives — warning
- Sticky group labels by default — warning

**Examples**

✓ A *Country* drawer with 195 options on a short laptop viewport — drawer flips above the trigger and caps at the available space minus 8px; rows scroll internally.

✗ A drawer hard-coded to `max-height: 400px` that overflows a 500px viewport.

---

## Rule: Row content

**Description**

A row is text-only, text + 20px leading icon, or text + 20px leading avatar — optionally with a smaller secondary description below the primary label. All rows in a drawer must align their labels horizontally.

**How to Apply**

- Three row variants: text-only, text + icon (20px), text + avatar (20px). Prefer one variant per drawer.
- 8px gap between the leading icon/avatar and the label.
- Optional secondary description: smaller text below the primary label, in `--text-muted`, informational only (not separately selectable). When used, all rows in the drawer should follow the same pattern.
- **Alignment**: if any row in a drawer has a leading icon or avatar, all other rows must either have one too or reserve the same left offset. Labels never jump horizontally between rows.

**Violations**

- Row labels jumping left and right within the same drawer — error
- Row icon not 20px — warning
- Mixed icon-and-avatar rows in the same drawer without a strong content reason — warning
- Icon-only row (no label) — warning

**Examples**

✓ A *Country* drawer with all rows showing a flag icon + country name; a *"Show all"* row at the bottom has no icon but reserves the left offset so its label aligns with the others.

✗ A drawer where *Norway* has a flag icon and *Sweden* doesn't, with *Sweden*'s label starting where *Norway*'s flag starts.

---

## Rule: Row states

**Description**

Rows have four states: default, hover, selected (single-mode only), and disabled. Selected rows show a trailing checkmark. Disabled rows render at reduced contrast, carry a tooltip explaining why, and are skipped by keyboard navigation. Keyboard focus uses the standard focus-ring token from `foundations/colors.md` — must be distinct from hover.

**Selected (single-mode only):**

- Trailing checkmark on the right; row background unchanged.
- Only one row selected at a time.
- Multi-mode pickers use checkboxes instead (per `forms/dropdown.md` *Single vs multi mode*).

**Disabled:**

- Reduced-contrast text per the Figma library.
- Not focusable by keyboard — arrow keys skip them.
- Tooltip required, explaining why and how to enable.
- `aria-disabled="true"` on the accessible element.

**Soft-dependency rows:** When a Dropdown / Combobox is downstream of another picker with a soft dependency (all options exist; only some are valid given the upstream — e.g. all tax codes exist, only some apply per product), the drawer can show non-relevant rows as disabled with per-row tooltips. See `patterns/dependent-pickers.md` for the filter-vs-disable decision by cardinality.

**Violations**

- Single-mode drawer with multiple selected rows — error
- Selected shown via background highlight instead of trailing checkmark — warning
- Disabled row still focusable by keyboard — error
- Disabled row without a tooltip — warning
- Disabled row still interactive on click — error

**Examples**

✓ A *Currency* drawer with *NOK* and *EUR* selectable, *USD* greyed out with *"USD is unavailable — contact your administrator to enable foreign currencies."* Arrow keys skip *USD*.

✗ User clicks a greyed-out row and it selects anyway.

---

## Rule: Grouping

**Description**

When grouping helps the user scan (countries by continent, customers by relationship), use a 1px divider between groups and a non-interactive label above each.

**How to Apply**

- 1px horizontal divider between groups using the internal divider colour token from `foundations/colors.md` (lighter than the outer `--border-primary`). The two must not be swapped — see *Visual treatment*.
- Group label uses `--text-muted` and the small/caption type size from `foundations/typography.md`. Non-interactive — not focusable, not clickable, no hover state.
- Group labels align horizontally with option labels (same indent, including any reserved icon/avatar offset).
- 2–6 groups is typical. More than that suggests search instead (per `forms/dropdown.md` *Search-in-drawer threshold*).

**Violations**

- Group label rendered with the same weight/colour as option labels — warning
- Group label that's interactive — error
- Groups without dividers — warning
- Empty group (zero options) — error
- More than ~8 groups in one drawer — warning

**Examples**

✓ A *Country* drawer grouped by continent: *Europe* label (lighter), divider, European countries; divider, *Asia* label, Asian countries.

✗ A *Country* drawer where the *Europe* group label is styled the same as country names — looks selectable, isn't.

---

## Rule: Empty state

**Description**

A drawer must always have content when it first opens. If the picker has nothing to render, its trigger is disabled and the drawer never opens (see the consuming component's *Disabled trigger when no content to show*). The only legitimate drawer empty state is **user-initiated**: a search query that filters to zero, or a selection that empties the visible list. In that case the drawer stays open and shows an illustration + Text Vault message.

**How to Apply**

- Drawer stays open at its current width on user-initiated empty.
- Search input stays visible at the top so the user can clear or refine.
- Render in the option-list region:
  - A 100×100 illustration of type `search` from the Atlas illustration library, centred horizontally.
  - A Text Vault key below the illustration. Wording varies by cause (*"No matches for [query]"* for search; *"All available items selected"* for selection-driven). Owned by Text Vault.
- **Combobox create-new exception**: when create-new is enabled, a typed query with no matches renders the create-new affordance as a normal row (e.g. *"Create new customer 'Acme'"*) instead of the empty state. The illustration only shows when there are zero matches *and* create-new isn't offered.
- Every search-enabled drawer must implement this empty state.

**Trigger-disabled cases (not drawer empty state):** initial empty data, async fetch returned zero at open time, surrounding context not ready. The drawer never opens — see the consuming component's *Disabled trigger when no content to show*.

**Violations**

- Drawer opens to an empty option list with no user action involved — error
- Drawer closes silently when a user action filters the list to zero — error
- Empty state hides the search input — error
- Empty state without the 100×100 `search` illustration or without the Text Vault message — error
- Illustration at a size other than 100×100 — warning
- Illustration of a type other than `search` — warning
- Hard-coded message instead of a Text Vault key — note
- Combobox with create-new showing the illustration instead of a create-new row — warning

**Examples**

✓ User types `xyz` into a *Country* Dropdown's search; drawer stays open, search visible at top, option-list region shows the 100×100 illustration above *"No matches for 'xyz'"*.

✓ A *Tags* multi-Dropdown on a new account: trigger is disabled with *"No tags yet — add tags in Settings"*. The drawer never opens.

✗ A *Tags* Dropdown trigger renders enabled, user clicks, drawer opens to *"No tags yet"* — the trigger should have been disabled.

---

## Rule: Async loading

**Description**

When the option list loads asynchronously, the drawer renders skeleton rows matching the expected row shape. Spinners are a fallback, flagged as a warning because they communicate less than skeletons. Loading is distinct from empty — the empty-state illustration must not appear during in-flight fetches.

**How to Apply**

- Render 3–5 skeleton rows in the option-list region. Skeletons match the expected row anatomy (text-only / text+icon / text+avatar) — if rows will have leading icons, the skeletons reserve those slots.
- The drawer's width, border, and position stay locked during loading. Only the option-list region changes.
- Real options replace skeletons in place when the fetch resolves. No layout shift.
- Search input stays visible during loading.
- **Spinner fallback**: when row shapes are wildly variable, a single centred spinner in the option-list region is acceptable but a warning. Document the choice per-component.
- For fetches that resolve under ~200ms, the loading indicator may be skipped. (Threshold owned by `patterns/loading-states.md` once it lands.)

**Violations**

- 100×100 empty-state illustration shown while a fetch is in flight — error
- Drawer chrome resizes when loading finishes — error
- Search input hidden during loading — error
- Spinner used when skeleton rows would be feasible — warning
- Skeleton rows that don't match the expected row anatomy — warning
- Drawer fills the entire scrollable region with skeletons (50+) — warning

**Examples**

✓ A *Customer* Dropdown opens; drawer renders 4 skeleton rows shaped like the expected rows (avatar + two text bars). 600ms later real rows replace skeletons in place.

✓ User types `acm` in a *Country* search; previous filtered results dim, 3 skeleton rows appear, results arrive and replace.

✗ A *Customer* Dropdown opens; drawer shows *"No matches"* illustration because real options haven't arrived yet.

---

## Rule: Z-stacking

**Description**

A drawer's z-index is one above its trigger. Anything stacked above the trigger covers the drawer too. A surface that opens above the trigger while the drawer is open counts as a click outside the drawer and dismisses it.

**How to Apply**

- Drawer z-index = trigger z-index + 1.
- A surface that opens above the trigger (modal, notification, popover from outside the drawer) dismisses the drawer.
- A drawer opened from a control inside a modal stacks above the modal's content (its trigger sits inside the modal).
- A modal opening while a page-level drawer is open stacks above that drawer's trigger and dismisses the drawer.
- Notifications and toasts always sit on top.
- Two drawers from the same trigger cannot be open at once — opening a second closes the first.

**Violations**

- Drawer rendered behind or below its trigger in the stack — error
- Drawer staying open when a surface opens above its trigger — error
- A modal opening while a page-level drawer stays open — error
- Notification rendered behind a drawer or modal — error
- Two drawers from the same trigger open at once — error

**Examples**

✓ User opens an "Edit invoice" modal containing a *Customer* Dropdown; the drawer stacks above the modal's form content because its trigger sits inside the modal. A notification fires top-right and renders above both.

✗ A page-level filter Dropdown's drawer is open; a background modal opens over the trigger — the drawer should have dismissed.

✗ A Dropdown inside a modal is opened and its drawer renders behind the modal.

---

## Rule: Outside-click and Esc dismissal

**Description**

A drawer dismisses on outside-click or Esc, without changing the value. Selecting an option dismisses in single mode; multi mode dismisses only via outside-click, Esc, or an explicit *Done* affordance.

**How to Apply**

- Outside click anywhere outside the drawer dismisses it. Focus returns to the trigger.
- Esc dismisses the drawer. Focus returns to the trigger.
- Page scroll does not dismiss the drawer by default (per-component opt-in if needed).

**Violations**

- Drawer that doesn't close on outside-click — error
- Drawer that doesn't close on Esc — error
- Drawer that auto-closes on page scroll without an explicit design reason — warning

**Examples**

✓ User opens a *Country* Dropdown, decides to check something in the page header instead, clicks the header — drawer closes, focus returns to the trigger.

✗ A drawer that requires the user to explicitly click a *"Close"* button.

---

## Rule: Keyboard navigation

**Description**

Keyboard users must reach every drawer state without leaving the keyboard. ARIA roles are set by the consuming picker (the drawer is a generic surface).

**ARIA roles set by the consuming component:**

- `role="listbox"` (with `role="option"` on rows) for Select and Dropdown.
- `role="menu"` (with `role="menuitem"` on rows) for action menus.
- `role="combobox"` on the trigger linked via `aria-controls` / `aria-expanded` for Combobox.

Rows expose the standard ARIA selection / disabled attributes (`aria-selected`, `aria-disabled`).

**How to Apply**

| Key | Behaviour |
|---|---|
| `Arrow Down` / `Arrow Up` | Next / previous interactive row (skips group labels) |
| `Home` / `End` | First / last interactive row |
| `Esc` | Close; focus returns to the trigger |
| Type a letter | Type-ahead to the first row starting with that letter; repeated letters cycle matches |

Selection keys (`Space`, `Enter`) differ between single and multi mode — defined in the consuming picker.

When the drawer has a search input, focus lands in the search input on open; arrow keys move from the search into the rows.

**Violations**

- Arrow keys focusing group labels — error
- Esc not closing the drawer — error
- Type-ahead not implemented — warning
- Focus returning to the wrong element on close — warning

**Examples**

✓ User Tabs to a *Country* Dropdown, opens with Space, presses Down repeatedly, skips the *Europe* group label, picks *Sweden* with Enter.

✗ Arrow Down lands focus on the group label and treats it as selectable.

---

## Related Rules

- `forms/dropdown.md` — picker-specific behaviour (single vs multi mode, search-in-drawer threshold, trigger placeholder, keyboard semantics).
- `forms/combobox.md` — typeable-trigger picker; uses the drawer for autocomplete suggestions.
- `forms/select.md` — single-pick picker; uses the drawer in its simplest configuration.
- `design-rules/components/modal.md` — *Modal stack order* cross-refs *Z-stacking* here.
- `patterns/dependent-pickers.md` — chained-picker flows; cross-component coordination.
- `patterns/popover-usage.md` — tooltips and popovers (separate surfaces from drawers).
- `patterns/loading-states.md` *(pending)* — cross-Atlas skeleton-vs-spinner decision.
- `design-rules/components/skeleton.md` *(pending)* — canonical skeleton-row component.
- `design-rules/foundations/colors.md` — `--border-primary` (outer edge), internal divider token (groups), `--text-muted` (group labels and secondary descriptions), focus-ring token (row focus).

---

## Open Questions

- **Sticky group labels** — currently per-design opt-in. Worth a team-decision pass once 2–3 grouped drawers are in production.
- **Drawer width tokens** — `--drawer-min-width` and `--drawer-max-width` would replace the inline 100px / 500px values. Coordinate with Astro.
- **Skeleton row tokens** — `--skeleton-*` (or equivalent) for the async-loading rule. Coordinate with Astro.
- **Loading time threshold** — the ~200ms default in *Async loading* is a placeholder; confirm against `patterns/loading-states.md` when that lands.
- **Motion tokens** — Atlas has no motion tokens yet, which is why drawers are silent. Revisit once Atlas defines them.


---

## components/expandable-table.md

# Expandable Table Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Expandable Table component — expand/collapse behavior, nested row structure, and indentation.

---

## components/labels.md

# Label Rules

> **Status: DRAFT — pending team review.**

A Label is a small pill-shaped indicator marking the *type* or *purpose* of something — primarily at the top of every banner, also in cards or sections. Labels are a constrained variant of Chip: always pair a fixed icon with fixed text and colour from one of the nine canonical types defined below in *Type and colour mapping*. For where labels appear inside banners, see [`banner.md`](banner.md).

**Figma reference:** [Atlas Library — Labels](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=6569-2215&t=DEKm0jloX2sZhgZk-11)

---

## Rule: Label anatomy

**Description**

Every label is a 24px-tall pill with rounded ends, a coloured background, no border, an icon on the left, and the type's text on the right in the primary text colour.

**How to Apply**

- Height: 24px.
- Shape: pill (fully rounded ends, **no border**).
- Background: a `--surface-{state}-{level}` token mapped to the label's type (see *Type and colour mapping* for the per-type token; labels are non-interactive so `-rest` / `-hover` levels don't apply — the canonical `-level` per Figma is in Open Questions).
- Icon: **20px** (`--icon-size-small`), `--text-primary` colour, fixed per type, on the left. Comes from the Atlas icon library — see [`foundations/icons.md`](../foundations/icons.md). The specific Atlas icon per type isn't yet documented — see Open Questions.
- Text: to the right of the icon, in `--text-primary`.
- Internal padding centres icon and text vertically; consistent horizontal padding across all types.

**Violations**

- Label height other than 24px — warning
- Label icon size other than 20px (`--icon-size-small`) — error
- Label icon colour not `--text-primary` — error
- **Label with a border — error**
- Label without an icon — warning
- Label without text — error
- Label background not from the `--surface-{state}-{level}` family (raw hex or other tokens) — error
- Label background token's `{state}` mismatched to the label's type (e.g. `--surface-info-*` on a Done label) — error
- Label background using a `-rest` or `-hover` level (labels are non-interactive) — error
- Label text not using `--text-primary` — warning

**Examples**

✓ A 24px pill, blue background, info icon on the left, *Info* text on the right.

✗ A 32px pill with a red background and custom *Warning* text.

✗ A label rendered as text-only with no pill background.

---

## Rule: Type and colour mapping

**Description**

Labels support nine canonical types. Each type has a fixed text, a fixed icon, and a fixed background colour — picking a type picks everything else. The mapping is canonical; `banner.md` references it rather than duplicating.

**How to Apply**

| Type | Colour | Background token | Use it for |
|---|---|---|---|
| **Info** | blue | `--surface-info-{level}` | Deadlines, system information, webinars |
| **Help** | blue | `--surface-info-{level}` | How-to guides, support articles, AI assistant |
| **Tips** | blue | `--surface-info-{level}` | General advice, relevant features, alternative products that save time or money |
| **News** | blue | `--surface-info-{level}` | Feature updates, general product changes, new functionality |
| **Get started** | blue | `--surface-info-{level}` | Assistive information for new users, tutorials |
| **Automated** | purple | `--surface-automation-{level}` | Available or active automations |
| **Done** | green | `--surface-success-{level}` | System feedback for success |
| **Attention** | yellow | `--surface-warning-{level}` | Warn the user about a potential error or risky action |
| **Error** | red | `--surface-error-{level}` | System feedback for an error (must include recovery info) |

The five blue types (Info, Help, Tips, News, Get started) share the same colour; their icon and text distinguish them.

**Violations**

- Label type outside the nine documented types — error
- Background token's `{state}` mismatched to the label's type (e.g. `--surface-success-*` on a Tips label, or `--surface-info-*` on a Done label) — error
- Background using a raw hex value, a global palette token, or any token outside the `--surface-{state}-{level}` family — error
- Custom icon used instead of the type's canonical icon — error
- Two labels of the same type using different `{level}` variants across the product (one uses `-rest`, another uses `-highlight`) — error

**Examples**

✓ A purple *Automated* label with the automation icon, used inside a card to mark the section as automated.

✗ A green label with *Tips* text — green is for *Done*.

✗ A custom *Premium* type — outside the nine. Reframe to fit a canonical type or use a Chip.

---

## Rule: When to use Label vs Chip vs Status

**Description**

Three components occupy a similar visual space: **Labels** are for *type* (nine canonical kinds), **Status** is for *state* (paid / pending / failed), **Chips** are for tags or filters (custom content, often interactive).

**How to Apply**

Decision tree:

1. Does the indicator fit one of the nine canonical types? → **Label**.
2. Does the indicator show the *state* of an entity (often in a table, list, or detail header)? → **Status** (see [`status.md`](status.md) *(pending)*).
3. Otherwise — custom text, interactive, or a tag / filter? → **Chip** (see [`chip.md`](chip.md) *(pending)*).

**Violations**

- Chip used where a canonical Label type would fit — warning (loses the consistency benefit)
- Label-shaped element with a custom (non-canonical) type — error (use a Chip)
- Status component used for a categorical type (e.g. *Info*, *Tips*) — warning (Status is for state, not type)

**Examples**

✓ A banner about a deadline uses the *Info* Label.

✓ A filter chip *"Last 30 days"* with a removable × — Chip, not Label.

✓ An invoices-table row with *Paid* / *Overdue* indicators — Status, not Label.

✗ A custom *Beta* pill styled like a label but with a non-canonical type — use a Chip.

---

## Related Rules

- [`banner.md`](banner.md) — primary use site; *Banner labels and colour mapping* references this file's mapping.
- [`chip.md`](chip.md) *(pending)* — flexible cousin (custom content, optional interactivity).
- [`status.md`](status.md) *(pending)* — entity *state* indicators, distinct from labels.
- [`patterns/icon-usage.md`](../../patterns/icon-usage.md) *(partial)* — icon-to-action mappings; label icons part of this work.

---

## Open Questions

- **Where outside banners are labels valid?** Working hypothesis: mostly banners, optionally inside cards to mark a section's purpose. Confirm whether cards, list items, section headers, empty states, or elsewhere are also valid.
- **Is 24px the only height?** Compact contexts (table cells, dense lists) might want smaller. Confirm: one size, or default + small?
- **Canonical icon per type** — the nine types imply icons but the specific Atlas icon per type isn't documented. Part of the icon-to-action work tracked in [`patterns/icon-usage.md`](../../patterns/icon-usage.md).
- **Background token level** — labels are non-interactive so `-rest` / `-hover` are out. Confirm against Figma whether labels use `-highlight` (pale) or `-active` (vivid) and replace the `{level}` placeholder in *Type and colour mapping* and the violations with the concrete suffix.
- **Yellow Attention contrast** — yellow backgrounds with primary-colour text can fall below WCAG AA on lighter palettes. Verify the exact tokens used.
- **Are labels ever interactive?** Default assumption: no — interactivity belongs to chips. Confirm.


---

## components/modal.md

# Modal Rules

A modal appears over other content to focus the user's attention exclusively on a single task or important message. It interrupts the user and demands an action — appropriate when the user's attention needs to be directed toward information that must be addressed before continuing.

In Tripletex, modals are used to show complex information that lives elsewhere on the page, to let users edit complex data (for example user details, comments, details views, or flow steps), and to surface critical warnings.

A modal is **not a dialog**. Dialogs are a separate surface; their rules are out of scope of this file.

For *when* to use a modal versus an alternative (inline edit, inline-editable table rows, drawer, banner, notification), see [`modal-usage.md`](../../patterns/modal-usage.md). For what happens to user-entered data when a modal is closed, see [`state-preservation.md`](../../patterns/state-preservation.md).

**Figma reference**: [Atlas Library — Modal](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=105-21232&t=a5rsetCbVeluqKNi-11)

---

## Rule: Modal anatomy

**Description**

Every modal uses the same structure: an optional illustration at the top, then a required title, an optional description, the content body, and an optional button group. A close button always sits in the upper-right corner, outside the vertical stack. Content is left-aligned.

**How to Apply**

The modal is centered in the viewport with the backdrop dimming the rest of the page. Visual specs (backdrop colour, modal background, corner radius, type, text colour) come from the Atlas Library in Figma — Figma is the source of truth for those values per decision #38.

Vertical stack inside the modal, top to bottom, all left-aligned:

1. **Illustration** (optional) — top of the modal, 100×100
2. **Title** (required)
3. **Description** (optional) — short supporting text below the title; this is also the slot for additional information and status fields that belong with the title rather than in the modal body.
4. **Content** — the modal body
5. **Button group** (optional) — see "Modal footer button group" below

The **close button** is required and sits in the upper-right corner of the modal, outside the vertical stack. It is a Tertiary icon button per [`buttons.md`](buttons.md) and carries a "Close" tooltip per [`popover-usage.md`](../../patterns/popover-usage.md).

**Violations**

- Modal without a title — error
- Modal without a close button — error
- Close button placed somewhere other than the upper-right corner — error
- Content not left-aligned — warning
- Modal styling that diverges from the Atlas Library Figma specs (backdrop, surface, radius, type, colour) — warning (Figma is the design SOT per decision #38)

**Examples**

✓ Correct: An "Edit user details" modal with the user's avatar illustration on top, the title "Edit user details", no description, a form in the content area, and a footer with `[Save] [Cancel]`. Close `[✕]` in the upper-right corner.

✗ Wrong: A modal with the title centered above centered body text — anatomy is right but content alignment is wrong.

✗ Wrong: A modal with no close button, relying only on a backdrop click.

<!-- Link to Figma: [Atlas Library — Modal](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=105-21232&t=a5rsetCbVeluqKNi-11) -->

---

## Rule: Modal sizing

**Description**

A modal is wide enough to let its body content break naturally and narrow enough to feel like a focused surface, not a page replacement. Atlas does not enforce a fixed set of named sizes — width is chosen to fit the content. There is a hard minimum and a hard rule for the full-screen edge case.

**How to Apply**

- **Minimum width**: 400px
- **Comfortable maximum**: chosen so body text and form fields break across at least two rows and don't visually rush across the screen
- **Above 800px**: generally fine when the content genuinely needs the room
- **Full-screen modals**: when a modal occupies essentially the full viewport, leave at least **24px** between the modal edge and the viewport edge on every side

**Violations**

- Modal width below 400px — error
- Full-screen modal with less than 24px between modal and viewport edge on any side — error
- Modal sized so wide that body text reads as a single very long line — warning

**Examples**

✓ Correct: A comment modal at 480px wide so the placeholder text wraps across two lines.

✓ Correct: A complex multi-section "Edit company settings" modal at 880px wide.

✗ Wrong: A 320px modal containing a form — fields are crushed.

✗ Wrong: A near-full-screen modal that touches the top and bottom of the viewport with no margin.

<!-- Link to Figma: [Atlas Library — Modal](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=105-21232&t=a5rsetCbVeluqKNi-11) -->

---

## Rule: Modal dismissal

**Description**

A modal can be dismissed three ways: the close button in the upper-right corner, a click on the backdrop outside the modal, or the Esc key. All three preserve the user's in-progress data per [`state-preservation.md`](../../patterns/state-preservation.md).

**How to Apply**

1. The close button (upper-right) is always present and always works.
2. A click on the backdrop dismisses the modal.
3. Pressing Esc dismisses the modal.
4. All three paths trigger the same dismissal behaviour and preserve data per [`state-preservation.md`](../../patterns/state-preservation.md).

For the optional explicit Cancel button in the footer, see "Modal footer button group" below.

**Violations**

- Modal without a close button — error
- Modal that ignores Esc — error
- Modal that ignores backdrop click — error
- Dismissal paths that lose user-entered data — error (see [`state-preservation.md`](../../patterns/state-preservation.md))

**Examples**

✓ Correct: User has typed half a comment, clicks the backdrop; modal closes; user re-opens the same modal; the half-comment is restored.

✗ Wrong: Esc inside a modal does nothing.

✗ Wrong: Backdrop click is suppressed because the modal is "important" — the close icon already covers that need; backdrop must always work too.

---

## Rule: Modal keyboard interactions

**Description**

Three keys carry meaning inside an open modal: Esc dismisses, Enter submits, and Cmd / Ctrl + Enter is the submit binding inside multi-line textareas. Tab and Shift+Tab navigation within the modal are governed by the focus-management foundation when it lands; this rule covers only the action keys.

**How to Apply**

1. **Esc** dismisses the modal, preserving state per [`state-preservation.md`](../../patterns/state-preservation.md). (Documented separately in "Modal dismissal" above; restated here for completeness.)
2. **Enter** in a single-line input fires the modal's primary action, after any field-level validation runs.
3. **Cmd / Ctrl + Enter** in a textarea fires the modal's primary action. Plain Enter inside a textarea inserts a newline; it never triggers the primary action.
4. If the primary action is disabled because an async commit is already in flight, Enter and Cmd / Ctrl + Enter do nothing.
5. If the modal has no primary action (info-only modals with just a Close button), Enter does nothing.
6. **The primary action is never disabled as a validation gate.** Submit stays enabled regardless of whether required fields are filled. Clicking submit on a form with invalid input opens the validation summary per [`validation-feedback.md`](../../patterns/validation-feedback.md) — it never silently no-ops. The only legitimate reason to disable the primary action is an in-flight async commit (point 4 above). This aligns Atlas with WCAG guidance: a disabled submit removes the user's path to discover *what's wrong*, and that's the validation surface's job. The cross-DS landscape on this position is captured in decision #52 in `PROJECT_STATUS.md`.

**Violations**

- Esc inside a modal does nothing — error
- Enter in a single-line input does not trigger the primary action — error
- Plain Enter in a textarea triggers the primary action instead of inserting a newline — error
- Cmd / Ctrl + Enter in a textarea does not trigger the primary action — error
- Enter triggers a disabled primary action (during an in-flight async commit) — error
- Primary action disabled because required fields aren't filled — error (validation-gate disabling is forbidden; surface the validation summary instead, per [`validation-feedback.md`](../../patterns/validation-feedback.md))

**Examples**

✓ Correct: Inside a "New customer" modal, the user fills in the Name field and presses Enter — the modal submits.

✓ Correct: Inside the comment modal, the user types two lines (plain Enter inserts a newline) and presses Cmd+Enter to submit.

✗ Wrong: Plain Enter inside the comment modal's textarea triggers Save instead of inserting a newline.

✗ Wrong: A required field is empty, so the primary action is greyed out — disabled-as-validation-gate is forbidden. Submit must stay enabled and surface the validation summary on click, per [`validation-feedback.md`](../../patterns/validation-feedback.md).

✗ Wrong: An async commit is in flight (the primary action is showing its spinner state) but pressing Enter triggers a duplicate submit.

---

## Rule: Modal isolation

**Description**

A modal isolates itself from the page in three ways: it stays inside the viewport, it locks the page beneath it (no scroll, no interaction), and it manages its own overflow internally. Together, this makes the modal the only active surface on screen until it closes.

**How to Apply**

1. **Modal stays within the viewport.** Combined with the sizing rule's full-screen ≥24px viewport-edge minimum, a modal grows up to its comfortable maximum and stops; it never extends past the screen.
2. **Page beneath is scroll-locked and interaction-locked.** While the modal is open, the underlying page does not scroll, and elements behind the modal cannot be clicked, hovered, or activated by mouse, touch, or keyboard. Tab order skips elements behind the modal. (Full focus-trap semantics will be defined when the Atlas focus-management foundation lands — see `TODO.md`.)
3. **Vertical overflow inside the modal: scroll.** If content is taller than the modal, the modal's content area scrolls vertically. No part of the modal is sticky — title and footer scroll along with the content.
4. **Horizontal overflow inside the modal: reflow.** If content is wider than the modal, reflow it (wrap text, stack columns, break grids). Horizontal scroll inside a modal is strongly discouraged — fall back to it only when reflow genuinely isn't possible.

**Violations**

- Modal extends past a viewport edge — error
- Page beneath scrolls while the modal is open — error
- Page content behind an open modal can be clicked, hovered, or activated — error
- Modal content exceeds modal height with no internal scroll — error
- Horizontal scroll inside a modal without first attempting to reflow — warning
- Title or footer kept sticky during vertical scroll — warning

**Examples**

✓ Correct: A tall "Edit company settings" modal scrolls inside its content area; the title scrolls out of view as the user reads further down. The page beneath stays fixed.

✓ Correct: A modal containing a wide table reflows the columns by wrapping or stacking them; no horizontal scrollbar appears.

✓ Correct: A user keyboard-tabs while a modal is open and the focus stays inside the modal — buttons and links on the underlying page are skipped.

✗ Wrong: A modal so tall that its title is clipped at the top of the viewport.

✗ Wrong: A 500px-wide modal whose grid scrolls horizontally because reflow wasn't attempted first — stack or wrap the columns where you can; only scroll horizontally as a last resort.

✗ Wrong: User scrolls the page behind an open modal and the page moves.

✗ Wrong: User clicks a link visible behind the modal backdrop and the link activates.

✗ Wrong: A modal pins its footer at the bottom while the body scrolls — Tripletex modals don't use sticky regions.

---

## Rule: Modal stack order

**Description**

The modal sits above page content and below notifications. Drawers (per [`drawer.md`](drawer.md)) follow their trigger: a drawer opened from a control inside the modal stacks above the modal's content; opening a modal above a page-level drawer dismisses the drawer. Side panels (PDF viewer, in-app chat, AI Assistant) are layout-level surfaces — see [`../foundations/layout.md`](../foundations/layout.md) *(pending)*. Modal-on-modal stacking is governed by the never-stack rule in [`modal-usage.md`](../../patterns/modal-usage.md).

**How to Apply**

From bottom to top:

1. Page content.
2. Modal.
3. Drawers opened from inside the modal (per `drawer.md` *Z-stacking*).
4. Popovers and tooltips anchored inside the modal.
5. Notifications and toasts (always on top).

**Violations**

- Drawer opened from inside the modal rendering behind the modal — error
- Page-level drawer staying open when a modal opens — error
- Notification rendered behind a modal — error
- Popover inside the modal rendering above a notification — error
- Two modals open at once — error (also covered by [`modal-usage.md`](../../patterns/modal-usage.md))

**Examples**

✓ User opens an "Edit invoice" modal containing a *Customer* Dropdown; the drawer stacks above the modal. A notification fires top-right and renders above both.

✗ A Dropdown inside a modal opens and its drawer renders behind the modal.

---

## Rule: Modal footer button group

**Description**

A modal can have many buttons but only one primary. The footer button group sits below the content and follows the standard alignment rules from [`button-placement.md`](../../patterns/button-placement.md). In modals, buttons are mostly left-aligned, so the order reads primary → secondary → tertiary left to right per the shared alignment principle — Tertiary sits at the right end of the left-aligned group.

There is one exception: when the modal contains a multistep form with a stepper, the **Next** and **Previous** buttons may be right-aligned. They are the only buttons that may sit outside the alignment of the rest of the group.

When the modal contains a form or any user-mutable state, an explicit **Cancel** button is required in the footer. It is the Tertiary button at the right end of the left-aligned group. Modals that show only read-only information may rely on the close icon and backdrop click without a footer Cancel button.

Button text comes from [Text Vault](https://cdn.tripletex.no/text-vault/index.html).

**How to Apply**

1. One primary button maximum, per [`buttons.md`](buttons.md)
2. Group is left-aligned by default; order reads primary → secondary → tertiary left to right (Tertiary on the right end)
3. **Stepper exception**: Next / Previous in stepper modals may be right-aligned, separate from the rest of the group
4. **Cancel required for forms or user-mutable state**: include an explicit Cancel button. Place it as the Tertiary at the right end of the left-aligned group
5. **Cancel optional for read-only modals**: the close icon and backdrop click are sufficient
6. Use Text Vault for button labels

**Violations**

- More than one primary button — error
- Random button order — error
- Cancel placed before primary in a left-aligned modal footer — error
- Form-bearing modal without an explicit Cancel button — warning
- Stepper Next / Previous mixed in with the rest of the button group — warning
- Custom button label that diverges from Text Vault — note

**Examples**

✓ Correct (form-bearing modal): `[Save] [Save Draft] [Cancel]` left-aligned below the content. Save is Primary, Save Draft is Secondary, Cancel is Tertiary.

✓ Correct (stepper modal): `[Cancel]` at the right end of the left-aligned group, with `[Previous] [Next]` right-aligned in the same footer row.

✓ Correct (info-only modal): a single Primary `[OK]` left-aligned, no Cancel button (the close icon suffices).

✗ Wrong: `[Cancel] [Save]` in a left-aligned footer — Cancel before Primary.

✗ Wrong: A modal footer with two primary buttons "for emphasis."

<!-- Link to Figma: [Atlas Library — Modal](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=105-21232&t=a5rsetCbVeluqKNi-11) -->

---

## Rule: Form fields inside a modal

**Description**

Form fields placed inside a modal use **24px vertical** spacing between rows and **12px horizontal** spacing between paired inputs. This keeps modal forms breathable while staying compact enough that the modal doesn't grow unnecessarily tall.

> **Note**: These values are the modal-specific application of a wider form-layout convention. Atlas has no top-level `forms.md` — form spacing is documented per-component for now; revisit once cross-cutting form-layout duplication justifies extraction (see [`forms/input.md`](forms/input.md) Open Questions).

**How to Apply**

- 24px vertical spacing between form rows
- 12px horizontal spacing between paired inputs (e.g. a date-range start/end pair)
- Form-to-button spacing follows [`button-placement.md`](../../patterns/button-placement.md) (16px preferred / 12px minimum / 24px maximum)

**Violations**

- Vertical spacing between form rows other than 24px — warning
- Horizontal spacing between paired inputs other than 12px — warning

**Examples**

✓ Correct: A "Create invoice" modal with form rows separated by 24px and a date-range pair separated by 12px.

✗ Wrong: 16px between rows because the modal "felt too tall."

---

## Rule: Errors render inline

**Description**

When a field or action in a modal produces an error, the error renders inline within the modal body — adjacent to the field that caused it for field-level errors, or as an inline alert at the relevant point in the body for action-level errors. Errors do not appear as a banner above the modal or as a notification, because the modal already has the user's full attention.

**How to Apply**

1. Field-level error: render adjacent to the field, per the validation feedback pattern ([`validation-feedback.md`](../../patterns/validation-feedback.md))
2. Action- or modal-level error: render as an inline alert at the relevant point in the body
3. Never use a banner inside a modal (banners are forbidden inside modals, per [`banner.md`](banner.md))

**Violations**

- Banner used inside a modal to display an error — error (see [`banner.md`](banner.md))
- Notification fired for an in-modal error — error
- Error message rendered outside the modal — error

**Examples**

✓ Correct: A required field shows "This field is required" directly below it.

✓ Correct: A failed save in a modal shows an inline alert above the footer: "Save failed — please try again."

✗ Wrong: A red banner appears at the top of the page behind the modal saying "Invalid input."

---

## Rule: Async commit behaviour

**Description**

When the user triggers an async commit (e.g. clicks Save and a network request is in flight), the modal stays dismissable through all three dismissal paths. On success, the user receives a Notification. If the modal is dismissed mid-commit and the in-flight work is required for the main view to continue, the main view shows a spinner with a brief explanatory note and disables any actions that depend on the in-flight work.

**How to Apply**

1. The action button itself is an Action button per [`buttons.md`](buttons.md) — spinner replaces the label during the commit, with the success / error result states applied as defined there.
2. Dismissal paths (close button, backdrop click, Esc) remain enabled during the spinner state — the user can leave.
3. **On success**: the action button briefly shows its success state per [`buttons.md`](buttons.md), then the modal closes and a Notification appears (top-right, per the existing component) confirming the action. *(The Notification component is being redesigned — see [`notification.md`](notification.md). The post-commit feedback pattern will likely move to a Toast component once that exists; until then, use Notification.)*
4. **If the user dismisses the modal mid-commit and the in-flight work blocks the main view**, the main view displays a spinner with a short message — for example "Saving in the background. Some actions are unavailable until this finishes." — and disables affected actions until the work resolves.
5. **On failure mid-commit**, render the error inline per "Errors render inline" above.

**Violations**

- Modal that locks all dismissal paths during async commit — error
- Modal stays open after a successful commit instead of closing — error
- No success feedback after a successful commit — error
- Main view that becomes unusable after a mid-commit dismissal without surfacing the blocking state — error
- Success feedback rendered inside a modal that has already closed — note

**Examples**

✓ Correct: User clicks Save, the spinner replaces the label, then a green success state, then the modal closes automatically and a Notification appears top-right confirming the action.

✓ Correct: User clicks Save, the spinner replaces the label, the user presses Esc, the modal closes. The save completes shortly after and a Notification appears top-right. The main view never shows a spinner because it wasn't blocked by the async work.

✓ Correct: User clicks Save in a "Lock period" modal and dismisses it mid-commit. The main view shows a spinner with the message "Locking the period. Some actions are unavailable until this finishes." Once it resolves, the spinner clears and a Notification confirms the lock.

✗ Wrong: Modal disables Esc and the close button during async commit — user is stuck waiting.

✗ Wrong: Save succeeds but no Notification ever appears — user has no idea it worked.

---

## Related Rules

- [`modal-usage.md`](../../patterns/modal-usage.md) — when to use a modal vs alternatives, modal stacking, draft persistence
- [`state-preservation.md`](../../patterns/state-preservation.md) — what happens to in-modal data on dismissal vs commit vs navigation
- [`button-placement.md`](../../patterns/button-placement.md) — alignment principle inherited by the modal footer button group
- [`buttons.md`](buttons.md) — Tertiary icon button (close), Action button (async commit), variant rules
- [`banner.md`](banner.md) — banners are forbidden inside modals (so errors render inline)
- [`notification.md`](notification.md) — post-commit success feedback (component being redesigned)
- [`popover-usage.md`](../../patterns/popover-usage.md) — close-button tooltip ("Close")
- [`loading-states.md`](../../patterns/loading-states.md) — when a modal needs to fetch content on open, render a skeleton or spinner inside the modal body — never an empty modal *(not yet documented — see `TODO.md`)*

---

## Out of Scope of This File

- **Dialog** is a separate surface, not a modal variant. Dialog rules are not documented here.
- **AI Assistant Modal** uses a different container with its own rules — see [`ai-assistant-modal.md`](ai-assistant-modal.md). The rules in this file do not apply to that surface.
- **Mobile modal**: a Figma spec exists rendering the modal as a content card on mobile, but the implementation is not shipped and the spec is not yet documented. Mobile behaviour is undefined until both land.
- **Visual grouping inside modal content** (the "different background colour for grouped content" question): pending its own rule. Not documented here.
- **Focus management**: deferred until the Atlas focus-management foundation lands. Modal exposes `onDeactivation` for focus-lock callbacks; the rule for *how* it should behave is to be written separately.


---

## components/notification.md

# Notification Rules

> **Status**: Not yet documented — component needs redesign first. See `TODO.md` for this task.

This file will document rules for the Notification component — a floating top-right element for system messages. The current component is outdated and needs redesign before rules can be finalized.

## Current Behavior (Reference Only)

- Floating position: top-right
- White box with black text
- Auto-dismisses
- Can be manually closed

## Notes

Component redesign should address: visual update, auto-dismiss timing, stacking behavior, and mobile adaptation. See also `patterns/notification-usage.md`.

---

## components/page-header.md

# Page Header Rules

> **Status: DRAFT — pending team review per decision #45.**

The page header is the topmost surface of every product page. It tells the user *where they are*, *what record they're on*, *whether work is being saved*, and *what global actions the page supports*. The header ships in two variants — **Default** and **Compact** — sharing the same slot anatomy. Slots top to bottom: **breadcrumbs** (Default only), **title row**, **metadata row** (sub-heading), and **alert**. Action buttons live inside the title row on the right; their placement is governed by [`patterns/button-placement.md`](../../patterns/button-placement.md) and not restated here.

**Figma references:**

- [Atlas Library — Page Header component](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=6806-3307) — variants, slots, anatomy.
- [Atlas Library — Page Header usage examples](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=12418-51347&t=a5rsetCbVeluqKNi-11) — worked examples of titles and metadata for common page types. The reference for "what should I put in the title and metadata row for this kind of page?"

---

## Rule: Page header is mandatory, topmost, and matches content width

**Description**

Every product page renders a page header. The header is the topmost element on the page (no page-team content above it) and its width matches the content section's width — same left and right edges as the body content.

**How to Apply**

- Render a header on every page (pick Default or Compact per *Page header variants*).
- Nothing the product team owns sits above the header. The Spacesuit topbar (company chooser, search, notifications, user profile) is the only chrome above — that's Spacesuit's territory.
- Header width matches the content section's width: same left edge, same right edge.

**Violations**

- Product page rendered without a page header — error
- Page-team content (banners, callouts, custom navigation) rendered above the page header — error
- Page header narrower or wider than the content section below it — error
- Page header's left or right edge misaligned with the content area's edges — warning

**Examples**

✓ Every page opens with the header at the top, edges aligned with the form / table / card grid below.

✗ An environment banner ("You're in staging") rendered above the page header — it belongs in the alert slot inside the header.

✗ A hero illustration that bleeds past the content edges sits above the page header.

---

## Rule: Page header anatomy

**Description**

The page header has four slots, rendered top to bottom in a fixed order: **breadcrumbs** (Default only), **title row**, **metadata row**, **alert**. Individual slots can be empty; the order never changes.

**How to Apply**

| Slot | Contents |
|---|---|
| 1. **Breadcrumbs** *(Default only)* | Optional; navigate to parent elements. Separator `/` (slash with surrounding spaces). Truncates with `…` under width pressure (never wraps). Standalone breadcrumb component file is pending — until breadcrumbs are exposed outside the page header, this row owns the contract. |
| 2. **Title row** | Page title (Text 2XL Default / Text XL Compact) + Compact-only alert beside title + auto-save indicator right of title + action button group right-aligned. Title truncates with `…` if it exceeds available width (never wraps). |
| 3. **Metadata row** | Object numbers, important details, sub-titles, status components. `--text-muted` colour. 12px spacing. Wraps to a second line under width pressure (never truncates). Always directly under the title in both variants. See *Metadata row contents*. |
| 4. **Alert** *(Default only)* | Alert component (distinct from Banner — see *Alert placement*). Sits below metadata row. Compact alerts sit on the title row instead. Banners do not appear inside the page header. |

The slots stack vertically with no other elements interleaved. Truncation vs wrapping behaviour per slot: title and breadcrumbs **truncate** (preserves the title row's single-line shape); metadata row **wraps** (keeps record identifiers fully readable on narrow screens).

**Violations**

- Slot added that isn't one of the four (e.g. tabs row, search bar) — error
- Slot order other than what the variant permits — error
- Metadata row not directly under the title — error
- Same slot rendered in two places (e.g. alert in both the title row and bottom slot) — error
- Title row split across two lines (action group or auto-save indicator pushed to a separate row from title) — warning
- Title rendered in a typography style other than Text 2XL (Default) or Text XL (Compact) — error

**Examples**

✓ Correct:

```
[Breadcrumbs (optional)]
[Title][Autosave (optional)]                 [Feedback][Send] [⋮]
1234   Acme AS   Due 15.05.26 Status:Sent
[Alert (optional)]
```

✗ Tabs rendered between the title row and metadata row — tabs go below the header, not inside.

✗ Status badge inline with the title *and* in the metadata row.

---

## Rule: Page header variants

**Description**

The page header ships in two variants — **Default** and **Compact** — sharing the same slot anatomy. They differ on breadcrumbs (Default only), title size (Text 2XL vs Text XL), and alert position (bottom slot vs beside title).

**How to Apply**

| Slot | Default | Compact |
|---|---|---|
| Breadcrumbs | Optional, rendered on top | Not rendered |
| Title | Text 2XL | Text XL |
| Auto-save indicator | Title row, right of title | Same |
| Action button group | Title row, right edge | Same |
| Metadata row | Directly under title | Same |
| Alert (when present) | Bottom slot, below metadata row | Title row, beside title |

Use **Default** for top-level and primary detail pages where breadcrumb navigation back to a parent helps. Use **Compact** for pages or panes nested inside a parent context that already provides navigation (embedded sub-views, tab bodies with breadcrumbs in the outer page, settings sub-pages).

**Violations**

- Compact variant rendering breadcrumbs — error
- Default variant rendering Text XL title — error
- Compact variant rendering Text 2XL title — error
- Compact variant on a top-level page with no parent context — warning
- Default variant nested inside a page that already has a Default header (double breadcrumbs) — warning

**Examples**

✓ Invoice detail (reachable from invoice list): Default with breadcrumbs `Fakturaer / 1234`. Sub-pane embedded within: Compact without breadcrumbs.

✗ Compact variant rendered with breadcrumbs.

✗ Default variant on a sub-pane producing a stacked breadcrumb trail.

---

## Rule: Sticky header with scroll-driven variant transition (optional)

**Description**

A Default page header may be made **sticky** so it remains pinned to the viewport top as the user scrolls. When enabled, the header transitions from Default to Compact form on scroll-down and reverts to Default when the user scrolls back to the top. The transition is between the two variants — not a third variant.

**How to Apply**

- Enable sticky-with-transition at the page level (one opt-in per header, not per slot).
- Start in **Default** (full size, breadcrumbs visible, Text 2XL title).
- On scroll past the top: header **pins to the viewport top** and **transitions to Compact** (breadcrumbs hidden, title shrinks to Text XL).
- Compact-on-scroll state has tighter vertical padding and a 1px hairline border-bottom to visually detach the pinned header from scrolling content (specific spacing and border tokens — see *Open Questions*).
- Other slots stay intact across the transition — action buttons, auto-save indicator, metadata row, and alert (if used) remain visible.
- On scroll back to the top: revert to Default with original padding and no border-bottom.

**Violations**

- Compact-variant header transitioning to Default on scroll-up — error (Compact is the page's chosen variant; it doesn't grow into Default)
- Scroll-driven transition hiding the metadata row, alert, or action buttons — error (only breadcrumbs and title size change)
- Scroll-driven transition hiding the page header entirely — error (header is mandatory at all times)
- Compacting the header on scroll without making it sticky — error (without stickiness, the user loses the header without gaining any benefit)
- Scroll-driven transitions on a fixed-height surface where scrolling is impossible — note (no harm; rule isn't doing anything)

**Examples**

✓ Object detail page with a long form opts in: opens Default with breadcrumbs + Text 2XL title; scroll down pins to top and shows Compact form; action buttons, metadata row, and alert remain visible.

✓ Short settings page doesn't opt in: Default header at top, scrolls away normally.

✗ Scroll transition drops the metadata row alongside breadcrumbs — breaks the variant contract.

✗ Header disappears entirely once the user scrolls past it.

---

## Rule: Page title format

**Description**

The page title is the type word for the page — singular for detail pages ("Faktura"), plural for list pages ("Fakturaer"), descriptive for settings and dashboards ("Innstillinger", "Dashboard"). Record-specific data (numbers, names, status, dates) lives in the metadata row, not the title.

The browser document title (`<title>`) is a different concern — it should still include record-specific info for tabs, history, and accessibility (e.g. *"Faktura 1234 — Acme AS · Tripletex"*). This rule governs the visible title inside the page header only.

**How to Apply**

- Use the shortest type word that identifies the page.
- Render the title in **Text 2XL** (Default) or **Text XL** (Compact). See [`typography.md`](../foundations/typography.md).
- Don't put the object number, customer name, status, or any record-specific data in the title.
- The browser document title is set separately and may include record-specific info.
- **Title text truncates with `…` if it exceeds available width — it never wraps to a second line.** The single-line title is part of the page header's visual shape; wrapping would push the metadata row down.
- For canonical examples of titles and metadata combinations per page type, see the [Atlas Library — Page Header usage examples](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=12418-51347&t=a5rsetCbVeluqKNi-11) Figma reference.

**Violations**

- Title contains the object number (e.g. "Faktura 1234") — error
- Title contains the customer / project / object name (e.g. "Acme AS") — error
- Title contains a status, label, or chip — error
- Title is a long descriptive sentence rather than a short type word — warning
- Title wrapping to a second line instead of truncating — error
- Title missing on a page that has a header — warning

**Examples**

✓ "Faktura" with the metadata row reading `1234   Acme AS   Sent   Due 15.05.26`.

✓ "Fakturaer" on the invoice list page.

✗ "Faktura 1234 — Acme AS" — record-specific data in the title.

✗ "9001 Website Redesign" — object ID and name in the title.

---

## Rule: Metadata row contents

**Description**

The metadata row sits directly below the title and carries the record-specific information the title leaves out: object numbers, important details, sub-titles, status components. The row is the user's primary at-a-glance identifier for *which* record this page is showing. All content renders in **`--text-muted`** — text, icons, and Status component labels alike.

**How to Apply**

The metadata row may contain:

1. **Object number(s)** — invoice number, project ID, voucher number, the system identifier. Render first when present.
2. **Important details / sub-title** — short descriptive plain text: customer name, due date, project manager name. Bulk of the row's content on most pages.
3. **Status component(s)** — the canonical Status component for state (Draft, Sent, Paid, Overdue, Approved). See [`status.md`](status.md) *(pending)*. For categorical *type* indicators (rather than state), use Labels per [`labels.md`](labels.md).

**Order:**

- Text first (object numbers and important details), then Status components.
- When multiple Status components are present, render them in **process order** — the order in which the content is processed. E.g. if a record must be approved before it can be sent to a customer, *Approved* status renders before *Sent* status.

**Colour and spacing:**

- All metadata content uses **`--text-muted`** — plain text, any icons used inside metadata items, and the **labels of Status components** rendered in this row.
- Spacing between items is **12px** (no separator character required).
- Items read left to right in the order above when all present: object number(s) → details / sub-title → status component(s) in process order.

**Wrapping:**

- If the row exceeds available width, **wrap to a second line — don't truncate.** The metadata row carries the record's identity; keeping it readable on narrow screens matters more than preserving a single-line shape.

**Reference:** for canonical title-plus-metadata combinations per page type, see the [Atlas Library — Page Header usage examples](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=12418-51347&t=a5rsetCbVeluqKNi-11) Figma reference.

**Violations**

- Form fields, inputs, dropdowns, or any interactive control in the metadata row — error (the row is descriptive, not interactive)
- Action button rendered as a metadata item — error
- Long-form copy / paragraphs in the metadata row — error
- Metadata content not in `--text-muted` (any other text colour token, or hardcoded colour) — error
- Icon inside a metadata item not in `--text-muted` — error
- Status component label inside the metadata row not rendering in `--text-muted` — error
- Status components rendered out of process order (e.g. *Sent* before *Approved* when approval is the prerequisite) — warning
- Spacing between metadata items other than 12px — warning
- Truncating an item before allowing the row to wrap — error

**Examples**

✓ `1234   Acme AS   [Approved]   [Sent]   Due 15.05.26` — number, customer, two Status components in process order (approval is the prerequisite to sending), due date, each separated by 12px, all `--text-muted`.

✓ `9001   Website Redesign   [Active]   Project manager: Olivier Klaver`.

✓ Long metadata row wraps to a second line on a narrow viewport rather than truncating.

✗ `[Save invoice]   1234` — action button as a metadata item.

✗ `1234   A long descriptive paragraph explaining what this invoice is for…` — long-form copy.

✗ Metadata row rendered in `--text-primary` instead of `--text-muted`.

✗ `1234   Acme AS   [Sent]   [Approved]` on a record where approval is a prerequisite to sending — Status order should reflect the process.

---

## Rule: Auto-save indicator placement

**Description**

On pages that auto-save, the header renders a sync-state indicator inside the title row, immediately to the right of the page title and to the left of the action group. When-to-auto-save and the indicator's state semantics belong to [`patterns/auto-save.md`](../../patterns/auto-save.md) *(pending)*; this rule covers placement only.

**How to Apply**

- Place the indicator right of the title, before the action group, whenever the title row has space.
- The indicator counts toward the title row's width budget — under width pressure, the title truncates against the indicator's left edge; the indicator stays put.
- **Narrow-viewport exception** (≈ ≤640px — see *Open Questions* re: breakpoint token): when the title row can't fit title + indicator + actions on one line, the indicator may wrap to its own row directly **below the title row, above the metadata row** — never below the metadata row, never into the action group or kebab, never hidden.
- The indicator never appears in the metadata row, action group, alert slot, or kebab — regardless of viewport.

**Violations**

- Auto-save indicator placed in the metadata row — error
- Auto-save indicator inside the action group or kebab — error
- Auto-save indicator hidden on any viewport — error (user must always know sync state)
- Auto-save indicator wrapping to its own row at desktop widths where the title row has space — warning
- Page auto-saves but renders no indicator — error

**Examples**

✓ `Faktura  [• Lagret]                          [Send] [⋮]`

✗ Indicator rendered as a metadata item below the title.

---

## Rule: No Save buttons on auto-save pages

**Description**

If the page auto-saves, the page header's action group does not contain a "Save" button. The auto-save indicator is the save UX — adding a "Save" button makes the persistence model ambiguous and creates two competing affordances for the same outcome. State-transition buttons (Send, Approve, Lock period, Post) are allowed and encouraged — they do something *beyond* persisting.

**How to Apply**

- **No "Save" button.** Don't place a button labelled "Save", "Lagre", "Save changes", or any equivalent in the action group.
- **State-transition action buttons are allowed.** A button is appropriate when the action does something beyond persisting: submit, send, publish, finalise, approve, lock period, post the voucher.
- **Label the button with the action's verb, not "Save".** "Send invoice", "Lock period", "Approve reconciliation", "Publish project". Mirror the label across confirmation modal title and resulting toast (see [`patterns/modal-usage.md`](../../patterns/modal-usage.md) for the confirmation-modal pattern).
- **Don't mix auto-save and explicit-save in the same form.** One commit model per page.
- **Sensitive fields are excluded from auto-save.** Passwords, MFA codes, payment details are not auto-saved — see [`patterns/state-preservation.md`](../../patterns/state-preservation.md).

**Violations**

- Auto-save page with a button labelled "Save" / "Lagre" / "Save changes" in the action group — error
- State-transition button labelled "Save" instead of the action's verb (e.g. "Save" instead of "Send invoice") — error
- Vague label ("OK", "Done", "Confirm") on a state-transition button where a specific verb would describe the action — warning
- Same form mixes auto-save and explicit-save fields — error
- Sensitive fields auto-save — error
- "Save" button added to address user reassurance about an unclear indicator — warning (treat the indicator, not the symptom)

**Examples**

✓ Invoice draft page auto-saves; action group contains "Send invoice" (primary) and "Save as template" (creates a new template entity — a state transition). The auto-save indicator sits next to the title.

✓ Settings page auto-saves with no Save button — the indicator is the only persistence affordance.

✗ Auto-save page with both an indicator and a "Save" button in the action group.

✗ State-transition button labelled "Save" on an auto-save page that actually posts a voucher.

✗ Form where the description field auto-saves but the project-manager dropdown waits for a Save click.

---

## Rule: Alert placement

**Description**

The page header has an alert slot for surfacing alerts with page-or-higher scope (system maintenance, environment warning, account-level notice, "you're viewing a read-only copy"). The alert slot holds an **Alert** component — **not a Banner**. The two are distinct: **the page header can contain an Alert; it cannot contain a Banner.** Banners sit below the page header in the page content area; they never appear inside any page-header slot.

The alert is **optional**. Position depends on the variant: Default renders it as a bottom slot below the metadata row; Compact renders it on the title row, beside the title.

Alert *content* rules (label / colour, stacking, dismissibility) belong to [`alert.md`](alert.md). This rule covers placement and width-pressure behaviour only.

**How to Apply**

**Default variant — bottom slot:**

- Place the alert below the metadata row, above main page content.
- Alert spans the page header's full content width.

**Compact variant — title row:**

- Place the alert on the title row, immediately next to the title (as far left as it can sit while remaining beside the title).
- The metadata row stays directly under the title; the alert does not push it down.
- The alert is constrained to the title row's width (it doesn't span full content width like the Default's bottom slot).

**Both variants:**

- Alert is rendered in one place per variant — never in both the title row and the bottom slot at the same time.
- Section-scoped alerts (about one card, one form, one workflow step) **do not** belong in the page header — they sit next to the section they refer to.
- **Banners never appear inside the page header.** They live in the page content area below the header. See [`banner.md`](banner.md).

**Width-pressure behaviour:**

- Alert **text truncates** with `…` if it exceeds the slot's width — it does not wrap to a second line inside the page header.
- The Alert's **"Read more" link always stays visible** — never truncated, never hidden, never collapsed under width pressure. The user must always be able to access the full message.

**Violations**

- Default variant: alert placed above breadcrumbs or in the title row — error
- Compact variant: alert placed below the metadata row instead of on the title row — error
- Compact variant: alert placed between the title row and the metadata row — error
- Alert rendered in two places at once — error
- **Banner rendered inside the page header (any slot) — error** (banners go below the page header, not inside it)
- Section-scoped alert placed in the page header's alert slot — warning (mismatched scope)
- Page-scoped alert rendered outside the page header (floating in the body) — warning
- Alert text wrapping to a second line instead of truncating — warning
- Alert "Read more" link hidden, truncated, or collapsed under width pressure — error

**Examples**

✓ Default: an "environment: staging" alert sits below the metadata row, above the page content.

✓ Compact: an embedded sub-pane uses Compact; a small alert sits on the title row beside the title; the metadata row stays directly underneath.

✓ Long alert text on a narrow viewport: text truncates with `…`; the "Read more" link sits to the right, always visible so the user can access the full message.

✗ A Banner placed inside the page header — banners go below the page header, not inside it.

✗ Compact-variant alert pushes the metadata row down instead of sitting beside the title.

✗ "You have unsaved changes in this section" alert placed in the page header alert slot when it refers to one form on a multi-form page.

✗ Alert "Read more" link disappears under width pressure while the alert text remains visible.

---

## Rule: Responsive collapse order

**Description**

When the viewport narrows past the point where the title row fits, the header collapses in a specific order. Hard constraint: **the primary action button never moves into the overflow kebab.** The user must always be able to perform the page's main action without opening a menu first. Everything else gives way before the primary does.

**How to Apply**

Collapse happens in this order. Each step is taken only when the previous didn't free enough space:

1. **Action buttons fold into the overflow kebab from left to right — least important first.** The right-aligned action group reads, from left to right, tertiary → secondary → primary → kebab. The leftmost (least prominent) folds first.
2. **Primary action never collapses.** It stays as a regular button in the rightmost regular-button position, left of the kebab. If only the primary remains, the kebab still shows the collapsed actions.
3. **Title truncates to a min-width with ellipsis** only after action collapse is exhausted. Set a min-width long enough to show the type word in full; truncate with `…` past that point. The auto-save indicator does not move.
4. **Metadata row wraps** to a second line if needed, before any item is truncated.

When folded into the kebab, action buttons render as **drawer rows** — text-only or text + 20px icon — per [`drawer.md`](drawer.md) *Row content*. They never render as full buttons inside the kebab's drawer.

**Violations**

- Primary action button folded into the overflow kebab — error
- Auto-save indicator hidden under width pressure — error
- Action buttons folded out-of-order (e.g. secondary collapses before tertiary) — warning
- Title truncated before action collapse is exhausted — warning
- Action buttons rendered as full buttons inside the kebab drawer instead of drawer rows — error

**Examples**

✓ Viewport narrows; the leftmost tertiary "Send feedback" button folds into the kebab first; primary "Send invoice" stays visible as a regular button.

✗ Viewport narrows; the page hides every action button (including primary) behind the kebab so the user can no longer see what the page's main action is.

✗ Title truncates while three regular action buttons are still visible.

---

## Related Rules

- [`patterns/button-placement.md`](../../patterns/button-placement.md) — action button slot, ordering, overflow kebab.
- [`breadcrumb.md`](breadcrumb.md) — breadcrumbs slot, including truncation behaviour.
- [`alert.md`](alert.md) — the Alert component used in the page header's alert slot.
- [`banner.md`](banner.md) — the Banner component, which lives **below** the page header in the page content area (banners do not appear inside the page header).
- [`patterns/banner-usage.md`](../../patterns/banner-usage.md) — when to use banners.
- [`status.md`](status.md) *(pending)* — Status component used in the metadata row.
- [`labels.md`](labels.md) — canonical label types for the metadata row.
- [`drawer.md`](drawer.md) — drawer rows used inside the page header's overflow kebab.
- [`typography.md`](../foundations/typography.md) — Text 2XL / Text XL title sizes.
- [`patterns/auto-save.md`](../../patterns/auto-save.md) *(pending)* — full auto-save pattern; this file covers placement only.
- [`patterns/state-preservation.md`](../../patterns/state-preservation.md) — sensitive-field carve-out.

---

## Open Questions

- **`PageActionLink` variant** — link-styled action with a full-width hitbox. Usage rule (vs `PageActionButton`, hitbox spec, hover / focus treatment) to be defined.
- **Tabbed pages** — when the canonical "Add" action belongs to the active tab's content rather than the page header; follow-up rule belongs in `patterns/table-usage.md` or a tabs pattern file.
- **Metadata-row icon decoration** — `apps/project/src/components/Page/ProjectPageHeader.tsx` decorates metadata items with icons (calendar next to dates, avatar next to project manager). This rule does not endorse icon decoration; team needs to decide whether to bless this pattern or align `apps/project` to plain text + status components.
- **Tabs row inside page header** — Atlas does not currently document a tabs slot inside the header. If needed, belongs in `tabs.md` *(pending)* and would extend this anatomy.
- **Sticky-on-scroll spacing and border tokens** — *Sticky header* references "tighter vertical padding" and "1px hairline border-bottom" without concrete tokens. Confirm against Figma and replace the prose with token names.
- **Narrow-viewport breakpoint** — *Auto-save indicator placement* uses "≈ ≤640px" as the narrow-viewport breakpoint. Atlas has no breakpoint tokens; if / when defined, replace this approximation.
- **Compact-mode alert tooltip-collapse bug** — current React implementation collapses the Compact-mode alert to an icon-only tooltip trigger. This is a bug per the design intent in *Alert placement*; alerts should remain readable in Compact form. Tracked in `TODO.md` as a follow-up for the Astro design system team.
- **Compact variant prop** — React component renders Compact only via the sticky-scroll transition; no `variant="compact"` prop exists for static Compact rendering on non-scrolling surfaces. Follow-up in `TODO.md` for the Astro design system team.


---

## components/pagination.md

# Pagination Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Pagination component — page size options, navigation controls, and when to use pagination vs. infinite scroll.

---

## components/popover.md

# Popover Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Popover component — the desktop hover-open surface for rich content (text, links, buttons, inputs, graphics, charts, AI clarifications). Covers anatomy, the ARIA contract (`role="dialog"` + `aria-expanded` on trigger), focus management (focus moves into the popover on open, returns to trigger on close, Escape dismisses), WCAG 1.4.13 dismissible / hoverable / persistent contract, auto-position / flip near viewport edges, and the mobile bottom-sheet rendering on tap-and-hold.

Pattern decision (popover vs tooltip) lives in [`../../patterns/popover-usage.md`](../../patterns/popover-usage.md). Pre-drafting QA: validate against [Microsoft HAX Toolkit](https://www.microsoft.com/en-us/haxtoolkit/ai-guidelines/) and [Google PAIR Guidebook](https://pair.withgoogle.com/guidebook/) plus the WAI-ARIA APG tooltip / dialog patterns.


---

## components/popup-menu.md

# Popup Menu — Redirect

> **This file is a redirect, not a rule file.** The canonical rules for the anchored option-list surface previously called "Popup Menu" now live in [`drawer.md`](drawer.md).

## Why this file exists

The Figma library calls this component **Popup Menu**. Atlas has renamed it **Drawer** in code and in design rules going forward. This file exists so anyone searching for "popup menu" in the design-system folder lands somewhere useful instead of dead-ending.

## Why the rename

*Popup menu* read as a sibling of *Popover* and *Modal* — three "popup-shaped" surfaces with three different meanings — which caused real confusion in reviews ("is this a popup menu or a popover?"). *Drawer* is unambiguous and reflects the component's actual behaviour: an anchored option-list surface that opens off the trigger (a `[⋮]` icon button, a chevron, a picker chrome), not a free-floating popup.

The Figma library still uses *Popup Menu* as the component name; that's the only place the old term is canonical. Everywhere else — code, design rules, PR descriptions, reviews — say **Drawer**.

## Where the rules live now

- **[`drawer.md`](drawer.md)** — anatomy, sizing, scroll behaviour, dismissal, keyboard navigation, and the full Atlas contract for the surface.
- **[`patterns/button-placement.md`](../../patterns/button-placement.md)** *Page header button placement* — when an overflow `[⋮]` opens a Drawer instead of a stacked button group.
- **[`buttons.md`](buttons.md)** — icon button rules (the trigger for the Drawer in overflow contexts).

## Related

- [`drawer.md`](drawer.md) — the canonical home.
- [`modal.md`](modal.md) — not the same component; modals are page-blocking surfaces with their own contract.
- [`../../patterns/popover-usage.md`](../../patterns/popover-usage.md) — popover vs tooltip (also not the same as a Drawer; popovers are informational, drawers are interactive option lists).


---

## components/progress-indicator.md

# Progress Indicator Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Progress Indicator component — linear vs. stepped, labeling, and completion states. See also `patterns/loading-states.md`.

---

## components/shortcut-group.md

# Shortcut Group Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Shortcut Group component — layout, key display, and usage context.

---

## components/skeleton.md

# Skeleton Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Skeleton loader component — when to use skeleton vs. spinner, sizing to match content, and animation behavior. See also `patterns/loading-states.md`.

---

## components/spinner.md

# Spinner Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Spinner component — sizes, placement, and when to use spinner vs. skeleton. See also `patterns/loading-states.md`.

---

## components/status.md

# Status Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Status component — variants, color usage, labeling, and placement in tables and headers.

---

## components/status-chip.md

# Status Chip Rules

> **Status**: Not yet documented. Requires a formal Atlas Library Figma entry before rules can be written. See `TODO.md` for this task.

This file will document rules for the **Status Chip** — Atlas's selectable-chip control for editing per-row state in tables. Status Chip is the preferred alternative to per-row Dropdown for small-N (2–4) state choices, and the recommended editable counterpart to the display-only Status component.

A working sketch lives in the [Atlas Component Development Workfile](https://www.figma.com/design/vCb2O3BLUotY1JdJ6rCBFf/Atlas-Component-Development--Workfile-?node-id=5094-19516). The component needs a formal Atlas Library Figma entry (anatomy / states / sizing) before this rule file can land. Coordinate with the Design System team.

Cross-referenced from `patterns/checkbox-vs-switch.md` Rule 2 and `design-rules/components/forms/toggle-switch.md` Rule 6 as the preferred control for editable per-row state in tables.


---

## components/stepper.md

# Stepper Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Stepper component — used inside modals and on dedicated pages to break a multi-step task into discrete steps with explicit progress indication. Two variants both in production but not yet documented:

- **Horizontal stepper** — used inside modals; steps render left-to-right with the current step highlighted; Next / Previous in the footer button group (see [`modal.md`](modal.md) *Modal footer button group* for the stepper exception).
- **Vertical-navigational stepper** — used on dedicated pages; steps render top-to-bottom and act as a navigation surface; the user can jump back to a previous step without losing in-progress state per [`../../patterns/state-preservation.md`](../../patterns/state-preservation.md).

Cross-refs: [`modal.md`](modal.md), [`../../patterns/state-preservation.md`](../../patterns/state-preservation.md), [`../../patterns/button-placement.md`](../../patterns/button-placement.md), and (when drafted) [`../../patterns/dependent-pickers.md`](../../patterns/dependent-pickers.md) for chained-picker flows that may use a stepper as an alternative shape.


---

## components/suggestion-buttons.md

# Suggestion Button Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document the small button used to suggest automations or auto-fill form fields. Sizing, placement, behavior, when to use.

## Notes

- Currently a tiny button used only for suggesting automations (e.g., "fill this with X")
- Considering consolidation with chips component (see `TODO.md`)

---

## components/table.md

# Table Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the standard Table component — column structure, row spacing, sorting, selection, and empty states. See also `patterns/table-usage.md` for data density and behavioral patterns.

---

## components/tabs.md

# Tabs Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Tabs component — variants, active states, overflow behavior, and when to use tabs vs. content switcher.

---

## components/tooltip.md

# Tooltip Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for the Tooltip component — the label-only hover hint required on every icon button. Covers anatomy, the label-only constraint (no interactive content; tooltips cannot receive focus), keyboard focus triggering the tooltip alongside pointer hover (WCAG 1.4.13 + 2.1.1), WCAG 1.4.13 dismissible / hoverable / persistent contract (Escape dismisses without moving focus), the ARIA contract (`role="tooltip"` + `aria-describedby` on trigger), and auto-position / flip near viewport edges.

Pattern decision (tooltip vs popover) lives in [`../../patterns/popover-usage.md`](../../patterns/popover-usage.md). Pre-drafting QA: validate against published AI-interaction guidelines and the WAI-ARIA APG tooltip pattern.


---

# FORMS

---




---

## forms/checkbox.md

# Checkbox Rules

> **Status: DRAFT — pending team review per decision #54.**

The checkbox is the canonical control for **selection** in Tripletex — picking one or more items from a list, opting into something at submit time, accepting terms, choosing rows in a table. It's a discrete binary (or tri-state via Indeterminate) the user reads and decides on, rather than a value they type.

Checkbox belongs to the **selection** sub-family of form components alongside [`radio-button.md`](radio-button.md) and [`toggle-switch.md`](toggle-switch.md) — controls where the chrome *is* the value. Value-entry components ([`input.md`](input.md), [`textarea.md`](textarea.md), and the input-derived types) are a separate sub-family where the chrome *contains* a typed value. Anatomy, modes, and interaction states are documented locally rather than inherited from `input.md`. Shared conventions (e.g. the 8px control-to-label gap matching input's 8px label-to-field gap) are noted per rule.

For *when* to reach for a checkbox vs radio button / toggle switch / multi-select dropdown, see [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md).

**Out of scope:** when to use checkbox vs other selection controls (see above); selection patterns inside tables (`table.md` *(pending)* — header *Select all*, shift+click range, persistence across pagination); filter checkboxes inside filter UIs; content type markers (Info / Automation / Warning) — checkbox is a binary signal; additional semantic meaning belongs in surrounding helper text, an Alert, or a Banner, not on the box itself.

**Figma reference:** [Atlas Library — Checkbox](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-40913) — anatomy, the nine-cell state matrix, sizing, focus-ring rendering.

---

## Rule: Checkbox anatomy

**Description**

A checkbox is a small square control with a label to its right. The control is `20 × 20` (component boundary, layout footprint, click target); inside that boundary the visible box renders at `18 × 18` with 1px reserved on every side for the focus ring (see *Interaction states*). The label is always present and sits to the right of the control with **8px** between them. Helper text is optional below the label. When multiple checkboxes share a logical group, a group label sits above the items (see *Standalone vs grouped*).

**How to Apply**

Horizontal order, left to right:

1. **The control** — `20 × 20` component boundary; visible `18 × 18` box with `2px` border radius.
2. **8px gap** between the right edge of the control's boundary and the start of the label. Matches the 8px label-to-field gap in `input.md`.
3. **Label** (required) — to the right of the control. Vertically centred to the first line of label text.

Helper text (optional) sits below the label.

**Inline contexts** (table row-select, filter chip, toolbar opt-in) drop the visible label and rely on `aria-label` / `aria-labelledby` — see *Every checkbox has an accessible name*. The label-on-the-left layout is never used in Atlas.

**Violations**

- Label rendered anywhere other than to the right of the control — error
- Control-to-label gap not 8px — warning
- Checkbox rendered without an accessible name (no visible label and no `aria-label` / `aria-labelledby`) — error
- Helper text rendered above the label instead of below — warning

**Examples**

✓ `[_]  Send me product updates` — control on the left, 8px gap, label on the right.

✓ An *I agree to the terms* checkbox above a Sign-up button — control on the left, full label-text to the right.

✗ A row of checkboxes with labels stacked above each control instead of to the right.

---

## Rule: Checkbox states

**Description**

A checkbox is in one of three behavioural states: **Unchecked**, **Checked**, or **Indeterminate**. The first two are user-set; the third is system-set and only appears when a parent checkbox summarises a group of children where some — but not all — children are checked. Each behavioural state has three interaction variants (Default / Hover / Disabled) for a total of nine state combinations.

**How to Apply**

Token mapping per state:

| Behaviour | Interaction | Box surface | Box border | Indicator |
|---|---|---|---|---|
| Unchecked | Default | `--form-rest` | `--border-primary` | none |
| Unchecked | Hover | `--form-rest` | `--form-border-hover` | none |
| Unchecked | Disabled | `--surface-disabled` | `--border-primary` (greyed) | none |
| Checked | Default | `--surface-info-active` | `--surface-info-active` | check, `--text-on-action` |
| Checked | Hover | `--surface-info-active` (hover darken) | `--surface-info-active` (hover darken) | check, `--text-on-action` |
| Checked | Disabled | `--surface-disabled` | `--border-primary` (greyed) | check, greyed |
| Indeterminate | Default | `--surface-info-active` | `--surface-info-active` | dash, `--text-on-action` |
| Indeterminate | Hover | `--surface-info-active` (hover darken) | `--surface-info-active` (hover darken) | dash, `--text-on-action` |
| Indeterminate | Disabled | `--surface-disabled` | `--border-primary` (greyed) | dash, greyed |

The hover-darken values for Checked and Indeterminate come from the Atlas Library Figma — they're hover-state variants of `--surface-info-active`.

**Indeterminate behaviour.** When a parent checkbox is Indeterminate (some children selected), clicking the parent **deselects all children first** — parent and children both move to Unchecked. A subsequent click selects all (parent and children Checked). The parent is never Indeterminate as a direct user choice; it always reflects "this is the summary state of my children."

**Indicator glyph.** Atlas's `done` icon (check) and `horizontal_rule` icon (dash) from the Atlas icon library — see [`foundations/icons.md`](../../foundations/icons.md).

**Violations**

- Indeterminate state set on a checkbox that has no children to summarise (e.g. a standalone *I agree* toggled into indeterminate) — error
- Click on an indeterminate parent that goes directly to Checked (skipping the deselect-all step) — error
- Checked or Indeterminate box rendered with a colour other than `--surface-info-active` — error
- Disabled state without the `--surface-disabled` fill — error
- Custom indicator glyphs (a star, a custom tick) instead of the canonical `done` / `horizontal_rule` icons — error

**Examples**

✓ Three children *Email / SMS / Push* with their parent *Send me notifications* — selecting two of three children renders the parent as Indeterminate.

✓ Clicking the Indeterminate parent above first deselects Email and SMS (children Unchecked, parent Unchecked). The next click selects all three.

✗ A *Show advanced options* toggle rendered as an Indeterminate checkbox to mean *"partially configured"* — Indeterminate is reserved for parent-of-children, not arbitrary tri-state semantics.

---

## Rule: Checkbox sizing

**Description**

Atlas checkboxes have one size everywhere: `20 × 20` component boundary, `18 × 18` visible box. The single-size rule applies on forms, in modals, inside tables, and in dense filter UIs — scaling smaller hurts hit targets and visual rhythm; scaling larger competes with the input field next to it.

**How to Apply**

| Measurement | Value |
|---|---|
| Component boundary (layout footprint, click target on the box) | `20 × 20` |
| Visible box (border + fill area) | `18 × 18` |
| Border width | `1px` |
| Border radius | `2px` |
| Indicator glyph | Atlas `done` / `horizontal_rule` icons (see [`foundations/icons.md`](../../foundations/icons.md)) |

The 1px gap between the visible box and the component boundary is the reserved space for the focus ring (see *Interaction states*) so focus styling doesn't push surrounding layout.

**Violations**

- Checkbox rendered at a size other than `20 × 20` boundary / `18 × 18` visible — error
- Custom border radius other than `2px` — warning
- A "compact checkbox" or "large checkbox" variant — error

**Examples**

✓ A 20×20 checkbox in a settings form lines up with input labels and other form controls.

✓ The same 20×20 checkbox used as a row-select control in a table.

✗ A scaled-down 14×14 checkbox squeezed into a dense table cell — fails the hit target and breaks visual rhythm.

---

## Rule: Standalone vs grouped, and group orientation

**Description**

A checkbox is either a **standalone** (one box with its own label, semantically independent — *Remember me*, *I agree to the terms*) or part of a **group** (≥2 boxes wrapped in a single labelled set, representing a multi-select question — *Notification channels: email / SMS / push*). The two patterns have different anatomy, different ARIA, and different validation routing.

**How to Apply**

**Standalone:**

- A single `Checkbox` with its own label.
- Native `<label>` association — clicking the label toggles the box (see *Click target spans label and box*).
- Validation message, when present, renders directly below the checkbox using `FieldError` (see *Validation behaviour*).

**Grouped:**

- ≥2 `Checkbox` items wrapped in a `CheckboxCollection`.
- Group label sits **8px above** the first checkbox in the group (rendered via the `<Label>` slot inside `CheckboxCollection`). Matches the control-to-label gap inside an individual checkbox and the label-to-field gap in `input.md`.
- Group label is the accessible name for the collection (`role="group"` + `aria-labelledby` is handled by the underlying react-aria-components `CheckboxGroup`).
- Group-level validation message (`errorMessage` prop on `CheckboxCollection`) renders below the group via `FieldError`.

**Group orientation:**

| Orientation | When | Spacing between items |
|---|---|---|
| Vertical (default) | Most groups — long labels, large item counts, top-to-bottom reading order | `8px` |
| Horizontal | Short labels, 2–4 items, fits on one row | `16px` |

Horizontal grouping is opt-in: the developer sets `flex-direction: row` and uses the larger `16px` gap so the row reads as a row, not a wrapped column.

Use a group whenever ≥2 checkboxes share a category. Even a two-checkbox group gets the group treatment; treating it as two standalones loses the semantic linkage and breaks screen-reader announcement.

**Violations**

- Two or more related checkboxes rendered as parallel standalones without a `CheckboxCollection` wrapper — error
- Group rendered without a group label — error
- Group orientation horizontal with `8px` gap instead of `16px` — warning
- Group orientation vertical with `16px` gap — warning (too airy; vertical groups read better at 8px)

**Examples**

✓ A standalone *I agree to the terms* checkbox above a Sign-up button.

✓ A *Notification channels* group with three vertical checkboxes (Email / SMS / Push), 8px between items, group label *Notification channels* above.

✓ A *Filter by status* group with three horizontal checkboxes (Open / In progress / Done), 16px between items.

✗ A pair of related opt-in checkboxes (*Send me weekly digest* / *Send me product news*) rendered as two standalones with no group label.

---

## Rule: Click target spans label and box

**Description**

Clicking anywhere on the visible label or the control toggles the checkbox. The label is part of the active click area, widening the effective target well past the `20 × 20` control alone — which matters for both pointer accuracy and touch.

**How to Apply**

- The full label-text element is part of the click target. Native HTML `<label for="...">` does this automatically when the label wraps or is associated with the input; react-aria's `Checkbox` does it via its render structure.
- Hover state is visible across the whole label+box area — cursor over the label gives the same hover affordance as cursor over the box.
- Helper text (when present) is **not** part of the click target — reading material, not an action surface.

**Touch-target recommendation.** The `20 × 20` box alone is below the WCAG 2.2 SC 2.5.8 minimum (`24 × 24`). With a visible label, the effective target is "box + 8px gap + label width" — comfortably above the minimum in practice. **Avoid shipping a labelless checkbox** (`aria-label`-only) in a touch context unless the surrounding container already provides a target above 24×24 (e.g. a full-width table row that toggles the row-select checkbox).

**Violations**

- Clicking the label does not toggle the box — error
- Hover state shown only when the cursor is over the box, not the label — warning
- Helper text rendered as part of the click target — warning
- Labelless checkbox in a touch-first context (mobile invoice line, dense touch table) without a surrounding ≥24×24 target — warning

**Examples**

✓ A *Send me product updates* checkbox — clicking the words "Send me product updates" toggles the box, same as clicking the box itself.

✗ A checkbox where only the small box accepts clicks; clicking the label does nothing.

---

## Rule: Every checkbox has an accessible name

**Description**

A checkbox without an accessible name is unusable with assistive technology — screen readers announce *"checkbox, unchecked"* with no indication of what the user is choosing. Atlas's default and strongly preferred approach is a **visible label** to the right of the box (per *Checkbox anatomy*); the carve-out below covers the rare inline cases where surrounding context provides the name.

**How to Apply**

Three ways to provide an accessible name, in order of preference:

1. **Visible label** — the default, required for any checkbox in a standard form, dialog, settings page, or standalone consent control.
2. **Group label** — for items inside a `CheckboxCollection`, the group label is the accessible name for the group; individual items still need their own labels per *Checkbox anatomy*.
3. **`aria-label` or `aria-labelledby`** — for inline / table contexts that don't have a label slot (table row-select, filter chip, toolbar opt-in). Use `aria-label` for a simple, stable string; `aria-labelledby` when an existing element in the surrounding context already labels what's being selected.

**Inside a table** (the most common labelless case):

- **Per-row checkbox** — `aria-label="Select <row identifier>"` where the row identifier is the most meaningful piece of data in the row (customer name, invoice number, project name). The visible column header gives sighted users visual context; the per-row `aria-label` gives screen-reader users per-row specificity. Examples: `aria-label="Select customer Acme Corp"`, `aria-label="Select invoice 10042"`.
- **"Select all" header checkbox** — `aria-label="Select all rows"` is the baseline. When pagination is in play and the scope changes meaning, narrow it: `aria-label="Select all visible rows"` or `aria-label="Select all on page"`.
- **Composed or multi-line row identifiers** — prefer `aria-labelledby="<id of the cell that labels the row>"` over hand-rolling the string. Keeps the announced name in sync with the cell text automatically.
- **The table caption (`<caption>`) or surrounding heading is not the accessible name** for individual row checkboxes — captions describe the table as a whole, not the action on a specific row. Always provide a per-checkbox `aria-label` or `aria-labelledby`.

The `aria-label` (or the text in the element referenced by `aria-labelledby`) must accurately describe the action — *"Select <something specific>"*, never just *"checkbox"*, *"tick this"*, or the placeholder column name.

Detailed table-specific row-selection conventions (column placement, header *Select all* indeterminate behaviour, shift+click range, persistence across pagination, keyboard nav for selection) belong in [`table.md`](../table.md) *(pending)*; this rule covers only the accessibility contract.

**Violations**

- Checkbox rendered with no visible label and no `aria-label` / `aria-labelledby` — error
- Checkbox using `aria-label` in a context that has a label slot available — warning (the visible label is preferred whenever there's room)
- `aria-label` text that doesn't describe the action (*"checkbox"*, *"tick this"*, *"select"*) — error
- Table row-select checkbox relying on the table caption alone for its accessible name — error
- `aria-labelledby` pointing at an element that's hidden or doesn't visibly label the row — warning

**Examples**

✓ `[_]  Send me product updates` — visible label, native association.

✓ A *Customers* table with a row-select column; each row's checkbox carries `aria-label="Select customer Acme Corp"`.

✓ A *Customers* table whose row's primary cell renders the customer name; row checkbox uses `aria-labelledby="customer-cell-42"` pointing at that cell.

✓ A *Select all* checkbox in the header of a paginated invoice table with `aria-label="Select all visible invoices"`.

✗ A standalone checkbox with no visible label and no `aria-label`.

✗ A row-select checkbox with `aria-label="checkbox"` — uninformative.

✗ A table with `<caption>Customers</caption>` and row-select checkboxes that have no per-row `aria-label`.

---

## Rule: Validation behaviour

**Description**

Checkboxes validate at two levels: **per-box** (an individual checkbox is required or fails a `validate` callback) and **group-level** (a `CheckboxCollection` carries an `errorMessage` reflecting a constraint on the whole group, e.g. *"Select at least one"*). Both error paths render their message below the affected surface via `FieldError`. Per-box error styling additionally re-skins the box itself (red border + red outline) for the duration of the invalid state.

**How to Apply**

**Per-box error styling** when an individual checkbox is in `isInvalid` state:

- Box border: `--border-error`.
- Box outer ring: `--surface-error-rest` outline, 3px, sitting outside the box border.
- Hover: border darkens to the error-hover variant.
- Error message: rendered as `FieldError` below the checkbox, leading error icon, left-aligned.

**Group-level error message** (the more common path):

- Set `errorMessage` on the `CheckboxCollection`.
- Renders as `FieldError` below the group, below the last child checkbox.
- The group's `isInvalid` is set when `errorMessage` is truthy.

Both paths use the standard validation-feedback pattern from [`patterns/validation-feedback.md`](../../../patterns/validation-feedback.md): focus management on submit-failure follows the form's `ErrorSummary`; the submit button stays enabled (validation-gate disabling is forbidden across Atlas).

**Cross-reference:** a `required` checkbox (e.g. *I agree to the terms* required to proceed) uses per-box error styling at submit time when unchecked.

**Violations**

- Per-box red-border styling applied without an `isInvalid` state — error
- Validation message rendered as a Banner inside a form instead of a `FieldError` — error (banners-in-forms forbidden per [`banner.md`](../banner.md) *Banner placement*, with the validation-feedback transitional exception)
- Submit button disabled because a required checkbox is unchecked — error (validation-gate disabling forbidden)
- Group-level constraint failure rendered as per-box error on every checkbox — warning (use the group `errorMessage` instead so the user sees one constraint message, not N duplicates)

**Examples**

✓ An *I agree to the terms* required checkbox above Sign-up — submitting unchecked renders the box with a red border + outline, *"You must agree to the terms"* as a `FieldError` below.

✓ A *Notification channels* group with `errorMessage="Select at least one channel"` — error renders once, below the group, when no children are selected on submit.

✗ A required checkbox failing validation by silently disabling the submit button.

✗ A Banner reading *"Please complete required fields"* rendered inside a modal form.

---

## Rule: Disabled state

**Description**

A checkbox is disabled when the user cannot toggle it *right now*, but the box *could* be edited under different circumstances — filling in another field first, changing permission level, moving to a different context. Disabled signals **conditional unavailability**: there is a path to making the field active, and the rule's job is to tell the user what that path is. For values that are permanently fixed (audit logs, finalised submissions, locked records), see *Read-only state* instead.

**How to Apply**

| Aspect | Spec |
|---|---|
| Visual | Disabled chrome per *Checkbox states* (Disabled row, per behaviour) |
| Box cursor | `cursor: default` (**not** `cursor: not-allowed`) |
| Label rendering | Greyed alongside the box, using Atlas's disabled-state text token |
| Tooltip | **Required** — explains *why* the field is disabled and, where possible, *how* to make it available (*"Fill in Country first"*, *"Available to admin users only"*, *"Available after invoice is finalised"*) |
| ARIA | `disabled` attribute on the underlying input |
| Focusable | **No** — Tab skips disabled checkboxes; screen readers announce as dimmed / unavailable |
| Click target | Inert — clicks on the box or label have no effect |

The `cursor: not-allowed` cursor reads as *"you've been blocked"*; `cursor: default` reads as *"this just isn't active right now,"* which is closer to the truth and matches the conditional-unavailability framing.

**Violations**

- Disabled checkbox using `cursor: not-allowed` — error
- Disabled checkbox without a tooltip explaining why — warning
- Tooltip that doesn't tell the user how to make the field available, when there is a way — note
- Disabled used for a permanently-fixed value with no path to editing (should be Read-only) — warning
- Disabled checkbox using `aria-readonly="true"` instead of the `disabled` attribute — error
- Disabled checkbox that's focusable (Tab lands on it) — error

**Examples**

✓ A *VAT-registered* checkbox is disabled until *Country* is filled in; hovering shows *"Choose a country to enable VAT registration."*

✓ A *Send to client* checkbox disabled on a draft invoice; tooltip reads *"Available once the invoice is finalised."*

✗ A *Terms accepted* checkbox on a finalised contract page rendered as disabled — should be Read-only; the user cannot make this editable under any circumstance.

✗ A disabled checkbox using `cursor: not-allowed` and no tooltip.

---

## Rule: Read-only state

**Description**

A checkbox is read-only when the value is fixed and the user cannot toggle it under any path forward — audit logs showing past confirmations, finalised submissions, locked records, summary views of decisions already made. Read-only signals **permanent unavailability**.

**Read-only currently shares the same visual treatment as Disabled** as an interim. The design team has not yet articulated a distinct read-only visual; until they do, the behavioural differences (tooltip absence, focusable, ARIA) carry the distinction at the keyboard and assistive-tech layers, and surrounding context (an audit-log row, a finalised form) carries it for sighted users. Distinct visual treatment is tracked in *Open Questions*.

**How to Apply**

| Aspect | Spec |
|---|---|
| Visual | Same as Disabled chrome (interim) |
| Box cursor | `cursor: default` |
| Label rendering | Same as Disabled (interim) — greyed alongside the box |
| Tooltip | **None** — no "how to enable" exists; surrounding context provides the meaning |
| ARIA | `aria-readonly="true"` on the underlying input (**not** the `disabled` attribute) |
| Focusable | **Yes** — Tab lands on read-only checkboxes; screen readers announce *"read-only checkbox, checked / unchecked / indeterminate"* |
| Click target | Inert for toggling, but the box remains in the focus order so keyboard and screen-reader users can navigate to and read the value |

**Why focus matters for read-only.** Unlike Disabled (where Tab skipping is correct — the field isn't part of the active flow), Read-only is part of the displayed *information*. Keyboard users need to navigate to read-only values to read them; skipping them hides information from these users.

**Violations**

- Read-only checkbox using the `disabled` attribute instead of `aria-readonly="true"` — error
- Read-only checkbox not focusable (Tab skips it) — warning
- Read-only checkbox carrying a tooltip explaining why — note (no tooltip needed; surrounding context provides the meaning)
- Read-only used for conditionally-unavailable values where the user could make the box editable (should be Disabled) — warning
- Read-only checkbox with `cursor: not-allowed` — error

**Examples**

✓ An audit-log row showing a *Terms accepted* checkbox as checked, read-only — focusable, no tooltip, screen readers announce *"read-only checkbox, checked."*

✓ A finalised tax return showing *Period locked* as a checked read-only checkbox.

✗ An audit-log *Terms accepted* checkbox rendered with the `disabled` attribute — the user cannot Tab to it to read the value.

✗ A read-only checkbox carrying a tooltip *"This is a historical record"* — surrounding context already provides that meaning.

---

## Rule: Interaction states

**Description**

The interaction state describes what's happening right now — hover, focus, disabled, read-only, invalid. Each has a distinct visual treatment (the state-token table in *Checkbox states*) so the user knows where they are without thinking. **Focus is keyboard-only** — visible via `:focus-visible` / react-aria's `[data-focused]`, never on mouse-click.

**How to Apply**

| State | When it applies | Visual treatment |
|---|---|---|
| Default | At rest, no interaction | State tokens from *Checkbox states* (Default row per behaviour) |
| Hover | Pointer over the label or box | State tokens from *Checkbox states* (Hover row per behaviour) |
| Focus | Keyboard focus on the box | Box border becomes `--border-focus`; outer focus ring renders as a 1px `--border-focus` border, 3px offset outside the box, 3px corner radius |
| Disabled | *Disabled state* | State tokens (Disabled row per behaviour) |
| Read-only | *Read-only state* | Same as Disabled (interim) |
| Invalid | `isInvalid` true (*Validation behaviour*) | Red border + red outline per *Validation behaviour* |

**Focus is keyboard-only.** The focus ring renders only on keyboard focus (`:focus-visible` / `[data-focused]`) — clicking with a pointer does not show the ring, by design.

**Violations**

- Focused checkbox without a visible focus ring — error
- Focus ring shown on mouse-click (any-focus styling instead of `:focus-visible` / `[data-focused]`) — warning
- Hover state visually identical to default — warning

**Examples**

✓ Tabbing onto a checkbox in a form shows a clear outer focus ring around the box; clicking it with the mouse does not.

✗ A focused checkbox indistinguishable from default — fails keyboard-navigation visibility.

---

## Related Rules

- [`radio-button.md`](radio-button.md) — selection sub-family sibling (single mutually-exclusive pick).
- [`toggle-switch.md`](toggle-switch.md) — selection sub-family sibling (immediate-commit live state).
- [`input.md`](input.md) — anchor of the value-entry sub-family; checkbox is in the broader form family but documents its own anatomy, modes, and interaction states.
- [`textarea.md`](textarea.md) — multi-line value-entry sibling of input.
- [`../../../patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md) — selection sub-family decision guide: checkbox vs radio vs toggle vs multi-select.
- [`../table.md`](../table.md) *(pending)* — table row-select and header *Select all* use checkboxes; canonical placement and shift+click behaviour live there.
- [`../../../patterns/validation-feedback.md`](../../../patterns/validation-feedback.md) — validation surfacing rules for form fields.
- [`../banner.md`](../banner.md) — banners-in-forms forbidden; cross-referenced by *Validation behaviour*.
- [`../../foundations/colors.md`](../../foundations/colors.md) — surface, border, text tokens used in *Checkbox states*.
- [`../../foundations/icons.md`](../../foundations/icons.md) — `done` / `horizontal_rule` indicator icons.

---

## Open Questions

- **Figma per-box error state** — Figma's `.checkbox` frame defines nine states (3 behavioural × 3 interaction); the per-box error state shipped in React isn't represented in Figma. Add for parity.
- **React `Checkbox.css` token migration** — legacy `--atl-color-*` tokens should migrate to the new semantic tokens (`--form-rest`, `--border-primary`, `--form-border-hover`, `--surface-disabled`, `--surface-info-active`, `--text-on-action`, `--border-error`, `--surface-error-rest`).
- **React `Checkbox.css` gap fix** — component uses `gap: 12px` between box and label; should be `8px` to match *Checkbox anatomy*.
- **React `Checkbox.stories.tsx` `WithoutLabel` story** — either rename + add an `aria-label` to demonstrate the inline-context carve-out, or remove.
- **Atlas Checkbox `isReadOnly` API** — *Read-only state* documents Read-only as a formal mode, but the React API currently omits `isReadOnly`. Add it.
- **Distinct read-only visual treatment** — *Read-only state* shares Disabled chrome as an interim. Design team to articulate a distinct read-only visual; update *Read-only state* and track migration when it lands.
- **Forms-family read-only consistency** — `input.md` renders read-only inputs as plain text; checkbox renders read-only with disabled-shaped chrome (interim). Worth a deliberate decision on whether to align or document the divergence as canonical.
- **`colors.md` token coverage gap** — the `--form-rest` / `--form-border-hover` family used in checkbox should be reconciled with the `--surface-*` family used in input — same conceptual surface, different token names.


---

## forms/combobox.md

# Combobox Rules

> **Status**: Not yet documented. The formal Atlas rule is pending — see `TODO.md` for this task.

Atlas Combobox is the picker whose chrome is a typeable text input with autocomplete from a predefined suggestion list (single or multi, with optional create-new). It shipped per Stian Tøsse's announcement in `#astro_reception` (2026-02-16) but the canonical rule file (this one) is still a stub.

**Current reference until the formal rule lands:** [Atlas Combobox — legacy storybook](https://atlas.tripletex.dev/#/Components/ComboBox).

For when to use Combobox vs Select vs Dropdown, see [`forms/select.md`](select.md) § *"When to use Select vs Dropdown vs Combobox"* — the short version is: Combobox when the user *types* into the chrome (with suggestions as a helper, optional create-new); Dropdown when the user *clicks* selections from a popup; Select for short single-pick.

Cross-team prototype implementations built before the official Combobox shipped are tracked in [`pirate-components/registry.md`](../../../pirate-components/registry.md) — row *"Custom combobox / searchable suggestion input"* (`KRR ComboBoxField.tsx`, `SearchBrregOr1881ComboBox.tsx`, both built with `react-aria`). These are migration candidates pending the formal rule.


---

## forms/dropdown.md

# Dropdown Rules

> **Status: DRAFT — pending team review per decision #63.**

The Dropdown is the click-from-list picker — single or multi selection from a known list, with optional search-in-drawer for longer lists. The user picks by clicking options in the drawer; the trigger itself isn't typeable. For typeable triggers with autocomplete, see [`forms/combobox.md`](combobox.md). For short single-pick lists, see [`forms/select.md`](select.md).

Dropdown inherits anatomy / sizing / modes / content type markers from [`forms/input.md`](input.md), and the drawer surface from [`design-rules/components/drawer.md`](../drawer.md). Multi-select is a Dropdown mode, not a separate component (replaces the planned `forms/multiselect-dropdown.md`).

**Figma reference:** [Atlas Library — Dropdown](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=10292-14277)

---

## Out of scope

Inherits from `forms/input.md`:

- Label-to-field anatomy.
- Sizing (40px default, 32px compact for table rows only).
- Editable / disabled / read-only modes.
- Content type markers.
- Min and max width.

Inherits from `design-rules/components/drawer.md`:

- Drawer anatomy, positioning, visual treatment.
- Width and text overflow.
- Row content, row states, grouping.
- Scroll behaviour, async loading, z-stacking.
- Outside-click and Esc dismissal, base keyboard navigation.

Out of scope of this file: typeable-trigger pickers (`forms/combobox.md`); short single-pick (`forms/select.md`); date pickers (`period-selectors/date-picker.md`); multi-select with quantity per item (research ledger 2026-03-12 — Open Question below).

---

## Rule: Dropdown anatomy

**Description**

The trigger shows the value (or placeholder) followed by a trailing chevron. Activating opens the drawer per `drawer.md`. In multi mode, selections render either as a count inside the trigger or as removable chips below the trigger (*inline-chips variant*).

**How to Apply**

Trigger, left to right:

1. Value or placeholder (see *Closed-state placeholder*).
2. Trailing chevron — signals the trigger opens a drawer.

Content type marker (per `forms/input.md` Rule 8) stacks beside the chevron on the label side.

**Inline-chips variant (multi mode):**

- Selected items render as removable chips *below* the trigger, left-aligned, with `✕` per chip.
- Removing a chip deselects the option.
- The trigger stays at its placeholder; the chips communicate the selection.

Multi mode without inline-chips shows the selection inside the trigger as a typed count — see *Closed-state placeholder*.

**Violations**

- Trigger rendered without a chevron — error
- Chevron not in the trailing position — warning
- Inline-chips variant rendering chips inside the trigger instead of below — error
- Inline chip without a remove affordance — warning

**Examples**

✓ Single mode: `[Norway ▾]`.

✓ Multi mode, count: `[3 attestanter ▾]`.

✓ Multi mode, inline-chips:

```
[Velg attestanter ▾]
[Olena ✕] [Stian ✕] [Kha ✕]
```

✗ Multi-select with three selections, no count in the trigger and no chips below — the user can't tell what's selected without re-opening.

---

## Rule: Closed-state placeholder

**Description**

Norwegian-first wording with English fallback. Wording differs by context (form input vs filter) and by mode (single vs multi).

**Single mode:**

- Form input context: `Ikke valgt` (NO) / *Not selected* (EN). Empty placeholder allowed inline (table row, toolbar, popover) when the field is optional and the surrounding context makes "no selection" obvious.
- Filter context: `Alle {category}` (e.g. `Alle attestanter`). Empty placeholder forbidden — the semantic flips ("no filter applied → all match" vs "nothing selected").

**Multi mode, with selections:**

- Without inline-chips: `{n} {category}` (e.g. `3 attestanter`). Mirrors the filter-context `Alle {category}` shape. Falls back to `{n} valgt` only when no meaningful category noun exists.
- With inline-chips: trigger stays at its placeholder (e.g. `Velg attestanter`); chips below show the selection. Don't double up by showing both.

**Multi mode, no selections (filter context):** `Alle {category}` — same as single mode filter context.

**Violations**

- Form-input Dropdown with `Alle {category}` — error
- Filter Dropdown with `Ikke valgt` — error
- Filter Dropdown with empty placeholder — error
- Multi-mode count falling back to `{n} valgt` when a category noun exists — warning
- Inline-chips variant showing both a count and chips — warning
- Multi-mode enumerating all selected items in the trigger — warning

**Examples**

✓ Form input: a *Currency* field shows `Ikke valgt` until picked.

✓ Filter: an *Approver* filter shows `Alle attestanter` when no filter is applied.

✓ Multi-mode count: `3 attestanter` when three approvers are picked.

✗ A filter Dropdown shows `Ikke valgt` — reads as "I haven't picked, so nothing shown" when the intended semantic is "no filter, so all shown."

---

## Rule: Single vs multi mode

**Description**

Pick the mode at design time; Atlas doesn't expect runtime toggling. Single mode closes the drawer on selection; multi mode keeps it open.

**Single mode:**

- Drawer rows are plain (no checkboxes).
- Selecting closes the drawer; value writes to the trigger; focus returns to the trigger.

**Multi mode:**

- Drawer rows have a leading checkbox.
- Clicking a row toggles the checkbox; drawer stays open.
- Drawer dismisses on outside-click, Esc, or an explicit *Done* button if the design includes one.
- Selections render in the trigger (typed count per *Closed-state placeholder*) or as chips below (inline-chips variant per *Dropdown anatomy*).

**Violations**

- Single-mode drawer that doesn't close on selection — error
- Multi-mode drawer that closes on every selection — error
- Multi-mode rows without checkboxes — warning
- Mode toggled at runtime on the same Dropdown instance — error

**Examples**

✓ Single: user picks *Norway*; drawer closes; trigger shows `Norway`.

✓ Multi: user picks *Olena*, drawer stays open, picks *Stian*, clicks outside to dismiss; trigger reflects both.

---

## Rule: Disabled trigger when no content to show

**Description**

If the Dropdown has nothing to render at open time (empty list, async returned zero, surrounding context not ready), the trigger is disabled with a tooltip. The drawer never opens. Trigger-side companion to `drawer.md` *Empty state*.

**How to Apply**

- Disabled-state mechanics from `forms/input.md` *Disabled state*.
- Tooltip names the reason and the path to availability (*"No tags yet — add tags in Settings"*, *"Pick a role first"*). Owned by Text Vault.
- Async loading before the data is known to be empty is a different state (skeleton rows per `drawer.md` *Async loading*).

**Chained pickers:** when a Dropdown sits in a chain (Product → Category → Tax code), the cross-component flow lives in [`patterns/dependent-pickers.md`](../../../patterns/dependent-pickers.md). NN/g cited there as the primary UX source.

**Violations**

- Enabled trigger that opens to an empty drawer — error
- Disabled trigger without a tooltip — warning
- Disabled trigger still activatable by Space / Enter — error

**Examples**

✓ A *Tags* multi-Dropdown on a new account: trigger disabled with *"No tags yet — add tags in Settings"*. Drawer never opens.

✓ Chained: *Category* and *Tax code* disabled with *"Pick a product first"* / *"Pick a category first"*. User picks a product; *Category* enables. User picks a category; *Tax code* enables.

✗ A *Customer* Dropdown's data returned zero, but the trigger stays enabled and the drawer opens empty.

---

## Rule: Search-in-drawer threshold

**Description**

The drawer optionally includes a search input at the top. Below ~10 options, search is noise. Above ~25, search is required.

**How to Apply**

| Option count | Search |
|---|---|
| Below 10 | Off |
| 10 to 25 | Optional — enable when labels are similar (countries starting with the same letters) or hard to scan |
| Above 25 | On |

Search filters the existing list. Typed values that aren't in the list aren't allowed (that's `forms/combobox.md`'s job).

**Violations**

- Dropdown with 4–6 options with a search input — warning
- Dropdown with 50+ options and no search — warning
- Search input accepts values not in the list — error (use Combobox)

**Examples**

✓ A *Currency* Dropdown with 4 options — no search.

✓ A *Country* Dropdown with 195 options — search at the top of the drawer.

✗ A *Status* Dropdown with three options (*Open*, *Closed*, *Archived*) with a search input.

---

## Rule: Keyboard navigation

**Description**

Single and multi mode differ on `Space` / `Enter` inside the drawer: single selects and closes; multi toggles and keeps the drawer open.

**Closed trigger:**

| Key | Behaviour |
|---|---|
| `Space` or `Enter` | Opens the drawer |
| `Arrow Down` | Opens the drawer with focus on the first row |

**Open drawer:**

| Key | Single mode | Multi mode |
|---|---|---|
| `Arrow Down` / `Arrow Up` | Next / previous row | Same |
| `Home` / `End` | First / last row | Same |
| `Enter` | Select; close; focus returns to trigger | Toggle row; drawer stays open |
| `Space` | Same as Enter | Toggle row; drawer stays open |
| `Esc` | Close, value unchanged | Same |
| Letter | Type-ahead | Type-ahead; selection still requires Space/Enter |

When the drawer has a search input, focus lands in the search on open; arrow keys move from the search into the rows.

Inline-chip remove affordances (multi mode + inline-chips) are reachable by Tab and removable by Enter or Backspace.

**Violations**

- Trigger that doesn't open on Space or Enter — error
- Multi-mode `Enter` that closes the drawer — error
- Single-mode `Space` that doesn't select — warning
- Inline chips not focusable / removable from the keyboard — error

**Examples**

✓ Single: user Tabs to a *Country* Dropdown, Space opens, types `n` to type-ahead to *Norway*, Enter selects, drawer closes.

✓ Multi: user opens *Tags*, presses Space on three options without the drawer closing, Esc dismisses, chips below show the three tags.

---

## Related Rules

- `design-rules/components/drawer.md` — open-state surface.
- `forms/input.md` — anatomy, sizing, modes, content type markers.
- `forms/select.md` — single-pick picker; *When to use Select vs Dropdown vs Combobox* decision tree lives there.
- `forms/combobox.md` — typeable-trigger picker.
- `patterns/dependent-pickers.md` — chained-picker flows.
- `patterns/validation-feedback.md` — form-level error summary.
- `patterns/popover-usage.md` — content type marker popovers.
- `design-rules/components/buttons.md` — chevron icon styling.

---

## Open Questions

- **Inline-chips vs count-in-trigger canonicality** — both valid today; team decision once 2–3 multi-Dropdowns ship.
- **Multi-select with quantity per item** (research ledger 2026-03-12) — out of scope for now; revisit after PR #1758 has been in production for a quarter.
- **Filter-context placeholder extraction** — `Alle {category}` is shared with Select and Combobox; candidate for `patterns/filters.md` once 2–3 ship with the convention.
- **Done / Apply button on multi-mode drawers** — required, recommended, or forbidden? Team decision after 2–3 multi-Dropdowns in production.


---

## forms/input.md

# Input Rules

> **Status: DRAFT — pending team review per decision #46.**

The input is the foundational form field for capturing typed user data — a value, a number, an amount, a date, a search term. It sits at the heart of every form, table cell, and inline editor in Tripletex, so the rules below cover a wide surface: anatomy, sizing, alignment, **type indicators** built into each input type (icons or word-marks that identify what kind of data goes in the field), the three editability modes (editable / disabled / read-only), and a four-type semantic-marker layer (Info / Automation / Warning / Error) that overlays additional meaning onto the field.

**Input types in scope:** `text`, `email`, `number`, `password`, `date`, `search`, `amount`, `money`, `percentage`.

Input is the anchor of the **value-entry** sub-family of form components — controls where the chrome *contains* a typed value. [`textarea.md`](textarea.md) is the multi-line sibling and inherits most of input's conventions. Selection components ([`checkbox.md`](checkbox.md), [`radio-button.md`](radio-button.md), [`toggle-switch.md`](toggle-switch.md)) form a separate sub-family where the chrome *is* the value — documented in their own files with their own anatomy, modes, and interaction states.

**Out of scope:** the selection sub-family (linked above), the date-picker pattern with calendar dropdown ([`period-selectors/date-picker.md`](../period-selectors/date-picker.md) *(pending)*), and search as a wider pattern ([`patterns/search.md`](../../../patterns/search.md) *(pending)*).

**Figma reference:** [Atlas Library — Input](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=427-39373)

---

## Rule: Input anatomy

**Description**

An input has at most three pieces stacked vertically: a label above, the field itself, and helper text below. The label and helper are both optional; the field is the only required element. Label-to-field spacing is fixed at **8px**.

**How to Apply**

Vertical order, top to bottom:

1. **Label** (optional) — sits above the field, separated by 8px. Omitted when the input is used inline (table row, toolbar, popover, multi-input row) and identification comes from the surrounding context.
2. **Field** (required) — the input itself.
3. **Helper text** (optional) — sits below the field; short instruction or example.

Inputs have a sensible min and max width — the field doesn't collapse to nothing in narrow containers and doesn't stretch to fill arbitrary widths. Atlas defaults:

- **`min-width: 160px`** — narrower than this and labels truncate and short values get clipped. Industry-standard floor used by Material (small text fields), Atlassian (small / default text field), and Carbon (small input). Override per-context only when the input genuinely holds a 1–3 character value (e.g. a postal-code or country-code field — see *Open Questions* in `tokens.md` for narrower input tokens).
- **`max-width: 480px`** — wider than this and the field absorbs whitespace without holding more useful content. Common ceiling across form-design literature; matches Atlassian's "large text field" default and is in the range Material / Carbon recommend for comfortable single-line entry. Override per-context only when the input genuinely holds long content (e.g. a comment row, a long URL field).

**Violations**

- Label rendered somewhere other than directly above the field — error
- Label-to-field gap not 8px — warning
- Input collapsed below its min width or stretched past its max width — warning
- Inline input rendering its label twice (once in the surrounding context, once above the field) — warning

**Examples**

✓ Form field with `[Label]` 8px above the field; helper text *"Email address used for invoices"* below.

✓ Editable table cell — no per-cell label; the column header identifies the field.

✗ A label rendered to the *side* of the field — breaks the vertical anatomy.

---

## Rule: Input sizing

**Description**

Atlas inputs come in two sizes. The default 40px matches the medium button so inputs and buttons line up cleanly side-by-side in any form or toolbar. The 32px compact size exists for one specific case — fitting more rows of editable data on screen — and only that case.

**How to Apply**

| Size | Height | Token | Use it for |
|---|---|---|---|
| Default | 40px | `--element-height-large` | Forms, dialogs, page-level inputs |
| Compact | 32px | `--element-height-medium` | Inputs inside compact table rows only |

The compact size is in development and not yet present in the Atlas Library Figma. Until it lands, smaller inputs in production (e.g. Phoenix's *"sats"* column variant) are ad-hoc product variants — not standard Atlas components.

**Violations**

- Compact 32px input used outside a compact table row — error
- Input height other than 40px or 32px — error
- Standalone form using compact 32px inputs to "save space" — error
- Hardcoded input height instead of `--element-height-large` / `--element-height-medium` — error

**Examples**

✓ Default 40px inputs throughout an invoice form.

✓ Compact 32px inputs inside the rows of a posting-suggestion table.

✗ Compact inputs used on a settings page to reduce vertical scroll.

---

## Rule: Input alignment by input type

**Description**

The text inside an input aligns by what it represents. Text-entry types align left so users read from the start of the value, the same direction Norwegian and English are read. Numeric types align right so columns of values line up by place value — currency, quantities, and percentages add up visually when stacked in tables.

**How to Apply**

| Input type | Value alignment |
|---|---|
| `text`, `search`, `date`, `password` | Left |
| `number`, `amount`, `money`, `percentage` | Right |

Date stays left-aligned even though it's a structured value — its components (DD.MM.YYYY) read left-to-right like text.

**Violations**

- Numeric input (`number`, `amount`, `money`, `percentage`) left-aligned — error
- Text-entry input (`text`, `search`, `date`, `password`) right-aligned — error

**Examples**

✓ An amount input in an invoice line right-aligned so columns sum visually.

✓ A search input left-aligned so the query reads forward from the cursor.

✗ A `number` input left-aligned to "match" surrounding text fields — breaks the by-type rule.

---

## Rule: Type indicators

**Description**

Every input type except plain `text` and `number` ships with a built-in **type indicator** — a small icon or word-mark that tells the user what kind of data goes in the field without them having to read the label. The indicator carries weight and expectations: a magnifying glass means search; `NOK` means Norwegian kroner; `%` means percentage; a calendar means date.

Type indicators are the *default* chrome of the input. Content type markers (Info / Automation / Warning / Error) are *added* on top to communicate additional state — see *Content type markers* below for how the two stack.

**How to Apply**

| Input type | Indicator | Kind | Position | Interactive? |
|---|---|---|---|---|
| `text` | None | — | — | — |
| `number` | None | — | — | — |
| `email` | None by default | — | — | — |
| `search` | Magnifying glass | Icon | Opposite side of value (right edge of field, since search value is left-aligned) | No |
| `date` | Calendar | Icon | Right edge (opposite the left-aligned value) | Yes — clicking opens the date picker |
| `password` | Eye / eye-off | Icon | Right edge (opposite the left-aligned value) | Yes — clicking toggles password visibility |
| `amount`, `money` | Currency word-mark (`NOK`, `USD`, etc.) | Word-mark (text) | Left edge (opposite the right-aligned value) | No |
| `percentage` | `%` symbol | Suffix character | Trailing the value at the right edge | No |

**Position convention:** type indicators sit on the **side opposite the value's text alignment** — text-aligned value → indicator on the right; numeric right-aligned value → indicator on the left. This keeps the indicator from visually colliding with the value.

**Exception — suffix indicators.** Indicators that read as suffixes to the value (`%`, unit markers like `stk`) sit at the value's **trailing edge** instead. For a right-aligned numeric value, the suffix sits on the right immediately after the value — same side as the value, not the opposite side.

**Icon set.** Canonical icons (magnifying glass for search, calendar for date, eye / eye-off for password) come from the Atlas icon library — see [`foundations/icons.md`](../../foundations/icons.md) for the icon source and selection process, and [`patterns/icon-usage.md`](../../../patterns/icon-usage.md) for the icon-to-action mappings.

**Violations**

- `search`, `date`, `password`, `amount`, `money`, or `percentage` input rendered without its type indicator — error
- Currency word-mark on the wrong side (right of a right-aligned amount value, instead of left) — error
- `%` placed to the left of a percentage value instead of as a trailing suffix on the right — error
- `search`, `date`, or `password` indicator on the same side as the value's text alignment — error
- `password` visibility-toggle icon rendered as decorative only (non-interactive) — error
- Custom icon used in place of the canonical Atlas icon for the type — error (see [`foundations/icons.md`](../../foundations/icons.md) and [`patterns/icon-usage.md`](../../../patterns/icon-usage.md))

**Examples**

✓ Search input: left-aligned text value with a magnifying-glass icon on the right edge.

✓ Amount input: right-aligned numeric value with `NOK` word-mark on the left edge.

✓ Percentage input: right-aligned numeric value with `%` immediately to the right of the number (suffix exception).

✓ Password input: left-aligned masked value with an eye / eye-off icon on the right edge; clicking toggles visibility.

✓ Quantity input (`number` with `stk` unit): right-aligned numeric value with `stk` immediately after it at the right edge (suffix exception).

✗ Amount input with `NOK` on the right edge — same side as the right-aligned value, collides with the number.

✗ Percentage with `%` on the left of the field.

✗ Password input without the visibility-toggle icon.

✗ Search input using a custom icon instead of the canonical magnifying glass.

---

## Rule: Character counter and maxLength

**Description**

When an input has a hard character limit, the user needs to see how much room they have. A counter shows current characters over the maximum; the field hard-caps at the maximum — typing the next character is a no-op rather than a silent truncation. The counter is purely informational; it doesn't change colour or signal an error.

**How to Apply**

- Show a counter as a small label *"n / max"* beside or below the input.
- The input prevents typing beyond `maxLength` — additional keystrokes are ignored, not silently truncated.
- The counter does not change colour, switch into an error state, or play any other validation role.

**Violations**

- `maxLength` set without a visible counter — warning
- Counter shown without an enforced `maxLength` — warning
- Counter changing colour (red, orange) at or past the limit — error
- Input that silently truncates over `maxLength` instead of hard-capping — error

**Examples**

✓ A 280-character *Comment* field showing `42 / 280` below the input; typing past 280 is ignored.

✗ An input that accepts 1000 characters but truncates the last 720 on submit with no visual feedback.

---

## Rule: Disabled state cursor and explanation

**Description**

A disabled input is one the user could fill in but can't right now — perhaps because it depends on another field's value, or because their role doesn't permit editing it. The user shouldn't be left guessing why.

**How to Apply**

- Use `cursor: default` on a disabled input — **not** `cursor: not-allowed`. The not-allowed cursor reads as *"you've been blocked"*; default reads as *"this just isn't active right now,"* which is closer to the truth.
- Render a tooltip on hover / focus that explains *why* the field is disabled and, where possible, how to make it available (*"Fill in 'Customer' first,"* *"Available to admin users only"*).

**Violations**

- Disabled input using `cursor: not-allowed` — error
- Disabled input with no tooltip explaining why — warning
- Tooltip explanation that doesn't tell the user how to make the field available, when there is a way — note

**Examples**

✓ A *VAT rate* input is disabled until *Country* is filled in; hovering shows *"Choose a country to set the VAT rate."*

✗ A disabled *Discount* field with `cursor: not-allowed` and no tooltip — the user has no idea what's blocked or why.

---

## Rule: Placeholder is not a label

**Description**

A placeholder shows the user *what kind of value goes here* — the format, an example, a hint. It is not the label, and it does not replace one. Using a placeholder as a label disappears the moment the user types, leaving the field unidentified, and screen readers don't reliably treat placeholders as labels.

**Exception:** inline inputs (per *Input anatomy*) have no label slot at all, and a descriptive placeholder may stand in there — see the affordance ladder below.

**How to Apply**

- Placeholder content is a **format hint or example value** — `dd.mm.yyyy`, `you@firm.no`, `Hammer, 250 kr`.
- Placeholder is **not** the field name. Repeating the label inside the placeholder (*"Email"* inside an email field) is noise.
- An empty placeholder is preferred over a forced placeholder.

**Inline-input exception — affordance ladder.** When an input is used inline (no label slot) and the surrounding context doesn't on its own identify the field clearly, reach for the cleanest affordance first:

1. **Leading icon**, when the field has a canonical one — magnifying glass for search, funnel for filter, calendar for date. The icon alone does the identifying.
2. **Descriptive placeholder** — *"Search invoices…"*, *"Filter by name…"*, *"Select period"*. Use this when no canonical icon exists, or when the icon alone is ambiguous.
3. **Descriptive placeholder + leading icon** — when the icon narrows the *kind* of action and the placeholder narrows the *target*.

Whichever rung you land on, the field **must** set `aria-label` for screen readers. This exception only applies when there is no label slot — inputs with a visible label still follow the no-placeholder-as-label rule above.

**Violations**

- Placeholder used as the field label when the field has a label slot — error
- Inline input using a placeholder as the visible identifier without an `aria-label` set — error
- Placeholder repeating the label text verbatim — warning
- Placeholder containing instructions that should be in helper text — warning

**Examples**

✓ An email input with the label *"Email"* and the placeholder `you@firm.no`.

✓ A date input with the label *"Due date"* and no placeholder.

✓ An inline search input in a menu bar with a leading magnifying-glass icon, the placeholder *"Search invoices…"*, and `aria-label="Search invoices"` — no label slot; both visual affordance and screen-reader identification present.

✗ A form field with a label slot left empty, identified only by the placeholder *"Email address"* — the placeholder vanishes the moment the user types.

---

## Rule: Editable, disabled, and read-only modes

**Description**

An input is in one of three modes that say *who is allowed to do what with the value*. The three modes look different on purpose, because they mean different things — and read-only specifically must not look like an input at all.

**How to Apply**

| Mode | What the user can do | How it renders |
|---|---|---|
| **Editable** (default) | Type into the field, change its value | Standard input chrome: border, fill, focus ring on focus |
| **Disabled** | See the value, but not edit it; the field *could* be edited under different circumstances | Field-shaped chrome, greyed; `cursor: default`; tooltip explains why (per *Disabled state cursor and explanation*) |
| **Read-only** | See the value, select-and-copy it, but never edit it | **Plain text — no border, no fill, no field-shaped chrome.** The value is the value. |

The read-only convention is strict: rendering a read-only field as input-shaped misleads the user into thinking they could edit it (or into wondering what's wrong when they can't). If a value can't be edited, present it as a value, not as an input.

**Violations**

- Read-only field rendered with field-shaped chrome (border, fill) — error
- Disabled field rendered without field-shaped chrome (looks like read-only text) — error
- Editable field rendered greyed by default — error
- Read-only field that the user can focus into and type into — error

**Examples**

✓ An invoice number on a posted invoice is shown as plain text, no border — the value can be copied but not changed.

✓ A *VAT rate* input on a draft invoice is greyed out with a tooltip *"Choose a country first"* — disabled, not read-only.

✗ An archived customer's address rendered as a field-shaped, greyed-out input — read-only mistakenly styled as disabled.

---

## Rule: Content type markers

**Description**

A field can carry one extra layer of meaning beyond its value — informational context, that the system filled it in (Automation), that something about the value is suspicious (Warning), or that something is wrong with it (Error). Atlas calls these **content type markers**, and there are exactly four: **Info**, **Automation**, **Warning**, **Error**. A field carries at most one marker at a time.

Each marker renders as an **interactive icon on the side opposite the value's text alignment** (left-aligned value → right-side icon; right-aligned value → left-side icon). The icon supports a popover that gives the *why* behind the state.

These token mappings are shared across **all form components that carry content type markers** (input, textarea, select, period selectors, etc.) so a marker on any field looks the same as on any other.

**How to Apply**

| Marker | Icon | Field surface | Field border | Used for |
|---|---|---|---|---|
| **Info** | Info icon | `--surface-background` (unchanged from default) | `--border-primary` (unchanged from default) | Adding context the user can read on hover, without changing the field's apparent state |
| **Automation** | Sparkle | `--surface-automation-rest` (and `-hover` / `-active` on interaction) | `--border-automation` (and `-hover` / `-focus` on interaction) | A value the system filled in for the user — image-to-text conversion, suggestion accepted, AI-recognised value |
| **Warning** | Warning icon | `--surface-warning-rest` (and `-hover` / `-active`) | `--border-warning` (and `-hover` / `-focus`) | Something about the value is suspicious or worth a second look, but not blocking |
| **Error** | Error icon | `--surface-error-rest` (and `-hover` / `-active`) | `--border-error` (and `-hover` / `-focus`) | Validation failed; the value is invalid as it stands |

The default field colours (no marker) are `--surface-background` for fill and `--border-primary` for border. Info keeps these; the other three shift to their semantic state tokens.

**Marker icon position when a native icon already occupies the opposite side.** When the field already shows a native icon (e.g. the calendar trigger on a date input, the chevron on a dropdown), the marker icon stacks **beside the native icon, on the label side** of it — closer to the value. For a date input (left-aligned value, calendar icon at the right edge), an Error marker renders to the *left* of the calendar icon, between the value and the calendar.

**Marker interaction.** Hovering the marker icon opens a popover with the marker's explanation, per [`patterns/popover-usage.md`](../../../patterns/popover-usage.md). The user reads the why without leaving the form.

**Error has a second valid placement.** As well as the inline icon, an error can be rendered as a **message below the field**, left-aligned with a leading error icon. This is the right choice when the explanation is too long for a popover, or when the user needs to read it without hovering. The other three markers (Info / Automation / Warning) are inline-only.

**Violations**

- More than one marker on the same field at the same time — error
- Marker icon on the same side as the value's text alignment — error
- Marker icon overlapping or replacing a native icon (chevron, calendar) instead of stacking beside it — error
- Marker applied without the matching surface and border tokens (e.g. Warning marker without `--surface-warning-*` / `--border-warning`, Error marker without `--surface-error-*` / `--border-error`, Automation marker without `--surface-automation-*` / `--border-automation`) — error
- Warning or Error marker without a popover (or, for errors, a below-field message) explaining the why — error
- Info marker that changes the field's colour — error

**Examples**

✓ A right-aligned `amount` field with an Automation marker (sparkle icon, purple field) on the left side; hovering shows *"Filled from receipt scan."*

✓ A left-aligned `date` field with a calendar icon at the right; an Error marker stacks just to the left of the calendar icon, and the error message also renders below the field.

✗ A left-aligned `text` field with an Info marker icon also on the left side — same side as the value alignment.

✗ A field showing both a Warning and an Error marker simultaneously.

---

## Rule: Interaction states

**Description**

The interaction state describes what's currently happening to the input — is the user hovering it, focusing it, has the value failed validation? Each state has a distinct visual treatment so the user knows where they are without thinking.

This is orthogonal to *Editable, disabled, and read-only modes* and to *Content type markers*. **Mode** says who's allowed to edit; **markers** say what extra meaning the field carries; **interaction states** say what the user is doing right now.

**How to Apply**

| State | When it applies | Border |
|---|---|---|
| Default | At rest, no interaction | `--border-primary` |
| Hover | Pointer is over the field | `--border-hover` |
| Focus | Field has keyboard focus | **2px** focus ring at `--border-focus`, applied via the Figma Effects preset — see [Focus ring effect](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=19455-15707&t=a5rsetCbVeluqKNi-11). |
| Disabled | Mode is disabled (per *Editable, disabled, and read-only modes*) | `--border-disabled` |
| Read-only | Mode is read-only — rendered as plain text, no field chrome | n/a |
| Error | Content type marker is Error (per *Content type markers*) | `--border-error` (with `-hover` / `-focus` interaction variants) |

**Violations**

- Focused input without a visible focus ring — error
- Focus ring width other than 2px — error
- Hover state visually identical to default — warning
- Error state styling applied without an Error content type marker — error
- Hardcoded border colour instead of using the `--border-*` token family — error

**Examples**

✓ An email input with a clear focus ring (`--border-focus`) when the user tabs to it.

✗ A focus state rendered only as a 1px colour shift, indistinguishable from default at a glance — fails keyboard-navigation visibility.

---

## Related Rules

- [`textarea.md`](textarea.md) — multi-line value-entry sibling; inherits most of this file's conventions.
- [`select.md`](select.md) — single-pick picker; chrome derives from this file's anatomy.
- [`dropdown.md`](dropdown.md) — click-from-list picker; chrome derives from this file's anatomy. Dropdown's chevron is the canonical "native icon" referenced in *Content type markers*.
- [`checkbox.md`](checkbox.md), [`radio-button.md`](radio-button.md), [`toggle-switch.md`](toggle-switch.md) — selection sub-family (chrome *is* the value); separate anatomy, modes, and interaction states.
- [`drawer.md`](../drawer.md) — option-list surface used by pickers; not relevant to plain inputs but useful context for the family.
- [`period-selectors/date-picker.md`](../period-selectors/date-picker.md) *(pending)* — date-picker pattern with calendar dropdown (the `date` input here is the simpler native variant).
- [`patterns/popover-usage.md`](../../../patterns/popover-usage.md) — interactive marker icons open popovers.
- [`patterns/validation-feedback.md`](../../../patterns/validation-feedback.md) — error rendering as a below-field message; validation patterns at large.
- [`patterns/ai-automations/suggestions.md`](../../../patterns/ai-automations/suggestions.md) *(pending)* — the Automation marker is the entry point into the AI / automations pattern.
- [`colors.md`](../../foundations/colors.md) — surface / border / text tokens for Warning, Error, Automation states; the focus-ring token (`--border-focus`).
- [`tokens.md`](../../foundations/tokens.md) — element height tokens (`--element-height-large`, `--element-height-medium`).
- [`typography.md`](../../foundations/typography.md) — text style for labels and helper text; no-italics, no-emojis rules.

---

## Open Questions

- **Compact 32px input** — sized at 32px but not yet present in the Atlas Library Figma or the React component library. The component is planned for a future addition in both Figma and React. Until it ships, smaller inputs in production are ad-hoc product variants — not standard Atlas components.


---

## forms/number-stepper.md

# Number Stepper Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document rules for number steppers — sizing, spacing, states (default, hover, focus, error, disabled), labels, and validation.

---

## forms/radio-button.md

# Radio Button Rules

> **Status: DRAFT — pending team review per decision #56.**

The radio button (often just "radio") is the canonical control for **single-pick selection** in Tripletex — choosing exactly one option from a group of mutually exclusive alternatives. A radio is a discrete choice the user reads and decides on, rather than a value they type, and only carries meaning as part of a group of two or more (see *Always grouped*).

Radio belongs to the **selection** sub-family of form components alongside [`checkbox.md`](checkbox.md) and [`toggle-switch.md`](toggle-switch.md) — controls where the chrome *is* the value. Value-entry components ([`input.md`](input.md), [`textarea.md`](textarea.md), and the input-derived types) are a separate sub-family where the chrome *contains* a typed value. Anatomy, modes, and interaction states are documented locally rather than inherited from `input.md`. Shared conventions (e.g. the 8px control-to-label gap matching input's 8px label-to-field gap) are noted per rule.

For *when* to reach for a radio vs checkbox / toggle / multi-select dropdown, see [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md).

**Out of scope:** when to use radio vs other selection controls (see above); radio-based row picking inside tables (`table.md` *(pending)* — single-pick row selection, keyboard nav, persistence across pagination); content type markers (Info / Automation / Warning / Error) — radio is a single-pick state signal; additional semantic meaning belongs in surrounding helper text, an Alert, or a Banner, not on the 18×18 circle.

**Figma reference:** [Atlas Library — Radio](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-41048) — anatomy, the state matrix, sizing, focus-ring rendering.

---

## Rule: Radio anatomy

**Description**

A radio button is a small circular control with a label to its right. The control is `20 × 20` (component boundary, layout footprint, click target on the circle); inside that boundary the visible circle renders at `18 × 18` with 1px reserved on every side for the focus ring (see *Interaction states*). When selected, a `10 × 10` filled dot sits centred inside the circle. The per-radio label is always present and sits to the right of the control with **8px** between them. Helper text is optional. Radios always exist in a group (see *Always grouped*), and the group carries a separate group-level label above the items — naming what the group is deciding (e.g. *Shipping method* above three delivery-option radios).

**How to Apply**

Horizontal order, left to right:

1. **The control** — `20 × 20` component boundary; inside, the visible circle is `18 × 18` with a 1px border. When selected, a `10 × 10` dot centred inside the circle.
2. **Gap** — exactly `8px` between the right edge of the control's boundary and the start of the label. Same value as `input.md`'s label-to-field gap, applied horizontally here.
3. **Per-radio label** (required) — vertically centred to the control's first line of text.

**Helper text** (optional, per radio) sits in one of two positions — pick one per radio, never both:

- **Below the per-radio label** (default) — beneath the label on its own line. Use for helper text longer than a few words.
- **Inline next to the per-radio label** — same line as the label, separated by a small visual divider (e.g. `( ) Standard delivery · 3–5 business days`). Use when the helper is short and benefits from being on the same row.

**Group-level label** (required, per *Always grouped*) sits 8px above the first radio in the group; names what the group as a whole is deciding.

**Violations**

- Label rendered anywhere other than to the right of the control — error
- Control-to-label gap not 8px — warning
- Radio rendered without an accessible name (no visible label and no `aria-label` / `aria-labelledby`) — error (see *Every radio has an accessible name*)
- Helper text rendered above the per-radio label — warning
- Helper text rendered in both the below-label and inline-next-to-label positions on the same radio — warning
- Selected dot at any size other than `10 × 10` — warning

**Examples**

✓ `( ) Standard delivery` — control on the left, 8px gap, label on the right; selection adds the centred 10×10 dot.

✓ `( ) Express delivery · 1–2 business days` — short helper text inline on the same row, separated by a divider dot.

✓ A *Shipping method* group with three vertical radios (Standard / Express / In-store pickup); group label 8px above the first radio.

✗ Labels stacked above each control instead of to the right.

---

## Rule: Radio states

**Description**

A radio is in one of two behavioural states at any time: **Unselected** or **Selected**. There is no indeterminate state — radio represents a definite single-pick decision at the group level (one option is selected, or none are; never "partially selected"). Each behavioural state has three interaction variants (Default, Hover, Disabled) and a separate Focus state that overlays on either when the radio holds keyboard focus.

**How to Apply**

Token mapping per state — canonical surface and border tokens from the Atlas Library. Use them verbatim; do not hand-roll hex values.

| Behaviour | Interaction | Circle surface | Circle border | Dot |
|---|---|---|---|---|
| Unselected | Default | `--form-rest` | `--border-primary` | none |
| Unselected | Hover | `--form-rest` | `--form-border-hover` | none |
| Unselected | Disabled | `--surface-disabled` | `--border-disabled` | none |
| Selected | Default | `--surface-background` | `--surface-info-active` | `--surface-info-active`, `10 × 10` |
| Selected | Hover | `--surface-background` | `--surface-info-active` (hover darken) | `--surface-info-active` (hover darken) |
| Selected | Disabled | `--surface-disabled` | `--border-disabled` | `--border-disabled` |

The hover-darken values for Selected come from the Atlas Library Figma — they're hover-state variants of `--surface-info-active`. Matches `checkbox.md` *Checkbox states* for sub-family consistency.

**Focus state** overlays on either Unselected or Selected when the radio has keyboard focus: the circle border shifts to `--border-focus`, plus a `2px` solid outline at `--border-focus` rendered `2px` outside the circle. Keyboard-only via `:focus-visible` / `[data-focused]`.

**No indeterminate state.** Radio represents a single-pick choice — "exactly one of these N is the answer." There is no semantic for "partially picked." The closest analogue is "no option selected yet," which is Unselected applied to every radio in the group, not a dedicated state. Indeterminate is checkbox-only (see [`checkbox.md`](checkbox.md) *Checkbox states*).

**Violations**

- Indeterminate-like state on a radio (any glyph or styling that's neither Unselected nor Selected) — error
- Selected radio without the centred dot — error
- Disabled state without `--surface-disabled` fill — error
- Selected radio using a colour other than `--surface-info-active` for the dot and border — error
- Custom indicator glyphs (a square, a checkmark, an icon) instead of the standard centred dot — error

**Examples**

✓ A *Shipping method* group; the user picks *Express* — the circle gains the `--surface-info-active` border and a `10 × 10` centred `--surface-info-active` dot.

✓ A disabled *Payment method* group renders all radios with `--surface-disabled` fill; the previously-selected radio still shows a `--border-disabled` dot so the user can see which option was picked.

✗ A *Quick reply* radio showing a half-filled circle to mean *draft response* — invented state.

Link to Figma: [Atlas Library — `.radio` state matrix](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-40895)

---

## Rule: Radio sizing

**Description**

Atlas radios have one size everywhere: `20 × 20` component boundary, `18 × 18` visible circle, `10 × 10` selected dot. The single-size rule applies on forms, in dialogs, inside tables, in dense filter UIs — the circle is already small, and scaling it smaller would hurt hit targets and visual rhythm; scaling it larger would visually compete with the input field next to it.

**How to Apply**

| Measurement | Value |
|---|---|
| Component boundary (layout footprint, click target on the circle) | `20 × 20` |
| Visible circle (border + fill area) | `18 × 18` |
| Border width | `1px` |
| Selected dot | `10 × 10`, centred |
| Circle border radius | `50%` (fully circular) |
| Indicator | Solid centred dot — no glyph, no icon |

The 1px gap between the visible circle and the component boundary is the reserved space for the focus ring (see *Interaction states*) so focus styling doesn't push surrounding layout.

**Violations**

- Radio rendered at a size other than `20 × 20` boundary / `18 × 18` visible — error
- Selected dot at a size other than `10 × 10` — warning
- A "compact radio" or "large radio" variant — error
- Selected indicator rendered as anything other than a solid centred dot (e.g. a check icon) — error

**Examples**

✓ A `20 × 20`-boundary radio in a settings form lines up with input labels and other form controls.

✓ The same `20 × 20` radio used as a row-pick control in a *Choose shipping address* table.

✗ A scaled-down `14 × 14` radio squeezed into a dense filter UI to save space.

---

## Rule: Always grouped, and group orientation

**Description**

A radio has no meaning when it's the only radio on a page — its semantic ("this is the picked option among mutually exclusive alternatives") requires at least one sibling. The siblings don't need to share a visual container: radios can be distributed across cards, sections, or other surfaces as long as they belong to the same semantic `RadioCollection`.

If you need a single binary choice with no sibling, use a checkbox (deferred-commit opt-in) or a toggle (immediate-commit live state) instead — see [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md). A single radio with no sibling is a bug: the user can select it but cannot deselect it without picking a different option, so a single-radio "decision" is a one-way switch with no off path.

**How to Apply**

- Wrap all radios in a single `RadioCollection`, even when they're visually distributed across multiple surfaces (cards, sections). The `RadioCollection` is the semantic container; visual layout is set via CSS on its children.
- **Group label** sits `8px` above the first radio (or above the visual container holding the first item) — rendered via the `<Label>` slot inside `RadioCollection`. Required for every group.
- **Group-level validation** (`errorMessage` prop on `RadioCollection`) renders below the group via `FieldError` — see *Validation behaviour*.

**Group orientation:**

| Orientation | When | Spacing between items |
|---|---|---|
| Vertical (default) | Long labels, large item counts, top-to-bottom reading order | `8px` |
| Horizontal | Short labels, 2–4 items, fits on one row | `16px` |
| Distributed (card grid) | Each radio sits inside a card; cards laid out in a grid | Whatever the card grid uses — typically `16px` between cards, `16–24px` between rows |

Vertical is the default. Horizontal grouping is opt-in (developer sets `flex-direction: row` on the collection and uses the larger `16px` gap so the row reads as a row rather than a wrapped column). Card-grid layout is also opt-in (collection's default flex overridden with a grid; each radio's position determined by its parent card).

**Violations**

- Single radio rendered on a page with no semantic siblings — error (use checkbox or toggle instead)
- Two or more semantically-grouped radios rendered without a wrapping `RadioCollection` (relying only on the native `name` attribute) — warning
- Group rendered without a group label or accessible group name — error
- Horizontal group with `8px` gap instead of `16px` — warning (reads as a wrapped vertical group)
- Vertical group with `16px` gap — warning (too airy; vertical groups read better at `8px`)

**Examples**

✓ A *Shipping method* group with three vertical radios (Standard / Express / Pickup), `8px` between items, group label *Shipping method* `8px` above the first radio.

✓ A *Sort by* group with two horizontal radios (Newest / Oldest), `16px` between items.

✓ A *Choose your plan* card grid with three pricing cards. Each card has a radio at the top. All three cards are children of one `RadioCollection`. Selecting a radio in one card deselects radios in the others (single-pick across cards).

✗ A single *Subscribe to newsletter* radio in a form — should be a checkbox.

✗ A *Notification preference* group rendered as two separate radios with no `RadioCollection` wrapper — screen readers can't announce the radiogroup.

---

## Rule: Click target spans label and circle

**Description**

Clicking anywhere on the visible label or the circle selects the radio. The label is part of the active click area, not just an associated identifier — it widens the effective target well past the `20 × 20` circle alone, which matters for both pointer accuracy and touch.

**How to Apply**

1. The full label-text element is part of the click target. Native HTML `<label for="...">` association does this automatically; react-aria's `Radio` does it via its render structure.
2. Hover state (see *Radio states*) is visible across the whole label + circle area — cursor over the label gives the same hover affordance as cursor over the circle.
3. Helper text is **not** part of the click target — reading material, not an action surface.
4. **Clicking an already-selected radio is a no-op.** Radio cannot be deselected by clicking it again; deselection happens only by selecting a different radio in the group. This is the load-bearing difference from checkbox (which toggles on every click).

**Touch-target note.** The `20 × 20` circle on its own is below WCAG 2.2 SC 2.5.8's `24 × 24` minimum. With a visible label, the effective target is "circle + 8px gap + label width" — comfortably above the minimum in practice. **Avoid shipping a labelless radio (`aria-label`-only) in a touch context** unless the surrounding container already provides a target above `24 × 24` (e.g. a full-width table row).

**Violations**

- Clicking the label does not select the radio — error
- Hover state shown only when the cursor is over the circle, not over the label — warning
- Helper text rendered as part of the click target — warning
- Labelless radio shipped in a touch-first context without a surrounding ≥`24 × 24` target — warning
- Clicking an already-selected radio deselects it — error (radio is select-only)

**Examples**

✓ A *Standard delivery* radio — clicking the words selects the radio, same as clicking the circle.

✗ A *Region* radio group where clicking the currently-selected radio deselects it — breaks the single-pick contract.

---

## Rule: Every radio has an accessible name

**Description**

A radio without an accessible name is unusable with assistive technology — screen readers announce "radio button, unselected" with no indication of what the user is choosing. Atlas's default is a **visible label** to the right of the circle (see *Radio anatomy*); the carve-out below covers the rare inline cases where surrounding context provides the name.

The `RadioCollection` itself also needs an accessible name (the group label per *Always grouped*) — required in addition to the per-radio labels covered here.

**How to Apply**

Three ways to provide a per-radio accessible name, in order of preference:

1. **Visible label** — the default, required for any radio in a standard form, dialog, settings page, or grouped-decision context. Position per *Radio anatomy*.
2. **Group label as the group's accessible name** — for the `RadioCollection`, the group label is the accessible name for the radiogroup; individual radios still need their own labels per *Radio anatomy*.
3. **`aria-label` or `aria-labelledby` for inline / table contexts** — when the radio lives in a place with no per-radio label slot (table row-pick, dense filter chip, toolbar opt-in). Use `aria-label` for a simple stable string, `aria-labelledby` when an existing element already labels what's being picked.

**Inside a table specifically** (row-pick radios — the most common labelless case in Tripletex tables):

- **Per-row radio** — `aria-label="Select <row identifier>"` where the identifier is the most meaningful piece of data in the row (customer name, invoice number, address). Example: `aria-label="Select address Hovedgaten 5, Oslo"`.
- **Composed or multi-line row identifiers** — prefer `aria-labelledby="<id of the cell that labels the row>"` so the announced name stays in sync with cell text automatically.
- **Group label for the row-pick column** — the table's `<th>` (often *Choose* or no header text) provides the group label; reference it from the `RadioCollection` via `aria-labelledby`.
- **The table `<caption>` is not the accessible name for individual row radios** — captions describe the table as a whole.

The `aria-label` (or the text in the element referenced by `aria-labelledby`) must accurately describe the option — `"Select <something specific>"`, never just `"radio"`, `"choose this"`, or the placeholder column name.

Detailed table row-pick conventions (column placement, keyboard nav, persistence across pagination) live in `table.md` *(pending)*; this rule covers only the accessibility contract.

**Violations**

- Radio rendered with no visible label and no `aria-label` / `aria-labelledby` — error
- Radio using `aria-label` in a context that has a label slot available — warning (visible label preferred)
- `aria-label` text that doesn't describe the option (*radio*, *choose this*, *select*) — error
- Table row-pick radio relying on the table caption alone for its accessible name — error
- `aria-labelledby` pointing at an element that's hidden or doesn't visibly label the row — warning
- `RadioCollection` rendered without a group label or accessible group name — error

**Examples**

✓ `( ) Standard delivery` — visible label, native association inside a *Shipping method* `RadioCollection` with the group label `8px` above.

✓ A *Choose shipping address* table with a row-pick column; each row's radio carries `aria-label="Select address Hovedgaten 5, Oslo"`. The column header `<th>` *Choose* is referenced by the `RadioCollection`'s `aria-labelledby`.

✓ A *Choose customer* row-pick radio using `aria-labelledby="customer-cell-42"` pointing at the row's customer-name cell.

✗ A radio with no visible label and no `aria-label` — fails accessibility.

✗ A row-pick radio with `aria-label="radio"` — uninformative.

---

## Rule: Validation behaviour — group-level only

**Description**

Radio validation lives at the group level: a `RadioCollection` carries an `errorMessage` reflecting a constraint on the whole group (typically *Select an option* or *Choose a shipping method to continue*). **There is no per-radio error styling** — the design choice is to not apply error chrome to individual radios because radio's semantic is group-level (one of N is picked) and per-radio invalidity doesn't compose with mutual exclusivity. The group-level message renders below the group via `FieldError`.

This is the load-bearing difference from [`checkbox.md`](checkbox.md) *Validation behaviour*, which has both per-box error styling and group-level error messages. Radio drops the per-box level.

**How to Apply**

- Set `errorMessage` on the `RadioCollection`. The group's `isInvalid` is set when `errorMessage` is truthy.
- Renders as `FieldError` below the group, below the last child radio.
- Per-radio circle / dot rendering does **not** change on invalid — no red border, no red ring around any individual radio. Radios stay in their normal state-token mapping (see *Radio states*).

**Composition with form-level error summary.** When a form with one or more radio groups fails validation on submit, the group-level error message participates in the form's `ErrorSummary` per [`patterns/validation-feedback.md`](../../../patterns/validation-feedback.md) — same composition path as checkbox group-level errors and input per-field errors. The submit button stays enabled (validation-gate disabling is forbidden across Atlas per the same pattern file).

**Required radio group.** A "you must select an option to proceed" group sets `isRequired` on the `RadioCollection`. Required-empty on submit triggers the group's `errorMessage` (typically *Select an option*) which composes into the form's `ErrorSummary`. No per-radio required indicator on individual radios; the group label carries the required indicator (asterisk or other convention) per Atlas's form-required convention.

**Why no per-radio error.** The structural reason: radios are mutually exclusive, so a "this specific option is invalid" framing conflicts with the pick-one semantic. If a specific option is unavailable, disable it (see *Disabled state*) with a tooltip explaining why; if the constraint is "you must pick something," that's group-level. The canonical edge case for adding per-radio error (e.g. *Card on file is expired* once the user picks Credit card) doesn't appear strongly enough in Tripletex flows to justify the addition yet. Filed as an Open Question below.

**Violations**

- Per-radio red-border or red-outline styling on an individual radio — error (validation is group-level only)
- Validation message rendered as a Banner inside a form instead of a `FieldError` — error (banners-in-forms forbidden per [`banner.md`](../banner.md) and the validation-feedback transitional carve-out)
- Submit button disabled because a required radio group has no selection — error
- Multiple per-radio "errors" inside a single group — error

**Examples**

✓ A required *Shipping method* group with three radios; submitting nothing selected renders the group with `errorMessage="Select a shipping method"` as a `FieldError` below the group.

✓ A *Sort by* filter group with an external constraint (*Sort by date requires a date range to be set*) — group's `errorMessage` reflects that; radios render in their normal state tokens.

✗ A radio with a red border around its circle indicating *you can't pick this one*. If a specific option is unavailable, disable it with a tooltip explaining why.

✗ Submit button disabled because no radio is selected in a required group.

---

## Rule: Disabled state

**Description**

A radio is disabled when the user cannot select it *right now*, but the radio *could* be selected under different circumstances — filling in another field first, changing permission level, switching context. Disabled signals **conditional unavailability**: there is a path to making the radio active, and the rule's job is to tell the user what that path is. For values that are permanently fixed (audit logs, finalised submissions, locked records), use *Read-only state* instead.

**How to Apply**

| Aspect | Spec |
|---|---|
| Visual | Disabled chrome per *Radio states* Disabled row, per behavioural state (Unselected or Selected × Disabled) |
| Circle cursor | `cursor: default` (**not** `cursor: not-allowed`) |
| Label rendering | Greyed alongside the circle, using `--text-disabled` |
| Tooltip | **Required** — explains *why* the radio is disabled and, where possible, *how* to make it available (*Available to admin users only*, *Available once Country is filled in*) |
| ARIA | `disabled` attribute on the underlying input |
| Focusable | **No** — Tab skips disabled radios; screen readers announce as dimmed / unavailable |
| Click target | Inert — clicks on the circle or label have no effect |

The `cursor: not-allowed` reads as "you've been blocked"; `cursor: default` reads as "this just isn't active right now," which is closer to the truth and matches the conditional-unavailability framing.

**Group-level vs per-radio disabled.** Setting `isDisabled={true}` on `RadioCollection` disables every child and visually greys the whole group (group label + all radios). Setting `isDisabled={true}` on an individual `Radio` disables only that option; siblings remain selectable.

**Violations**

- Disabled radio using `cursor: not-allowed` — error
- Disabled radio without a tooltip explaining why — warning
- Tooltip that doesn't tell the user how to make the radio available, when there is a way — note
- Disabled used for a permanently-fixed value with no path to selecting — warning (use Read-only instead)
- Disabled radio using `aria-readonly="true"` instead of the `disabled` attribute — error
- Disabled radio that's focusable (Tab lands on it) — error

**Examples**

✓ A *Payment method* group where *Direct debit* is disabled until the user fills in an IBAN; hovering shows *Add an IBAN to enable direct debit*.

✓ A *Workflow stage* group disabled at the collection level on a locked-record view; tooltip on the group: *Unlock the record to change workflow stage*.

✗ A *Shipping method* radio on a finalised order rendered as disabled — should be Read-only; the user cannot change the order's shipping method under any circumstance.

✗ A disabled radio using `cursor: not-allowed` and no tooltip.

---

## Rule: Read-only state

**Description**

A radio is read-only when the value is fixed and the user cannot select a different option under any path forward. Read-only signals **permanent unavailability** — audit logs showing past picks, finalised submissions, locked records, summary views of decisions already made.

**Read-only currently shares the same visual treatment as Disabled.** No distinct read-only visual exists yet (filed in Open Questions alongside the same item for Checkbox). The behavioural differences (no tooltip, Tab-focusable, `aria-readonly`) carry the distinction at the keyboard and assistive-tech layers; surrounding context (an audit-log row, a finalised order) carries it for sighted users.

**How to Apply**

| Aspect | Spec |
|---|---|
| Visual | Same as Disabled (interim) — per *Radio states* Disabled row, per behavioural state |
| Circle cursor | `cursor: default` |
| Label rendering | Same as Disabled (interim) — greyed alongside the circle |
| Tooltip | **None** — no "how to enable" exists for a permanently-fixed value; surrounding context provides the meaning |
| ARIA | `aria-readonly="true"` on the underlying input (**not** the `disabled` attribute) |
| Focusable | **Yes** — Tab lands on read-only radios; screen readers announce "read-only radio button, selected / unselected" |
| Click target | Inert for selection, but remains in the focus order so keyboard and screen-reader users can navigate to read the value |

**Why focus matters for read-only.** Read-only is part of the displayed *information*. Keyboard users need to be able to navigate to read-only values to read them; screen-reader users need the value announced. Skipping read-only fields hides information.

**Group-level vs per-radio read-only.** The common case is a whole `RadioCollection` rendered as read-only — a *Shipping method* group on a finalised order, all radios rendered with read-only chrome, the selected one still visually distinguished by its dot. Per-radio read-only is unusual and only applies when one option in an otherwise-editable group is permanently locked.

**Violations**

- Read-only radio using the `disabled` attribute instead of `aria-readonly="true"` — error
- Read-only radio not focusable (Tab skips it) — warning
- Read-only radio carrying a tooltip explaining why — note (no tooltip needed; surrounding context provides the meaning)
- Read-only used for conditionally-unavailable values where the user could make the radio selectable — warning (use Disabled instead)
- Read-only radio with `cursor: not-allowed` — error

**Examples**

✓ An audit-log row showing a *Shipping method* group with *Express* selected, the whole group rendered read-only — focusable, no tooltip, screen readers announce "read-only radio button, Express, selected."

✓ A finalised order summary showing the picked *Payment method* as a read-only group.

✗ An audit-log *Shipping method* group rendered with the `disabled` attribute on every radio — the user cannot Tab to read which one was picked.

✗ A read-only radio carrying a tooltip *This is a historical record* — surrounding context already provides that meaning.

---

## Rule: Interaction states

**Description**

The interaction state describes what's currently happening to the radio — hover, focus, disabled, read-only. Each state has a distinct visual treatment so the user knows where they are without thinking. **Focus must be visibly distinguished from default** — keyboard-only, via `:focus-visible` / `[data-focused]`, never on mouse-click.

**How to Apply**

| State | When it applies | Visual treatment |
|---|---|---|
| Default | At rest, no interaction | State tokens from *Radio states* (Default row per behaviour) |
| Hover | Pointer over the label or circle | State tokens from *Radio states* (Hover row per behaviour) |
| Focus | Circle has keyboard focus | Circle border becomes `--border-focus`; outer focus ring renders as a `2px` solid outline at `--border-focus`, `2px` outside the circle |
| Disabled | Mode is Disabled (see *Disabled state*) | State tokens from *Radio states* (Disabled row per behaviour) |
| Read-only | Mode is Read-only (see *Read-only state*) | Same as Disabled (interim) |

The focus-ring rendering differs slightly from checkbox's (radio uses a `2px` solid outline, checkbox uses a 1px border with 3px offset) — this is the current React implementation and is preserved as-is unless a future Atlas focus foundation reconciles the two state-shaped controls. Filed in Open Questions.

**Focus is keyboard-only.** The ring renders only on keyboard focus (`:focus-visible` / `[data-focused]`) — clicking the circle with a pointer does not show it, by design.

**No per-radio Invalid state.** Validation lives at the group level (see *Validation behaviour*). The group's `FieldError` is the visual signal; individual radios stay in their normal state-token mapping.

**Violations**

- Focused radio without a visible focus ring — error
- Focus ring shown on mouse-click (any-focus styling instead of `:focus-visible` / `[data-focused]`) — warning
- Hover state visually identical to default — warning
- Per-radio Invalid styling applied (red border on an individual radio) — error (use group-level `errorMessage` instead)

**Examples**

✓ Tabbing onto a radio in a group shows a clear outer focus ring around the circle; clicking it with the mouse does not.

✗ A focused radio indistinguishable from default — fails keyboard-navigation visibility.

---

## Related Rules

- [`checkbox.md`](checkbox.md) — selection sub-family sibling (binary or multi-pick selection). Radio mirrors checkbox's structure with four key differences: always grouped, no indeterminate, no per-radio error styling, circle / dot visuals instead of square / check.
- [`toggle-switch.md`](toggle-switch.md) — selection sub-family sibling (immediate-commit live state).
- [`input.md`](input.md) — anchor of the value-entry sub-family; radio is in the broader form family but documents its own anatomy, modes, and interaction states.
- [`textarea.md`](textarea.md) — multi-line value-entry sibling of input.
- [`../../../patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md) — selection sub-family decision guide: radio vs checkbox vs toggle vs dropdown.
- [`../table.md`](../table.md) *(pending)* — table row-pick uses radios; canonical placement and keyboard nav live there.
- [`../../../patterns/validation-feedback.md`](../../../patterns/validation-feedback.md) — radio group-level errors compose into the form's `ErrorSummary`.
- [`../banner.md`](../banner.md) — banners-in-forms forbidden; cross-referenced by *Validation behaviour*.
- [`../../foundations/colors.md`](../../foundations/colors.md) — surface, border, text tokens used in *Radio states*.

---

## Open Questions

- **Figma library — Focus and Read-only state variants missing.** The `.radio` state-matrix frame ([484:40895](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-40895)) lays out six variants but lacks Focus and Read-only. Same gap exists on `.checkbox` ([484:40913](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-40913)). Astro design system team.
- **React `Radio.css` token migration.** Component still uses legacy `--atl-color-*` tokens (e.g. `--atl-color-grey-40`, `--atl-color-blue-100`); should migrate to semantic tokens documented in *Radio states*. Coordinates with the same Checkbox migration filed in PR #605.
- **Atlas Radio `isReadOnly` API addition.** *Read-only state* documents the mode but the React API currently omits `isReadOnly`. Coordinates with the same Checkbox follow-on.
- **Distinct read-only visual treatment for Radio (and Checkbox).** *Read-only state*'s How to Apply notes the read-only / disabled visual collision as an interim; design team to articulate distinct read-only visuals for both state-shaped controls together.
- **Forms-family read-only consistency.** `input.md` *Read-only mode* renders read-only inputs as plain text; selection sub-family controls (`checkbox.md`, `radio-button.md`) render read-only with disabled-shaped chrome. Reconciliation tracked alongside checkbox's identical item.
- **`colors.md` token coverage — `--form-rest` / `--form-border-hover` vs `--surface-*` family.** Same conceptual surface, different token names; one of them is canonical and the other should be retired. **Figma must align first** — the same hex `#f7f8fc` appears as *Form/Rest* in Checkbox's Figma and *Surface/Background* in Radio's Figma. Without Figma alignment, the docs and code can't converge. Astro design system team (Figma alignment as prerequisite).
- **Per-radio error styling — revisit if a Tripletex use case emerges.** Atlas keeps validation group-level only (see *Validation behaviour*). Revisit if a specific picked option becomes invalid distinct from selection (canonical example: *Card on file is expired* once the user has already picked Credit card). Would need a per-radio error visual (likely a red ring matching checkbox's per-box pattern), corresponding ARIA, and an update to *Validation behaviour*.
- **Focus-ring rendering mismatch with Checkbox.** Radio uses a `2px` solid outline; checkbox uses a 1px border with 3px outset. Two sub-family siblings, two focus-ring patterns. Reconcile when a future Atlas focus foundation lands; tracked alongside the same Checkbox item.


---

## forms/select.md

# Select Rules

> **Status: DRAFT — pending team review per decision #61.**

The Select is the simplest picker — a trigger that opens a short drawer of options, lets the user pick exactly one, and writes the chosen value back to the trigger. Use a Select when the list is short, fixed, and single-pick.

Select inherits anatomy / sizing / modes / content type markers from [`forms/input.md`](input.md), and the drawer surface from [`design-rules/components/drawer.md`](../drawer.md) in its simplest configuration (single-pick, no checkboxes, no search). Atlas pickers never use native HTML `<select>` rendering — the drawer is always Atlas-owned.

For longer lists or multi-pick, see [`forms/dropdown.md`](dropdown.md). For typeable triggers with autocomplete, see [`forms/combobox.md`](combobox.md).

**Figma reference:** [Atlas Library — Select](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-40687)

---

## Out of scope

Inherits from `forms/input.md`:

- Label-to-field anatomy.
- Sizing (40px default, 32px compact for table rows only).
- Editable / disabled / read-only modes.
- Content type markers.

Inherits from `design-rules/components/drawer.md`:

- Drawer anatomy, positioning, visual treatment.
- Width and text overflow.
- Row content, row states.
- Scroll behaviour, z-stacking.
- Outside-click and Esc dismissal, base keyboard navigation.

Out of scope of this file: multi-select, search (use Dropdown); typeable triggers (use Combobox); date pickers.

---

## Rule: Select anatomy

**Description**

The trigger shows the value (or placeholder) followed by a trailing chevron.

**How to Apply**

Trigger, left to right:

1. Value or placeholder (see *Closed-state placeholder*).
2. Trailing chevron — 20px square, 8px gap from the value, rotates 180° on open. Uses the standard interactive-icon token from `foundations/colors.md`.

Content type marker (per `forms/input.md` Rule 8) stacks beside the chevron on the label side.

**Violations**

- Trigger rendered without a chevron — error
- Chevron not in the trailing position — warning
- Value right-aligned in the trigger — warning (left-aligned for text; right-aligned is for number/amount inputs)

**Examples**

✓ `[Norway ▾]`.

✓ `[Ikke valgt ▾]` when no value is picked.

✗ Value without a chevron — looks like a read-only field.

---

## Rule: Closed-state placeholder

**Description**

Wording differs by context (form input vs filter). The semantic of "no selection" flips between them, so the wording must match. Norwegian-first with English fallback.

**Form input context** (user is entering data; no selection = not picked yet):

- Default: `Ikke valgt` / *Not selected*.
- Empty placeholder allowed inline (table row, toolbar, popover) when the field is optional and the surrounding context makes "no selection" obvious.

**Filter context** (user is narrowing a list; no selection = all match):

- Default: `Alle {category}` — `{category}` is the plural noun (`Alle attestanter`, `Alle kategorier`, `Alle leverandører`).
- Empty placeholder forbidden — reads as "no filter applied → nothing shown," the wrong mental model.

Placeholders use the same typography as a value, rendered at `--text-muted`.

**Violations**

- Form-input Select empty when required without surrounding context — error
- Filter Select empty — error
- Filter Select with `Ikke valgt` — error
- Form-input Select with `Alle {category}` — error
- Custom placeholder string that diverges from `Ikke valgt` / `Alle {category}` — warning (raise in `#astro_reception` to add to Text Vault)

**Examples**

✓ Form input: a *Currency* field shows `Ikke valgt` until picked.

✓ Filter: an *Approver* filter shows `Alle attestanter`.

✓ Inline form input, empty placeholder: a table row's *Status* cell shows nothing in the trigger when unpicked — the column header and the chevron carry the affordance.

✗ A required *Country* field on a settings page renders empty.

✗ A filter Dropdown shows `Ikke valgt` — reads as "nothing matches" instead of "no filter."

---

## Rule: Drawer and single selection

**Description**

Activating the trigger opens the drawer per `drawer.md` in its simplest configuration: plain rows (no checkboxes), no search, single-pick. Picking closes the drawer.

**How to Apply**

1. Activation (mouse click, Space, Enter) opens the drawer.
2. Drawer rows are plain — no checkboxes (those are Dropdown multi-mode per `forms/dropdown.md`). Rows can be text-only, text + 20px icon, or text + 20px avatar per `drawer.md` *Row content*.
3. The previously-selected option (if any) shows a trailing checkmark per `drawer.md` *Row states*.
4. Picking closes the drawer; value writes to the trigger; focus returns to the trigger.
5. Dismissal (outside-click, Esc) leaves the value unchanged per `drawer.md` *Outside-click and Esc dismissal*.

**Violations**

- Select supporting multiple selections — error (use Dropdown's multi mode)
- Select drawer with leading checkboxes — error (checkboxes signal multi-mode)
- Select drawer with a search input — warning (if you need search, use Dropdown)
- Picking that doesn't close the drawer — error
- Selected indicated by background highlight instead of trailing checkmark — warning

**Examples**

✓ User clicks *Currency*; drawer opens with `NOK / EUR / USD / GBP` (no checkboxes, no search); clicks `EUR`; drawer closes; trigger shows `EUR`. On re-open, *EUR* carries a trailing checkmark.

✗ A Select that lets the user check multiple options before submitting.

✗ A Select drawer with a search input — long-list-with-search is Dropdown's job.

---

## Rule: Disabled trigger when no content to show

**Description**

If the Select has nothing to render (empty list, async returned zero, context not ready), the trigger is disabled with a tooltip. The drawer never opens.

**How to Apply**

- Disabled-state mechanics from `forms/input.md` *Disabled state*.
- Tooltip names the reason and any path to availability (*"No currencies configured for this account"*, *"Pick a role first"*). Owned by Text Vault.

For chained-picker flows (Product → Category → Tax code), see `patterns/dependent-pickers.md`.

**Violations**

- Enabled trigger that opens to an empty drawer — error
- Disabled trigger without a tooltip — warning
- Disabled trigger still activatable by Space / Enter — error

**Examples**

✓ A *Currency* Select on an account with no configured currencies — trigger disabled with *"No currencies configured for this account"*.

✗ Enabled trigger opens to an empty drawer.

---

## Rule: Keyboard navigation

**Description**

Bindings match native `<select>` so keyboard and screen-reader habits carry over.

**How to Apply**

| Key | Behaviour |
|---|---|
| `Space` or `Enter` (closed trigger) | Opens the drawer |
| `Arrow Down` / `Arrow Up` (open drawer) | Next / previous row |
| `Home` / `End` (open drawer) | First / last row |
| `Enter` (focused row) | Selects; closes; focus returns to trigger |
| `Esc` (open drawer) | Closes, value unchanged |
| Letter (open drawer) | Type-ahead; repeated letters cycle matches |

Focus returns to the trigger on close unless the user Tab'd to another control during the open state.

**Violations**

- Select that traps focus inside the drawer — error
- Type-ahead not implemented — warning
- Arrow keys that don't navigate rows — error

**Examples**

✓ User Tabs to a *Country* Select, Space opens, types `n` (jumps to *Netherlands*), types `n` again (jumps to *Norway*), Enter picks.

✗ Tab inside the open drawer moves focus to the next form field instead of letting the user navigate rows.

---

## Rule: When to use Select vs Dropdown vs Combobox

**Description**

Atlas has three pickers, distinguished by **interaction model**.

- **Select** — short fixed list, click to pick, single only. No search, no typing.
- **Dropdown** — list (single or multi), click to pick, optional search-in-drawer for longer lists.
- **Combobox** — typeable trigger with autocomplete suggestions, single or multi, optional create-new for values not in the list.

**How to Apply**

Pick by answering two questions in order:

1. **Is typing into the trigger the primary interaction?** If yes → **Combobox**.
2. **Otherwise the user picks by clicking.** Then:
   - Short fixed list, no search, single-pick → **Select**.
   - Long list (needs search) or multi-pick → **Dropdown**.

| If… | Use |
|---|---|
| Short fixed list, click, single-pick | Select |
| List (single or multi), click, optional search-in-drawer | Dropdown |
| Typeable trigger with autocomplete (single or multi, optional create-new) | Combobox |

**Violations**

- Multi-select wrapped in a Select trigger — error
- Select with 50+ options and no search affordance — warning (use Dropdown's search)
- Combobox where a click-only Dropdown suffices — warning (typeable trigger misleads users into thinking they can type a value when only predefined options are valid)

**Examples**

✓ Select: *Currency* — 4 currencies, single, short.

✓ Dropdown (single + search): *Country* — 195 entries, single, search-in-drawer.

✓ Dropdown (multi): *Tags* filter — pick several from the drawer.

✓ Combobox (single): *Customer* — user types the name, autocomplete from existing customers, create-new if enabled.

✓ Combobox (multi): *Tags* on a customer record — attach existing tags or create new by typing.

✗ A *Country* Select with 195 options and no search.

✗ A *Currency* Combobox when no new currencies will ever be added.

---

## Related Rules

- `forms/input.md` — anatomy, sizing, modes, content type markers.
- `design-rules/components/drawer.md` — open-state surface.
- `forms/dropdown.md` — click-from-list picker (single or multi).
- `forms/combobox.md` — typeable-trigger picker.
- `patterns/dependent-pickers.md` — chained-picker flows.
- `patterns/validation-feedback.md` — form-level error summary.
- `patterns/popover-usage.md` — content type marker popovers.
- `design-rules/components/buttons.md` — chevron icon styling.

---

## Open Questions

- **Compact 32px Select inside table rows** — `input.md` Rule 2 documents the compact size as pending Figma; confirm the Select compact variant.
- **Filter context placeholder extraction** — `Alle {category}` is shared with Dropdown and Combobox; candidate for `patterns/filters.md` once 2–3 ship with the convention.
- **Async option loading** — Select assumes a closed, known list. Async (rare for Select, common elsewhere) follows `forms/combobox.md` once it lands.
- **Combobox is shipped but unrule'd** — see `forms/combobox.md` (currently a stub). Legacy storybook reference: [Atlas Combobox](https://atlas.tripletex.dev/#/Components/ComboBox).


---

## forms/textarea.md

# Textarea Rules

> **Status: DRAFT — pending team review per decision #47.**

The textarea is the multi-line form field — used wherever the user types more than a sentence (comments, descriptions, notes, replies, free-form text). Textarea is **block-level only** (see *Block-level only — no inline use* below).

Textarea is the multi-line sibling of [`input.md`](input.md) in the **value-entry** sub-family of form components. Selection components ([`checkbox.md`](checkbox.md), [`radio-button.md`](radio-button.md), [`toggle-switch.md`](toggle-switch.md)) are a separate sub-family with their own conventions.

**Shared with [`input.md`](input.md):** anatomy, modes, interaction states, placeholder, character counter, content type markers. This file documents only what differs.

**Figma reference:** [Atlas Library — Textarea](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=427-39373)

---

## Rule: Resize behaviour

**Description**

A textarea is resizable in principle, but unconstrained resize creates more problems than it solves. Horizontal resize breaks page layouts that weren't designed for the new width; the corner resize handle is the most-misclicked element in modal-comment textareas — users grab it instead of clicking inside the field, lose their typing position, and sometimes lose their text. Atlas defaults to a single safe resize axis and disables resize entirely in modals.

**How to Apply**

| Context | `resize` value |
|---|---|
| Default (any non-modal textarea) | `vertical` |
| Inside a modal | `none` (required, no opt-out) |
| `horizontal` or `both` | Never |

The default `vertical` is the safe choice; horizontal resize is forbidden because it breaks layouts that weren't designed for it. In modals, the corner handle is enough of a misclick hazard that resize is disabled outright — `minRows` / `maxRows` (see *Sizing by rows*) cover the height needs.

**Violations**

- Textarea with `resize: horizontal` — error
- Textarea with `resize: both` — error
- Textarea inside a modal with any `resize` value other than `none` — error
- Non-modal textarea with `resize: none` set without a designer-articulated reason — note (allowed in tight contexts; flag as a question if the rationale isn't clear)

**Examples**

✓ A *Description* textarea on a settings page with `resize: vertical` — the user can pull it taller if they need more room.

✓ A comment textarea inside a modal with `resize: none` — no resize handle to misclick.

✗ A textarea on an invoice line with `resize: both` — the user pulls it wider, breaking the line layout.

---

## Rule: Sizing by rows

**Description**

A textarea's height is set by row count, not pixels. `minRows` is the height reserved at rest; `maxRows` caps how tall the field can grow before scrolling kicks in. Auto-grow between min and max keeps the field roomy for what the user is writing without pushing the rest of the form off-screen.

**How to Apply**

- **`minRows`** — default `3`. Override when the field is intended to be taller at rest (e.g. a *Notes* field that explicitly invites long entries).
- **`maxRows`** — set per use case by the caller; no global default. Comment fields ~6–8, descriptions ~10–15, long-form notes higher.
- **Auto-grow between min and max** — typing past `minRows` grows the textarea row by row until it hits `maxRows`.
- **At `maxRows`, scroll inside the textarea** — never grow beyond `maxRows` to keep all content visible.
- **No compact size** — textarea has one size; for compact contexts use `input` per [`input.md`](input.md). See *Block-level only — no inline use* below.

**Violations**

- Textarea without an explicit `maxRows` — warning (the cap is what stops runaway growth)
- `minRows` greater than `maxRows` — error
- Textarea growing past `maxRows` to keep all content visible — error
- A "compact textarea" variant — error (textarea has one size; for compact contexts use `input`)

**Examples**

✓ A comment textarea with `minRows={3}` and `maxRows={8}` — short by default, grows up to 8 rows, then scrolls.

✓ A *Description* field on a product form with `minRows={5}` and `maxRows={15}` — invites longer content from the start.

✗ A textarea growing to 30 rows tall on a tightly-packed form, pushing the action buttons below the fold.

---

## Rule: Block-level only — no inline use

**Description**

Textarea is a block-level form field only. It is **not** used inline — never inside a table cell, popover, multi-input row, or other dense / constrained layout. When the user needs multi-line content in a constrained surface, route them to one of the alternatives below.

This matches the industry pattern across Material, Atlassian, Carbon, Primer, and Polaris — all treat textarea as block-level only and route multi-line entry from constrained surfaces to a focused editing surface (typically a modal or expanded row).

**How to Apply**

When the surface needs multi-line entry but can't accommodate a full block-level textarea, use one of:

1. **A modal** (default) — open a focused editor with a full-size textarea inside, per [`../modal.md`](../modal.md). The right choice for almost every case where the content is rich enough that the user benefits from a dedicated editing surface.
2. **An expanded row / detail panel** (fallback) — expand the row to reveal a full-size textarea below the row's main content (inline-on-the-page, not inline-in-a-cell). Use when a modal would interrupt the surrounding context the user still needs to see.

For single-line text in a constrained surface, use [`input.md`](input.md)'s inline-use affordances instead.

**Violations**

- Textarea rendered inside a table cell — error
- Textarea rendered inside a multi-input row alongside other fields on the same row — error
- Textarea rendered inside a popover — error (popovers are informational, not editing surfaces; route to a modal instead)
- Textarea rendered inline in a dense layout because a modal *"felt heavy"* — error (use the expanded-row fallback)

**Examples**

✓ A comment column in a table that needs multi-line entries: a *Comment* icon opens a modal with a full textarea inside.

✓ A note attached to a row that's longer than one line: the row expands inline, revealing a block-level textarea below the row's main content.

✗ A textarea rendered directly inside a 32px-tall table cell.

✗ A multi-input row where one of the inputs is a textarea.

---

## Rule: Line-break preservation

**Description**

A textarea exists so users can write across multiple lines. Those line breaks are content, not formatting noise — a list of three items separated by newlines means three items, not one paragraph. When the value is rendered elsewhere (a report, a summary list, an export, an inline display), newlines must be preserved.

**How to Apply**

- Render the textarea's value with `white-space: pre-wrap` (or equivalent) so newlines and consecutive whitespace are preserved on display.
- Don't strip or join newlines on submit, on persist, or on render.
- Reports, exports (PDF, CSV, Excel), and inline displays render the field's value with line breaks intact.

**Violations**

- Textarea value rendered with newlines stripped or joined — error
- Textarea value persisted with newlines stripped — error
- Report or export rendering a textarea field as a single-line concatenation — error

**Examples**

✓ A *Notes* field with three bullet-style lines of text renders as three lines in the invoice report.

✗ The same field rendered as `"line one line two line three"` in the report — newlines silently joined.

---

## Rule: Newline vs commit key

**Description**

Inside a textarea, the user is writing — Enter is for new paragraphs, not for submitting. The keyboard contract differs from a single-line input, where plain Enter is the natural commit key. Atlas mirrors the platform-standard convention: Enter inserts, Cmd / Ctrl+Enter commits.

**How to Apply**

| Key | Inside a textarea |
|---|---|
| Enter | Inserts a newline |
| Cmd+Enter (macOS) / Ctrl+Enter (Windows, Linux) | Commits the textarea's primary action — submit the form, post the comment, save the modal |
| Esc | Standard dismiss for the surrounding surface (modal close, popover close); does not clear the textarea content |

The Cmd / Ctrl+Enter contract matches [`modal.md`](../modal.md) *Modal keyboard interactions*. When a textarea is the primary input of a modal, the modal's Enter / Cmd+Enter behaviour from that rule governs.

**Violations**

- Plain Enter inside a textarea triggering form submit instead of inserting a newline — error
- Cmd / Ctrl+Enter not bound to the primary action when a textarea is the primary input of a form or modal — warning

**Examples**

✓ A comment modal where Enter inserts a newline and Cmd+Enter posts the comment.

✗ A *Description* textarea on a settings page where pressing Enter triggers Save and the user loses their place mid-paragraph.

---

## Rule: Content type markers

**Description**

Textarea uses the same four content type markers (Info / Automation / Warning / Error) as input — same tokens, same mutual exclusivity, same popover interaction. See [`input.md`](input.md) *Content type markers* for the full contract. This rule documents only the textarea-specific position adjustment.

**How to Apply**

- The four markers, their surface / border tokens, popover behaviour, and Error's below-field message placement are documented in [`input.md`](input.md) *Content type markers*. Apply identically.
- **Position is textarea-specific.** Textareas are always left-aligned, so the marker icon sits on the right edge. **Pin the icon to the top of the field, not vertically centred** — so it stays in view as the textarea grows past its initial height.

**Violations**

- Marker icon vertically centred on the field instead of pinned to the top — error (a centred icon disappears as the textarea grows)
- Other violations from `input.md` *Content type markers* (multiple markers, wrong tokens, missing popover, etc.) apply identically.

**Examples**

✓ A textarea with an Automation marker (sparkle icon top-right, purple field) on a comment field auto-suggested by the AI assistant; hover shows *"Drafted from your previous reply pattern."*

✓ A *Notes* textarea failing validation: Error marker icon pinned top-right + error message rendered below the field.

✗ Marker icon vertically centred on the field — disappears the moment the user types past the first row.

---

## Related Rules

- [`input.md`](input.md) — single-line value-entry sibling; this file documents textarea-specific behaviour on top of input's shared rules (the slim list at the top of the file enumerates what's shared).
- [`checkbox.md`](checkbox.md), [`radio-button.md`](radio-button.md), [`toggle-switch.md`](toggle-switch.md) — selection sub-family (chrome *is* the value); separate anatomy and modes.
- [`../modal.md`](../modal.md) — *Modal keyboard interactions* (Cmd / Ctrl+Enter commit) and *Modal isolation* (no sticky parts) both interact with textareas inside modals.
- [`../../../patterns/popover-usage.md`](../../../patterns/popover-usage.md) — interactive marker icons open popovers.
- [`../../../patterns/validation-feedback.md`](../../../patterns/validation-feedback.md) — error rendering as a below-field message.
- [`../../../patterns/ai-automations/suggestions.md`](../../../patterns/ai-automations/suggestions.md) *(pending)* — Automation marker is the entry point into the AI / automations pattern.
- [`../../foundations/colors.md`](../../foundations/colors.md) — surface / border tokens for Warning, Error, Automation states (inherited via the Content type markers contract).

---

## Open Questions

- **React `TextAreaField` default** — currently defaults `resize='both'`, which contradicts the *Resize behaviour* rule. The prop default should be `vertical`. Tracked in `TODO.md` as a follow-on for the Astro design system team.
- **`forms.md` extraction** — once 2–3 components in this stack expose real cross-cutting form-layout duplication (grouping, spacing between fields, label placement variants), extract into a shared `forms.md`. Until then, restate per component or cross-ref `input.md`.


---

## forms/toggle-switch.md

# Toggle Switch Rules

> **Status: DRAFT — pending team review per decision #58.**

The toggle is the canonical control for **immediate-commit binary system state** in Tripletex — turning a setting or feature on and off where the change takes effect the moment the user clicks, with no save or submit button required. Toggles are the right choice for system preferences, feature enablement, dark mode, notification preferences, and similar binary settings where users expect instant results.

Toggle belongs to the **selection** sub-family of form components alongside [`checkbox.md`](checkbox.md) and [`radio-button.md`](radio-button.md) — controls where the chrome *is* the value. Value-entry components ([`input.md`](input.md), [`textarea.md`](textarea.md), and the input-derived types) are a separate sub-family where the chrome *contains* a typed value. Anatomy, modes, and interaction states are documented locally rather than inherited from `input.md`. Shared conventions (e.g. the 8px control-to-label gap matching input's 8px label-to-field gap) are noted per rule.

For *when* to reach for a toggle vs checkbox / radio / dropdown, see [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md).

**Out of scope:** when to use toggle vs other selection controls (see above); toggles and checkboxes in table cells to mark item state — explicitly discouraged in [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md); content type markers (Info / Automation / Warning / Error) — toggle is a binary state signal; additional semantic meaning belongs in surrounding helper text, an Alert, or a Notification, not on the track itself.

**Figma reference:** [Atlas Library — Toggle](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-41084) — anatomy, the state matrix, sizing, focus-ring rendering, and toggle-group layout.

---

## Rule: Toggle anatomy

**Description**

A toggle is a pill-shaped track with a sliding thumb and a label to its right. The track is `36 × 20` (component boundary, layout footprint, click target on the track); inside that boundary the visible track renders at `36 × 18` with 1px reserved on the top and bottom edges for the focus ring (see *Interaction states*). The thumb is a `14 × 14` white circle inset `2px` from the track edge, sliding from the left position (Unchecked) to the right (Checked). The per-toggle label is always present and sits to the right of the track with **8px** between them. Helper text is optional. Multiple toggles displayed together (see *Multiple toggles together*) are independent settings in a shared layout, each with its own per-toggle label.

**How to Apply**

Horizontal order, left to right:

1. **The track** — `36 × 20` component boundary; inside, the visible pill track is `36 × 18`, fully rounded (`border-radius: 18px`). The thumb is a `14 × 14` white circle, `2px` inset from the track edge; it slides horizontally between the Unchecked (left) and Checked (right) positions.
2. **Gap** — exactly `8px` between the right edge of the track's boundary and the start of the label. Same value as `input.md`'s label-to-field gap, applied horizontally here.
3. **Per-toggle label** (required) — vertically centred to the track's first line of text.

**State encoding by thumb position.** The thumb position is a load-bearing signal the user reads at a glance — not a decorative animation. **Thumb on the right = Checked (on); thumb on the left = Unchecked (off).** This is reinforced by the track's colour (blue for Checked, grey for Unchecked per *Toggle states*). The two encodings — position and colour — must agree; never invert one without the other. The on-right / off-left convention is the industry-standard platform expectation (iOS, Android / Material Design); users arrive at Atlas with a strong learned expectation. Atlas inherits this convention from react-aria-components' `Switch`, which renders the thumb on the right when `isSelected` is true.

**Helper text** (optional, per toggle) sits in one of two positions — pick one per toggle, never both:

- **Below the per-toggle label** (default) — beneath the label on its own line. Use for helper text longer than a few words.
- **Inline next to the per-toggle label** — same line as the label, separated by a small visual divider (e.g. `[—•] Auto-save · saves every 30 seconds`). Use when the helper is short and benefits from being on the same row.

**Section heading** (above a group of related toggles) — typographic heading naming the category (e.g. *Notifications* above three notification-preference toggles). This is a typographic heading + ARIA group container, not a single semantic group label in the radio/checkbox sense — see *Multiple toggles together* for the full grouping anatomy.

**Violations**

- Label rendered anywhere other than to the right of the track — error
- Track-to-label gap not 8px — warning
- Toggle rendered without an accessible name (no visible label and no `aria-label` / `aria-labelledby`) — error (see *Every toggle has an accessible name*)
- Helper text rendered above the per-toggle label — warning
- Helper text rendered in both the below-label and inline-next-to-label positions on the same toggle — warning
- **Thumb-on-left used to represent Checked / on** (or thumb-on-right for Unchecked / off) — error (inverts the industry-standard platform convention; users misread the toggle's current state at a glance)
- Track colour and thumb position disagreeing on which state the toggle is in (e.g. blue track with thumb on the left) — error (the two encodings must agree)

**Examples**

✓ `[—•] Dark mode` — track on the left, 8px gap, label on the right. When toggled on, the thumb slides 18px to the right and the track becomes blue.

✓ `[—•] Auto-save · saves every 30 seconds` — short helper text inline on the same row, separated by a divider dot.

✓ A *Notifications* section heading above three toggles (Email / Push / SMS), each with its own per-toggle label.

✗ A toggle where the thumb sits on the *left* when the setting is on — inverts the on-right convention.

✗ A toggle with a blue (Checked) track but with the thumb on the left — colour says *on*, position says *off*, user has to guess which signal is authoritative.

---

## Rule: Toggle states

**Description**

A toggle is in one of two behavioural states at any time: **Unchecked** or **Checked**. There is no indeterminate state — toggle represents a binary on/off decision where the state is always definite. Each behavioural state has three interaction variants (Default, Hover, Disabled) and a separate Focus state that overlays on either when the toggle holds keyboard focus.

**How to Apply**

Token mapping per state — canonical surface tokens from the Atlas Library `.toggle` frame. Use them verbatim; do not hand-roll hex values.

| Behaviour | Interaction | Track surface | Thumb |
|---|---|---|---|
| Unchecked | Default | `--surface-neutral-active` (#abafb7) | `--surface-default` (#ffffff) |
| Unchecked | Hover | `--surface-neutral-hover` (#51596a) *(aspirational name; track currently binds to a global token — see Open Questions)* | `--surface-default` |
| Unchecked | Disabled | `--surface-disabled` | `--border-disabled` |
| Checked | Default | `--surface-info-active` (#0a41fa) | `--surface-default` |
| Checked | Hover | `--surface-info-active-hover` (#6c8dfc) *(aspirational; currently a lighter tint, not the usual darker shade — see Open Questions)* | `--surface-default` |
| Checked | Disabled | `--surface-disabled` | `--border-disabled` |

The "hover-darken" Checked variant is actually a *lighter* tint of `--surface-info-active`, not a darker shade — uncommon, but documented in the Atlas Library `.toggle` frame and preserved here as-is. Filed in Open Questions for a deliberate review.

**Focus state** overlays on either Unchecked or Checked when the toggle has keyboard focus: a `2px` outline ring at the focus-ring token (rendered as `--border-focus` once the React migration lands; currently `--atl-color-blue-40` in the legacy stylesheet). Keyboard-only via `:focus-visible` / `[data-focused]`.

**No indeterminate state.** Toggle represents a binary on/off decision — there is no "partially on." Indeterminate is checkbox-only (see [`checkbox.md`](checkbox.md) *Checkbox states*). A "master toggle that controls N child toggles" pattern (where the master should reflect "some on, some off") is a different design problem; if the use case emerges, treat it as a follow-on for [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md), not by adding indeterminate to Toggle.

**Violations**

- Indeterminate-like state on a toggle (any visual treatment that's neither fully Unchecked nor fully Checked) — error
- Checked track using a colour other than `--surface-info-active` — error
- Disabled state without `--surface-disabled` track fill — error
- Custom track / thumb shapes (square thumb, rectangular track) — error
- Thumb at a size other than `14 × 14` — error

**Examples**

✓ A *Dark mode* toggle in Unchecked state with a grey track and a white thumb on the left; the user clicks → the thumb slides 18px right, the track becomes `--surface-info-active` blue, dark mode activates immediately.

✓ Hovering over a Checked toggle in a settings panel — the track shifts to its hover variant, the cursor becomes a pointer.

✗ A *Sync status* toggle showing a half-grey/half-blue track to indicate *partially synced* — invented state.

Link to Figma: [Atlas Library — `.toggle` state matrix](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-41058)

---

## Rule: Toggle sizing

**Description**

Atlas toggles have one size everywhere: `36 × 20` component boundary, `36 × 18` visible track, `14 × 14` thumb with `2px` inset. The single-size rule applies on settings pages, in dialogs, inside panels, and in dense preference UIs — the track is already small, and scaling it smaller would hurt hit targets and visual rhythm; scaling it larger would visually compete with the input field next to it.

**How to Apply**

| Measurement | Value |
|---|---|
| Component boundary (layout footprint, click target on the track) | `36 × 20` |
| Visible track | `36 × 18` |
| Track border radius | `18px` (fully rounded pill) |
| Thumb | `14 × 14`, fully circular |
| Thumb inset from track edge | `2px` (top, bottom, and sides) |
| Thumb translation (Unchecked → Checked) | `18px` horizontal |

The 1px gap between the visible track and the component boundary (top + bottom) is the reserved space for the focus ring (see *Interaction states*) so focus styling doesn't push surrounding layout.

**Violations**

- Toggle rendered at a size other than `36 × 20` boundary / `36 × 18` visible track — error
- Thumb at a size other than `14 × 14` — error
- Custom track radius (anything other than fully rounded pill) — error
- A "compact toggle" or "large toggle" variant — error

**Examples**

✓ A `36 × 20`-boundary toggle in a settings form lines up with input labels and other form controls.

✗ A scaled-down `28 × 16` toggle squeezed into a dense settings table to save space.

---

## Rule: Multiple toggles together — layout, not a single group component

**Description**

**Multiple toggles are grouped visually for the user's benefit — but technically each toggle is evaluated independently the moment its state changes.** Related settings displayed together (a settings panel with 5 toggles, a feature-enablement section, a notifications-preferences UI) share a section heading, consistent spacing, and ARIA group semantics so the user can scan related controls as a coherent unit. **What they don't share is state, validation, or a commit moment**: each toggle commits immediately when its state changes (per *Validation behaviour*), independently of every other toggle in the same visual group.

Because of this, **Atlas does not ship a `SwitchCollection` / `SwitchGroup` component** analogous to `CheckboxCollection` / `RadioCollection`. There is no shared group state to wrap, no group-level validation, no mutually-exclusive single-pick logic, no batched submit. The grouping serves the user (visual proximity, scannability, an accessible group name for screen-reader navigation); each toggle's state lifecycle runs entirely on its own.

**How to Apply**

For a group of related toggles in a shared layout:

1. **Section heading** above the toggles — typographic heading (Atlas heading or label component, not a button) naming the category. E.g. *Notifications*, *Privacy*, *Display*.
2. **Toggle stack** below the heading — toggles laid out vertically by default, each on its own row with per-toggle label to the right of the track (per *Toggle anatomy*).
3. **Vertical spacing between toggles** — `12px` matches the surrounding form's rhythm; tighter spacings can be appropriate in dense settings panels. Horizontal grouping is rare for toggles; if used, `16px` between items (same as horizontal checkbox / radio grouping).
4. **ARIA group semantics** (recommended) — wrap the toggles in a layout container with `role="group"` and `aria-labelledby` pointing at the section heading's id. This is **accessibility-only grouping**: screen readers announce *group: Notifications* when the user navigates in, but there's no shared React state, no shared event handler, no JavaScript implications.

**Standalone toggle** — a single toggle in a header bar, profile menu, or single-setting panel. No grouping container; just render the toggle with its per-toggle label.

**Why no `SwitchCollection`.** `react-aria-components` doesn't ship one either, for the same reason: the immediate-commit semantic means there's no shared group state for a collection component to manage. If a Tripletex use case ever emerges with genuine shared toggle state (a master-toggle pattern, section-level disabled propagation, bulk-action affordance), adding a `SwitchGroup` then is appropriate — filed as a tracked possibility in Open Questions, not a current gap.

**Violations**

- A `SwitchCollection` / `SwitchGroup` React component built to wrap multiple toggles and emit a single grouped event — error (invents semantics that don't apply)
- Multiple toggles controlling related settings rendered without a section heading or visual grouping — warning
- Section heading rendered as a button or interactive element when it's only a typographic label — warning
- ARIA `role="group"` applied to a single standalone toggle — warning (group semantics only make sense for ≥2 grouped toggles)

**Examples**

✓ A *Notifications* settings section with the heading *Notifications* and three toggles below (Email / Push / SMS); `role="group"` + `aria-labelledby="notifications-heading"` on the layout container. Each toggle commits its state immediately on click.

✓ A standalone *Dark mode* toggle in the user-profile menu — no grouping needed.

✗ A `SwitchGroup` component built to wrap 3 toggles and emit a single grouped event.

✗ A settings page with 8 toggles all rendered in a flat list with no section headings.

Link to Figma: [Atlas Library — Toggle Group](https://www.figma.com/design/4WZWeGkM9pNR8Y0c3X8z3H/Atlas-Library?node-id=484-41480)

---

## Rule: Click target spans label and track

**Description**

Clicking anywhere on the visible label or the track toggles the toggle. The label is part of the active click area, not just an associated identifier — it widens the effective target past the `36 × 20` track alone, which matters for both pointer accuracy and touch.

**How to Apply**

1. The full label-text element is part of the click target. Native HTML `<label for="...">` association does this automatically; react-aria's `Switch` does it via its render structure.
2. Hover state (see *Toggle states*) is visible across the whole label + track area — cursor over the label gives the same hover affordance as cursor over the track.
3. Helper text is **not** part of the click target — reading material, not an action surface.
4. **Clicking commits immediately** (see *Validation behaviour*) — there's no "select then save" two-step. The moment the user clicks, the system attempts the state change.

**Touch-target note.** The `36 × 20` track on its own is below WCAG 2.2 SC 2.5.8's `24 × 24` minimum on the short axis. With a visible label, the effective target is "track + 8px gap + label width" — comfortably above the minimum in practice. **Avoid shipping a labelless toggle (`aria-label`-only) in a touch context** unless the surrounding container already provides a target above `24 × 24`.

**Violations**

- Clicking the label does not toggle the toggle — error
- Hover state shown only when the cursor is over the track, not over the label — warning
- Helper text rendered as part of the click target — warning
- Labelless toggle shipped in a touch-first context without a surrounding ≥`24 × 24` target — warning

**Examples**

✓ A *Dark mode* toggle — clicking the words selects the toggle, same as clicking the track. The change commits immediately.

✗ A toggle where only the small track accepts clicks; clicking the label does nothing.

---

## Rule: Every toggle has an accessible name

**Description**

A toggle without an accessible name is unusable with assistive technology — screen readers announce "switch, off" with no indication of what the user is toggling. Atlas's default is a **visible per-toggle label** to the right of the track (see *Toggle anatomy*); the carve-out below covers the rare inline cases where surrounding context provides the name.

**How to Apply**

Three ways to provide an accessible name, in order of preference:

1. **Visible per-toggle label** — the default, required for any toggle in a standard settings panel, preferences page, feature-enablement context, or grouped-settings section. Position per *Toggle anatomy*.
2. **Section heading as the group's accessible name** — for a group of toggles wrapped in a `role="group"` container (see *Multiple toggles together*), the section heading is the accessible name for the group; individual toggles still need their own per-toggle labels.
3. **`aria-label` or `aria-labelledby` for inline contexts** — when the toggle lives in a place that doesn't have a per-toggle label slot (rare for toggles; usually a sign you should consider a different control). Use `aria-label` for a simple stable string, `aria-labelledby` when an existing element already labels what's being toggled.

**Toggles in tables are generally discouraged** — see [`patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md). Toggles in table cells lose context — users have to look at the column header to know what they toggled. Use a Status component, Status Chip, Dropdown, or dedicated state-marking affordance instead. The exception is settings tables (a row per setting, the toggle as the control) — in which case treat the row as a labelled context.

The `aria-label` (or the text in the element referenced by `aria-labelledby`) must accurately describe the toggle — *`<setting name>`*, never just *switch*, *toggle this*, or *on/off*.

**Violations**

- Toggle rendered with no visible label and no `aria-label` / `aria-labelledby` — error
- Toggle using `aria-label` in a context that has a label slot available — warning (visible label preferred)
- `aria-label` text that doesn't describe the toggle (*switch*, *on/off*, *toggle*) — error
- `aria-labelledby` pointing at an element that's hidden or doesn't visibly label the toggle — warning

**Examples**

✓ `[—•] Dark mode` — visible per-toggle label, native association.

✓ A *Notifications* group with three toggles, each with its own visible label (Email / Push / SMS); the group's accessible name comes from the section heading *Notifications* via `aria-labelledby`.

✗ A toggle with `aria-label="switch"` — uninformative.

---

## Rule: Validation behaviour — immediate commit, revert on failure

**Description**

Toggles validate differently from checkbox and radio. **A toggle commits its state the moment the user clicks** — no form-submit step, no `errorMessage` on a parent collection, no pre-submit validation. The system attempts the underlying state change immediately. **If the change succeeds**, the toggle's new state stays as-is. **If the change fails** (server error, downstream validation failure, network issue), the toggle's visual state **reverts** to its previous position and the user is shown an explanation.

This is a load-bearing difference from [`checkbox.md`](checkbox.md) *Validation behaviour* (per-box + group-level error styling on `isInvalid`) and [`radio-button.md`](radio-button.md) *Validation behaviour* (group-level `errorMessage`). Toggle has no per-control invalid state and no group-level validation message because there is no submit moment to validate against. Errors are post-action recovery, not pre-submit signals.

**How to Apply**

1. **Optimistic update on click.** The moment the user clicks, the toggle's visual state changes (track colour, thumb position) and the system kicks off the underlying state change. The user sees immediate feedback and doesn't wait for the round-trip.

2. **On success** — no further UI is required. The toggle stays in its new state. For non-trivial operations (e.g. enabling a feature that affects multiple parts of the product), a confirmation Notification / Toast is reasonable but not required.

3. **On failure — revert and explain.** Atlas's recovery contract for a failed toggle:
   - **Revert the toggle's visual state** to its previous position. The user immediately sees that the change didn't stick.
   - **Show error text describing why** — two valid placements, mirroring helper text placements from *Toggle anatomy*:
     - **Below the per-toggle label** — error text on its own line beneath the label (e.g. *Couldn't enable Dark mode — try again or refresh the page*).
     - **Inline next to the per-toggle label** — error text on the same row, separated by a thin divider (e.g. `[—•] Dark mode · couldn't enable, try again`).
   - **Fallback for constrained inline space** — when there isn't room for inline / below error text (dense settings tables, narrow panels), use an **error icon next to the toggle** with the full error message in a Popover on hover or focus. **Teams reaching for the icon+popover fallback should coordinate with Astro** to formalise the pattern as an Atlas Library component so it doesn't drift across teams.

4. **Notification or Toast for high-stakes operations.** When the failed operation affects more than just the local toggle (e.g. *Couldn't enable Two-Factor Authentication*), the post-action feedback should also fire a Notification or Toast in addition to inline error text.

5. **No per-toggle invalid styling.** The toggle's visual state in *Toggle states* does not change to a red-bordered "invalid" rendering. The React `Switch.css` has no `[data-invalid]` block. Error communication is via revert + descriptive text (and optional Notification), not by re-skinning the toggle.

**Async commit during the round-trip.** Between the user's click and the server confirming, the toggle's visual state has already updated optimistically. If the round-trip takes more than ~300ms, consider showing a brief loading indicator alongside the toggle (a small spinner adjacent to the track). For sub-300ms commits, no loading indicator is needed.

**Cross-reference: [`patterns/validation-feedback.md`](../../../patterns/validation-feedback.md).** That pattern owns form-level validation. Toggle's validation is fundamentally different because toggle doesn't participate in form submission. The cross-reference exists so teams searching for *validation* land on both files; the actual contracts are distinct.

**Violations**

- Per-toggle red-border or red-outline invalid styling — error (toggle has no per-control invalid state)
- Failed toggle not reverted on failure (stays in the wrong state with no explanation) — error
- Failed toggle reverted with no error message anywhere — error (user knows something went wrong but can't see why)
- Validation message rendered as a Banner in the page-header alert slot for a single toggle's failure — warning (use inline error text or a Notification; Banners are for page-level state)
- Toggle disabled because its underlying API is unavailable — note (Disabled is fine; just make sure the tooltip explains *Available when X* rather than letting the user think the toggle is broken)
- Icon+popover fallback used without coordinating with Astro on the pattern — warning

**Examples**

✓ User clicks *Dark mode* → toggle slides to On immediately → 200ms later the server confirms and the page goes dark. No error UI shown.

✓ User clicks *Email notifications* → toggle slides to On → server returns an error → toggle slides back to Off, *Couldn't enable — email service is temporarily unavailable. Try again in a few minutes.* renders below the toggle label.

✓ A dense settings table with no room for inline error text — the failed toggle reverts, an error icon appears next to it, hovering the icon shows the full error in a Popover.

✗ User clicks *Two-Factor Authentication* → toggle slides to On → server fails → toggle stays in On state with no indication of failure.

✗ A toggle with a permanent red border indicating *this setting is in an error state*.

---

## Rule: Disabled state

**Description**

A toggle is disabled when the user cannot toggle it *right now*, but the toggle *could* be toggled under different circumstances — the underlying feature isn't available in the user's plan, a prerequisite setting isn't enabled, the user's permission level doesn't allow it. Disabled signals **conditional unavailability**: there is a path to making the toggle active, and the rule's job is to tell the user what that path is. For settings that are permanently fixed (audit logs, finalised configurations, locked records), use *Read-only state* instead.

**How to Apply**

| Aspect | Spec |
|---|---|
| Visual | Disabled chrome per *Toggle states* Disabled row, per behavioural state (Unchecked or Checked × Disabled) |
| Track cursor | `cursor: default` (**not** `cursor: not-allowed`) |
| Label rendering | Greyed alongside the track, using `--text-disabled` |
| Tooltip | **Required** — explains *why* the toggle is disabled and, where possible, *how* to make it available (*Available on the Premium plan*, *Enable Notifications first*, *Available to admin users only*) |
| ARIA | `disabled` attribute on the underlying input |
| Focusable | **No** — Tab skips disabled toggles; screen readers announce as dimmed / unavailable |
| Click target | Inert — clicks on the track or label have no effect |

The `cursor: not-allowed` reads as "you've been blocked"; `cursor: default` reads as "this just isn't active right now," which is closer to the truth and matches the conditional-unavailability framing.

**Group-level disabled propagation.** When a section of related toggles is disabled at the layout level (e.g. the entire *Notifications* section is disabled because notifications are off at the account level), the disabled state applies to every toggle in the section. The section heading and per-toggle labels all render greyed. Recommended pattern: disable the layout container's interactive children rather than applying `isDisabled` to each toggle individually — but the visual outcome is the same. Each toggle still carries its own tooltip explaining the conditional unavailability (*Enable notifications at the account level first*).

**Violations**

- Disabled toggle using `cursor: not-allowed` — error
- Disabled toggle without a tooltip explaining why — warning
- Tooltip that doesn't tell the user how to make the toggle available, when there is a way — note
- Disabled used for a permanently-unavailable setting with no path to enabling — warning (use Read-only instead)
- Disabled toggle using `aria-readonly="true"` instead of the `disabled` attribute — error
- Disabled toggle that's focusable (Tab lands on it) — error

**Examples**

✓ A *Two-Factor Authentication* toggle disabled until the user verifies their email; hovering shows *Verify your email to enable 2FA*.

✓ A *Send weekly digest* toggle disabled on a free-plan account; tooltip: *Available on Premium and Business plans*.

✗ A *Period locked* toggle on a finalised accounting period rendered as disabled — should be Read-only; the user cannot enable it under any circumstance.

✗ A disabled toggle using `cursor: not-allowed` and no tooltip.

---

## Rule: Read-only state

**Description**

A toggle is read-only when the value is fixed and the user cannot change it under any path forward. Read-only signals **permanent unavailability** — audit logs showing past configurations, finalised submissions, locked records, summary views of decisions already made.

**Read-only currently shares the same visual treatment as Disabled** — same interim as [`checkbox.md`](checkbox.md) *Read-only state* and [`radio-button.md`](radio-button.md) *Read-only state*. No distinct read-only visual exists for any of the three selection sub-family controls yet. When a distinct visual lands, all three rules update together.

**How to Apply**

| Aspect | Spec |
|---|---|
| Visual | Same as Disabled (interim) — per *Toggle states* Disabled row, per behavioural state |
| Track cursor | `cursor: default` |
| Label rendering | Same as Disabled (interim) — greyed alongside the track |
| Tooltip | **None** — no "how to enable" exists for a permanently-fixed value; surrounding context provides the meaning |
| ARIA | `aria-readonly="true"` on the underlying input (**not** the `disabled` attribute) |
| Focusable | **Yes** — Tab lands on read-only toggles; screen readers announce "read-only switch, on / off" |
| Click target | Inert for toggling, but remains in the focus order so keyboard and screen-reader users can navigate to read the value |

**Why focus matters for read-only.** Read-only is part of the displayed *information*. Keyboard users need to be able to navigate to read-only values to read them; screen-reader users need the value announced. Skipping read-only fields hides information.

**React API gap.** The Atlas React `Switch` API currently omits `isReadOnly` (same pattern as Checkbox and Radio). Adding it is filed in Open Questions, coordinated with the same item for Checkbox + Radio so all three selection sub-family controls gain the API together.

**Violations**

- Read-only toggle using the `disabled` attribute instead of `aria-readonly="true"` — error
- Read-only toggle not focusable (Tab skips it) — warning
- Read-only toggle carrying a tooltip explaining why — note (no tooltip needed; surrounding context provides the meaning)
- Read-only used for conditionally-unavailable values where the user could make the toggle interactive — warning (use Disabled instead)
- Read-only toggle with `cursor: not-allowed` — error

**Examples**

✓ An audit-log row showing a *Two-Factor Authentication* toggle in the On position, read-only — focusable, no tooltip, screen readers announce *read-only switch, on*.

✓ A finalised accounting period's settings summary showing *Period locked: On* as a read-only toggle.

✗ An audit-log toggle rendered with the `disabled` attribute — fails ARIA + keyboard navigation.

✗ A read-only toggle carrying a tooltip *This is a historical record* — surrounding context already provides that meaning.

---

## Rule: Interaction states

**Description**

The interaction state describes what's currently happening to the toggle — hover, focus, disabled, read-only. Each state has a distinct visual treatment so the user knows where they are without thinking. **Focus must be visibly distinguished from default** — keyboard-only, via `:focus-visible` / `[data-focused]`, never on mouse-click.

**How to Apply**

| State | When it applies | Visual treatment |
|---|---|---|
| Default | At rest, no interaction | State tokens from *Toggle states* (Default row per behaviour) |
| Hover | Pointer over the label or track | State tokens from *Toggle states* (Hover row per behaviour) |
| Focus | Track has keyboard focus | `2px` outline ring around the track at `--border-focus` (currently `--atl-color-blue-40` in the legacy stylesheet; semantic name pending the React migration) |
| Disabled | Mode is Disabled (see *Disabled state*) | State tokens from *Toggle states* (Disabled row per behaviour) |
| Read-only | Mode is Read-only (see *Read-only state*) | Same as Disabled (interim) |

**No Invalid row** — toggle has no per-control invalid state (see *Validation behaviour*). Validation is post-action via revert + descriptive error text, not by re-skinning the toggle.

**Focus-ring divergence across the selection sub-family — known gap.** The three selection sub-family controls render focus differently in the current React implementation:

- **Checkbox** — 1px `--border-focus` border, 3px offset outside the box.
- **Radio** — `2px` solid outline at `--border-focus`, `2px` offset outside the circle.
- **Toggle** — `2px` outline at `--border-focus` (currently `--atl-color-blue-40`), no documented offset beyond the 1px reserved margin on the track.

Three different focus-ring renderings for three closely-related sub-family controls is real visual drift. **Filed as a high-priority follow-on** to be resolved as a foundation-level decision (a future `foundations/focus.md` would be the canonical home). Until that lands, this rule documents the current Toggle implementation as-is.

**Focus is keyboard-only.** The ring renders only on keyboard focus — clicking the track with a pointer does not show it, by design.

**Violations**

- Focused toggle without a visible focus ring — error
- Focus ring shown on mouse-click (any-focus styling instead of `:focus-visible` / `[data-focused]`) — warning
- Hover state visually identical to default — warning
- Per-toggle Invalid styling applied (red border on a toggle's track) — error (use revert-on-failure + inline error text per *Validation behaviour*)

**Examples**

✓ Tabbing onto a toggle in a settings panel shows a clear outer focus ring around the track; clicking it with the mouse does not.

✗ A focused toggle indistinguishable from default — fails keyboard-navigation visibility.

---

## Related Rules

- [`checkbox.md`](checkbox.md) — selection sub-family sibling (deferred-commit binary or multi-pick selection). Toggle mirrors checkbox's structure with three key differences: immediate-commit semantic, no `SwitchCollection`, no per-control invalid state.
- [`radio-button.md`](radio-button.md) — selection sub-family sibling (single-pick mutually-exclusive selection).
- [`input.md`](input.md) — anchor of the value-entry sub-family; toggle is in the broader form family but documents its own anatomy, modes, and interaction states.
- [`textarea.md`](textarea.md) — multi-line value-entry sibling of input.
- [`../../../patterns/checkbox-vs-switch.md`](../../../patterns/checkbox-vs-switch.md) — selection sub-family decision guide: toggle vs checkbox vs radio (and the explicit "avoid in table cells" rule).
- [`../../../patterns/validation-feedback.md`](../../../patterns/validation-feedback.md) — form-level validation surfacing rules; toggle does not participate in form-submit validation but the cross-reference exists for discoverability.
- [`../banner.md`](../banner.md) — banners-in-forms forbidden; cross-referenced by *Validation behaviour*.
- [`../../foundations/colors.md`](../../foundations/colors.md) — surface, border, text tokens used in *Toggle states* (note: two hover-variant tokens currently bind to global tokens; see Open Questions).

---

## Open Questions

- **HIGH PRIORITY — Resolve the focus-ring divergence across Checkbox / Radio / Toggle.** Three different renderings (1px border + 3px outset vs `2px` outline + `2px` offset vs `2px` outline + no documented offset). Resolve as a foundation-level decision; consider creating `foundations/focus.md` as the canonical home for focus-ring tokens and rendering rules.
- **HIGH PRIORITY — Add Focus state to the `.toggle` state-matrix frame.** Same gap as `.checkbox` and `.radio` — Focus is rendered in React but not represented in Figma. Coordinate one update across all three selection sub-family frames.
- **Figma library — Read-only state variant missing on the `.toggle` frame** (and `.checkbox`, `.radio`). Pending the distinct read-only visual-treatment design work that covers all three together.
- **React `Switch.css` token migration.** Component still uses legacy `--atl-color-*` tokens; should migrate to the semantic tokens documented in *Toggle states*. Coordinates with the same Checkbox + Radio migrations.
- **Atlas Switch `isReadOnly` API addition.** *Read-only state* documents the mode but the React API omits `isReadOnly`. Coordinates with the same Checkbox + Radio follow-ons — three components, one coordinated API change.
- **Distinct read-only visual treatment for all three selection sub-family controls.** *Read-only state* notes the read-only / disabled visual collision as an interim. Design team to articulate distinct read-only visuals for all three together.
- **Forms-family read-only consistency.** `input.md` *Read-only mode* renders read-only inputs as plain text; selection sub-family controls render read-only with disabled-shaped chrome. Worth a deliberate decision on whether to align across the family or document the divergence as canonical.
- **`colors.md` token coverage gap — selection sub-family Figma divergence.** The same hex appears under three different names across the selection sub-family Figma frames (Checkbox uses *Form/Rest* #f7f8fc, Radio uses *Surface/Background* #f7f8fc, Toggle uses *Surface/Default* #ffffff — and two different hex values). Toggle's hover variants also bind to **global tokens** (`Global/Grey/80`, `Global/Blue/60`), violating the "use semantic tokens in components" mandate. **Figma must align first** — consolidate to canonical names and add explicit semantic tokens for the hover variants; then `colors.md` and the React CSS migrations follow.
- **Checked-hover lighter tint anomaly.** Toggle's Checked-Hover track is a *lighter* tint of `--surface-info-active`, not a darker shade — the opposite of the usual hover convention. Atlas Library documents it this way; worth a deliberate review (is this intentional and should the convention apply elsewhere, or is it a bug in the Figma frame?).
- **`SwitchGroup` React component — consider only if a Tripletex use case emerges with genuine shared toggle state** (master-toggle pattern, section-level disabled propagation, bulk-action affordance). None exist today.
- **Icon+popover failure-fallback Library pattern.** *Validation behaviour*'s icon+popover fallback for error display currently doesn't have a formal Atlas Library component. Astro to formalise so teams reaching for the pattern don't drift across implementations.


---

# PATTERNS

---




---

## patterns/attestation.md

# Attestation Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document patterns for user confirmation and verification flows — when to require explicit user sign-off and how to present confirmation UI. Overlaps with AI/Automations pattern..

---

## patterns/auto-save.md

# Auto Save Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document how to handle two conflict scenarios: (1) two users editing the same record simultaneously, (2) user has unsaved changes and navigates away. Needs input from both UX and development..

---

## patterns/banner-usage.md

# Banner Usage Rules

When to reach for a banner — and when not to. Banners are prominent and don't auto-dismiss, which makes them powerful for critical messages and a source of fatigue if overused. The component-level rules for *what a banner looks like* live in [`../design-rules/components/banner.md`](../design-rules/components/banner.md); this file is about *when* a banner is the right answer.

The general principle: **if everything is marked as important, nothing is.** Treat banner real estate as scarce.

---

## Rule: When to use a banner

**Description**

A banner is the right component when a piece of system or product information is genuinely important to most users on the page where it appears, *and* a less intrusive component (alert, inline note, popover, tooltip) would not deliver the message effectively. If you can't say yes to both, the banner is probably the wrong choice — and adding it costs more than it gains, because every additional banner reduces the salience of every other.

**How to Apply**

Before adding a banner, run the **three-question pre-flight**:

1. **Relevance** — is the message relevant to most users on this page, not a niche subset?
2. **Helpfulness** — does it help the user with the task they came to the page to do, or alert them to something that affects that task?
3. **Better-than-alternatives** — could a less intrusive pattern (alert in context, inline note, popover, tooltip) communicate this more effectively?

If the answer to (1) or (2) is **no**, do not add the banner.
If the answer to (3) is **yes**, use the less intrusive pattern instead.

**Violations**

- Banner used for niche information relevant to a small subset of users — warning
- Banner used where an alert, inline note, or popover would have communicated the same thing — warning
- Multiple unrelated banners on a single page (banner overload) — warning

**Examples**

✓ An **Error** banner explaining that the user's last automation run failed and how to retry it — relevant to anyone using that page, helpful to their task, and a banner is the right level of prominence.

✗ A **Tips** banner reminding users that filters exist — better as inline microcopy or a popover near the filter UI itself.

✗ An **Info** banner about a webinar relevant only to accountants displayed on every page — niche audience, page-specific irrelevance.

---

## Rule: Banner stacking

**Description**

Stacking banners is generally discouraged — multiple banners on the same page compete for attention and accelerate banner fatigue. There are cases where stacking is unavoidable: when several genuinely system-level messages must remain accessible to the user without taking up viewport space individually. When stacking does happen, the order matters — the most urgent banner should be on top so it gets read first.

Stack banners only when **all** of the following are true: more than one system-level message is simultaneously relevant; each one independently passes the pre-flight from *When to use a banner*; and showing them one at a time would hide information the user needs to act on. If only one of the candidates passes the pre-flight, drop the others — don't stack them just because you can.

**How to Apply**

When stacking is necessary:

1. **Order the banners by severity, highest first:**
   **Error → Attention → Done → Automated → News → Get started → Help → Tips → Info**
2. **Place the stack directly under the page header**, occupying the full content width.
3. Each banner in the stack still follows the full anatomy and dismissibility contract from [`../design-rules/components/banner.md`](../design-rules/components/banner.md) — including the rule that **Error** and **Attention** banners do not carry a close button (they clear when the underlying condition resolves).

**Violations**

- Stacked banners in arbitrary order (not severity-first per the order above) — warning
- Stacking a banner that doesn't independently pass the pre-flight from *When to use a banner* — warning
- Stacking multiple banners of the same type — warning (consolidate the messaging)

**Examples**

✓ An **Error** banner about a failed payment stacked above an **Info** banner about a deadline — both are genuinely system-level and both pass the pre-flight; Error is on top because it's higher severity.

✗ A stack of three **Tips** banners reminding users about features they could use — none of these pass the pre-flight; remove them or pick the best one.

---

## Related Rules

- [`../design-rules/components/banner.md`](../design-rules/components/banner.md) — what a banner looks like (anatomy, label / colour mapping, dismissibility contract).
- [`../design-rules/components/product-spotlight-banner.md`](../design-rules/components/product-spotlight-banner.md) — the dedicated upsell banner variant (component contract).
- [`product-spotlight-banner-usage.md`](product-spotlight-banner-usage.md) — upsell-specific behaviour rules (frequency, tracking, end date, dismissal).
- [`../design-rules/components/alert.md`](../design-rules/components/alert.md) — when an alert in the page header is the better fit (single message, page-scoped, narrower than a banner).


---

## patterns/breadcrumb-usage.md

# Breadcrumb Usage Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document breadcrumb usage rules — only used in page headers. When to show, how many levels, truncation behavior.

---

## patterns/button-placement.md

# Button Placement Rules

Buttons live in three places: the page header (top right), within a form, or at the end of a page section. Each placement context has its own rule below.

**Shared principle for any button group:** button order follows the group's alignment. A left-aligned group reads primary → secondary → tertiary (left to right). A right-aligned group reverses, so primary sits furthest right.

---

## Rule: Page header button placement

**Description**

Page header buttons are the global actions for the page — things that affect the whole record or page, not the form on it. They live in the top-right of the page header. Because the group is right-aligned, the order reverses (per the shared principle): primary sits at the rightmost regular-button position, with the overflow `[⋮]` placed even further right when buttons don't fit.

Use the page header for actions that affect the entire page or object (delete, archive, duplicate, settings), are performed infrequently or as secondary tasks, don't follow the natural form flow, or are global to the context.

**Tabbed-page carve-out.** When the page contains tabs, the page header carries **only** actions that apply to the **entire record / page** across all tabs — record-level operations like *Archive record*, *Delete record*, *Settings for this record* that remain valid regardless of which tab is active.

**Any action scoped to a single tab — including changes to the current tab's content, edits, exports, adds, posts, or other tab-local operations — MUST live inside the tab's content area and is NOT ALLOWED in the page header.** The page header is always visible across all tabs; rendering a tab-scoped action there would mislead users into thinking the action applies regardless of the active tab, and the action becomes a no-op (or ambiguous trigger) on every tab except one. Tab-scoped actions follow *Section button placement* — each tab is treated as a section.

**How to Apply**

The page header's full anatomy (slot rules, variants, responsive collapse, auto-save indicator, alert placement) lives in [`design-rules/components/page-header.md`](../design-rules/components/page-header.md). This rule covers the action-button slot only.

The group is right-aligned, so the order reverses. From right to left:

1. **Overflow** `[⋮]` — furthest right, when buttons don't fit.
2. **Primary action** — rightmost regular button (just left of the overflow).
3. **Secondary actions** — middle.
4. **Tertiary actions** — leftmost.

When the overflow is needed, it appears on the far right of the group and opens a **Drawer** (the anchored option-list surface; the Figma library still calls it *Popup Menu* — see [`../design-rules/components/popup-menu.md`](../design-rules/components/popup-menu.md) for the rename rationale). Items inside the Drawer are **drawer items**, not buttons: text-only, no default fill, hover and focus chrome only. Drawer items stack top to bottom. The full Drawer contract lives in [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md).

**Violations**

- **Tab-scoped action rendered in the page header on a tabbed page — error** (the action is misleading there; tab-local actions belong inside the tab per *Section button placement*)
- Page header button that should be form-specific — warning
- Primary button not in the rightmost regular-button position (i.e. not directly left of the overflow) — error
- Regular buttons placed inside the overflow Drawer instead of drawer items — error
- Overflow placed somewhere other than the far right — warning

**Examples**

✓ Page header reads `[Delete] [Edit] [⋮]` left to right — Edit is primary, sitting at the rightmost regular-button position; the overflow is further right.

✗ Page header reads `[⋮] [Edit] [Delete]` — overflow in the wrong slot.

✗ A *Save* button in the page header for a form on the page — form-specific action in a global slot.

---

## Rule: Form button placement

**Description**

Form buttons complete or advance the form workflow itself. They live below the form fields, aligned to the form's edge (left- or right-aligned), with order following alignment per the shared principle.

Use form buttons for actions that complete or advance the form workflow (Save, Next, Submit, Cancel), are part of a linear process, should follow the natural reading flow (bottom of form), or apply specifically to form data rather than the whole page.

**How to Apply**

1. Place buttons **below** all form fields.
2. **Align to the same left edge as form fields** — never centred.
3. **Space between form and buttons:** `16px` preferred, `12px` minimum, `24px` maximum.
4. **Order follows alignment** (shared principle): left-aligned → primary → secondary → tertiary; right-aligned reverses (primary furthest right).
5. **Space between buttons in the group:** `8px`.

**Violations**

- Form buttons placed in the page header — error
- Form buttons centred — warning
- Form-to-button spacing below `12px` — warning
- No clear spacing between form and buttons — warning
- Form button order doesn't match its alignment (left-aligned must read primary → tertiary; right-aligned must reverse) — error
- Form-to-button spacing off-scale (e.g. `10px`, `14px`) — warning (see [`../design-rules/foundations/spacing.md`](../design-rules/foundations/spacing.md))

**Examples**

✓ A form with `[Save] [Cancel]` left-aligned below fields, `16px` above the buttons, `8px` between them.

✗ `[Cancel] [Save]` — reversed order.

✗ Form buttons centred.

✗ `10px` between form and buttons — off-scale, also below the `12px` minimum.

---

## Rule: Section button placement

**Description**

Section buttons apply to a specific part of a larger page — a multi-step workflow's *Next* button, actions scoped to one card or panel inside a longer page, **or actions scoped to a single tab in a tabbed page (where each tab is treated as a section).** They follow the same ordering and grouping rules as form buttons, but live at the end of their section rather than the bottom of a form.

Use section buttons for actions that apply to a specific part of a larger page, are part of a multi-step workflow within a page, should stay in the natural reading flow, or apply to a specific tab in a tabbed page. Tab-scoped actions are forbidden in the page header (per the tabbed-page carve-out in *Page header button placement*); they must live inside the tab.

**How to Apply**

1. Place at the **end of the relevant section**.
2. **Align to the same edge as the section's content.**
3. **Spacing above the buttons:** `24px`.
4. **Order follows alignment** (shared principle): primary → secondary → tertiary if left-aligned; reverses if right-aligned.
5. **Space between buttons in the group:** `8px`.

**Violations**

- Section buttons placed somewhere other than the end of the section — warning
- Section buttons aligned differently from the section's content — warning
- Section button order doesn't match its alignment — error
- Unclear which button applies to which section — note
- Spacing above section buttons off-scale (anything other than `24px` from the spacing scale) — warning

**Examples**

✓ A multi-step form where each section ends with `[Next]`, and the final section ends with `[Submit] [Save draft]`.

✓ A *Comments* tab on a record-detail page ending with `[Post comment] [Cancel]` aligned to the tab's content; the page header above contains record-level actions like `[Archive] [⋮]` that apply regardless of the active tab. The Comments-specific actions live inside the tab, not in the page header.

✗ Section button placed in the page header instead of at the end of the section.

✗ A *Post comment* button in the page header of a record-detail page with tabs — the button only applies on the Comments tab, but it's visible (and apparently clickable) regardless of which tab the user is on.

✗ Two sections of buttons stacked together with no visual separation — unclear which applies to which.

---

## Related Rules

- [`../design-rules/components/buttons.md`](../design-rules/components/buttons.md) — button variants, sizing, ordering, and the spacing tokens these rules reference.
- [`../design-rules/components/page-header.md`](../design-rules/components/page-header.md) — full page-header anatomy and the action-button slot's behaviour inside it.
- [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) — the overflow `[⋮]` opens a Drawer; full contract for the surface.
- [`../design-rules/components/modal.md`](../design-rules/components/modal.md) — modal footers follow the alignment principle from this file. The modal stepper exception (Next / Previous may be right-aligned, separate from the rest of the group) is documented there since it's scoped to that component.
- [`../design-rules/foundations/spacing.md`](../design-rules/foundations/spacing.md) — the `8px` / `16px` / `24px` values used here are part of the canonical spacing scale.


---

## patterns/checkbox-vs-switch.md

# Checkbox vs Switch Pattern Rules

> **Status: DRAFT — pending team review per decision #59.**

When to reach for a switch, a checkbox, or a radio button. The three controls look superficially similar — small binary controls with labels — but they encode different semantics: switches commit immediately, checkboxes commit at form submit, radios let the user pick one option from a mutually-exclusive set. **Picking the wrong control misinforms users about what their click will do**, so the rules below are the canonical decision tree.

Switch, checkbox, and radio together form the **selection** sub-family of form components — controls where the chrome *is* the value (the visual control encodes the state). Value-entry components ([`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md), [`textarea.md`](../design-rules/components/forms/textarea.md), and the input-derived types) are a separate sub-family where the chrome *contains* a typed value. This file is the cross-component decision rule **within** the selection sub-family: how to pick between its three members. Each component's own anatomy, states, sizing, and behaviour live in its file ([`toggle-switch.md`](../design-rules/components/forms/toggle-switch.md), [`checkbox.md`](../design-rules/components/forms/checkbox.md), [`radio-button.md`](../design-rules/components/forms/radio-button.md)) — those files defer the *when to use which* question to this one.

This pattern is decision logic across controls and has no Figma frame of its own.

---

## Rule: Picking the control — switch, checkbox, or radio

**Description**

The three controls map to three different semantics:

- **Switch (toggle)** — *immediate-commit binary on / off*. The user's click takes effect the moment they click. There is no save / submit / apply step. Use for system state, feature flags, preferences where instant feedback is expected.
- **Checkbox** — *deferred-commit binary selection*. The user picks (or doesn't pick) the box, and the choice only takes effect at form submit. Use when the box is part of a form workflow, or for a single binary acknowledgment that belongs to a submit moment.
- **Radio button** — *deferred-commit single-pick from a mutually-exclusive group*. The user picks exactly one option from N alternatives; the choice takes effect at form submit. Use when the choice is one-of-N and the alternatives are mutually exclusive.

The decision tree is sharpest on two axes:

- **Commit timing** — immediate (switch) vs deferred (checkbox / radio). This is the first question.
- **Cardinality** — within deferred-commit, is the selection one-of-N (radio) or zero-or-more independently (checkbox)?

**How to Apply**

The decision tree, in order:

1. **Does the action take effect immediately?** If yes → **switch**. If no (the value is collected and applied at form submit) → continue.
2. **Is the choice mutually exclusive (one of N, never zero, never more than one)?** If yes → **radio**. If no (the user can pick zero, one, or more independently) → **checkbox**.

Use a **switch** when the setting applies immediately without confirmation; the user is toggling a single feature or module on or off; the action produces an observable change in the application state or interface (not just the control itself); the action is high-frequency and benefits from being quick (dark mode, notifications, auto-save); or there is no Save / Apply button on the surface.

Use a **checkbox** when multiple related options need to be selected and the user reviews them before submitting; the change requires a save or apply button to take effect; you're presenting a list of independent choices (multi-select filter, opt-in checkboxes during onboarding); or a single binary acknowledgment is needed at form submit (e.g. *I agree to the terms*).

Use a **radio button** when the user picks exactly one option from a mutually-exclusive set of N alternatives; the choice is part of a form workflow and the value is submitted with the rest of the form; or the options are alternatives to each other (Standard / Express / Pickup), not independent toggles.

If the use case doesn't fit cleanly into any of the three, the right control is probably not in the selection sub-family at all — consider Select / Combobox / Dropdown / Button group depending on the shape of the data.

**Violations**

- A switch in a form with a Save / Submit / Apply button (the value isn't taken until submit, but the switch's visual semantic suggests instant action) — error
- A switch used for a mutually-exclusive choice (the user picks one of N, not on / off) — error (use radio)
- A checkbox used for immediate-commit live system state (dark mode rendered as a checkbox in a settings page that auto-saves) — error (use switch)
- A single radio button rendered with no sibling options (radio has no semantic in isolation) — error (use checkbox or switch per the decision tree above)
- A settings form with N switches and a *Save* button — error (this is the canonical anti-pattern: switches imply instant action, save buttons imply deferred action; the two semantics conflict)

**Examples**

✓ A *Dark mode* toggle in the user-profile menu — the user clicks, the entire product instantly switches to dark theme. No save button.

✓ An *Auto-save* toggle on a long-form editor settings panel — clicking immediately enables / disables auto-save behaviour.

✓ *Email notifications* toggle in a preferences page — clicking immediately changes the underlying notification subscription.

✓ *Send me product updates* checkbox in a sign-up form — the value is collected and submitted with the rest of the form.

✓ *I agree to the terms* checkbox above a *Sign up* button — single binary acknowledgment that submits with the form.

✓ A multi-select filter on a list view — users tick the categories they want and the filter applies on a *Filter* button click (or on filter blur, but not on each individual click).

✓ *Shipping method* with three radios (Standard delivery / Express / In-store pickup) — the user picks one; the choice submits with the rest of the order form.

✗ A *Settings* form with 15 switches and a *Save* button at the bottom. Switches imply each setting takes effect on click; the Save button implies deferred commit. Users either click Save expecting nothing has saved yet (and lose unsaved changes), or trust the switches and never realise the Save button needed clicking. **Use checkboxes** in this form, or remove the Save button and let each switch commit on its own.

✗ A *Dark mode* checkbox in a settings page that auto-saves each change. The auto-save makes commit immediate, so the deferred-commit semantic of a checkbox lies to the user. **Use a switch.**

✗ A single *Subscribe to newsletter* radio button on a form. Radio's mutually-exclusive semantic doesn't apply with N=1. **Use a checkbox** (single binary acknowledgment that submits with the form) or **a switch** (immediate-commit if the subscription is processed on click).

---

## Rule: Avoid switches and checkboxes in tables for item-state marking

**Description**

Don't use switches or checkboxes in table cells to mark *item state* (e.g. *flagged*, *needs follow-up*, *archived*, *published / draft*). When a toggle or checkbox sits in a table cell without surrounding context, users must read the column header to understand *what* they've toggled. The cognitive cost is higher than it looks: every row asks the same look-up question, and the table becomes a maze of binary controls whose meaning lives one row away.

This rule applies to *item-state marking* — using a toggle or checkbox in a cell to indicate the state of the object the row represents (an article, a task, a customer). Two table patterns are explicitly **OK** and out of scope:

- **Row-select checkboxes** — a column of checkboxes, one per row, where ticking the box selects the row for a bulk action. Follow [`checkbox.md`](../design-rules/components/forms/checkbox.md) *Every checkbox has an accessible name* (with the `aria-label` / `aria-labelledby` pattern for inline contexts).
- **Settings tables** — a row per setting, the toggle or checkbox as the control for that setting. The row itself labels the control. Examples: a permissions table where each row is a permission and the toggle enables / disables it; a feature-flag admin view where each row is a flag; a notification-preferences matrix where rows are notification types and columns are channels (Email / Push / SMS). The row's primary cell provides the per-control labelling context.

**How to Apply**

When designing a table that needs to show or edit binary item state:

1. **Treat the state as a value, not a control.** Render it as text, a Status component, a Tag, or a Label per the surrounding content's rhythm. The cell shows *what* the state is.
2. **If the state is editable per row**, lift the editing affordance out of the cell:
   - **Prefer a Status Chip** for small-N (2–4 states). Atlas's Status Chip is a selectable-chip control that names the state on the control itself — clicking the chip steps through (or opens a small menu of) the available states without leaving the row. Status Chip is currently undocumented and missing a formal Figma design — see the [Atlas Component Development Workfile — Status Chip sketch](https://www.figma.com/design/vCb2O3BLUotY1JdJ6rCBFf/Atlas-Component-Development--Workfile-?node-id=5094-19516). Teams reaching for this pattern should coordinate with the Astro design system team.
   - **Use a Dropdown / Select per row** when the option list grows beyond 4 states.
   - **Use a row-action button or edit drawer** when inline editing doesn't fit.
3. **If multiple rows need bulk-edit**, use a row-select column of checkboxes (per [`checkbox.md`](../design-rules/components/forms/checkbox.md)) and a bulk-action toolbar above the table.

**Violations**

- A switch in a table cell marking item state (*flagged*, *archived*, *published*) — warning (re-evaluate whether the column should be a Status / Tag / Label for display-only, or a Status Chip for editable state)
- A checkbox in a table cell marking item state (not row-select) — warning (re-evaluate as above)
- Row-select checkboxes and item-state checkboxes mixed in the same table — error (the visual collision makes it ambiguous which is which; pick one pattern and use the other column-shape for the other use case)
- A per-row Dropdown / Select used for editable state with 2–4 options where a Status Chip would name the state on the chip — note (Dropdown is not wrong here, but Status Chip tends to read better for small-N state choices; revisit once Status Chip is formally documented)

**Examples**

✓ A *Customers* table with a *Status* column rendered using the Status component (Active / Inactive / Pending). The cell shows the value; editing happens via a row-action menu.

✓ An *Articles* table with a *Status* column showing *Published* / *Draft* / *Archived* as Tag components. Clicking the tag opens an edit drawer where the user changes the state via a Select.

✓ A *Customers* table with a row-select column on the left (checkboxes per [`checkbox.md`](../design-rules/components/forms/checkbox.md) *Every checkbox has an accessible name*) for bulk action — separate from any item-state column.

✓ A *Permissions* admin table where each row is a permission (*Can edit invoices*, *Can delete records*, *Can approve expenses*) and the toggle in the row enables / disables that permission. The row's primary cell is the permission name — that names the toggle. Same pattern works for feature-flag admin views and notification-preferences matrices.

✗ An *Articles* table with a *Published* column rendered as switches per row — users have to look up the column header to know what they're toggling, and the table becomes a wall of binary controls with no contextual labelling.

✗ A table with a *Done* column of checkboxes that toggle individual row completion — should be a Status component (Done / Pending) with row-actions for state transitions.

---

## Rule: Writing labels for switches and checkboxes

**Description**

Switch and checkbox labels are read alongside the control, not as part of a sentence. They should describe **what's being toggled or selected**, not pose a question. *Dark mode* reads as a setting name; *Do you want to enable dark mode?* reads as a survey question and adds noise.

Keep labels:

- **Action-focused** — name the setting, the feature, or the choice. The control's state (on / off, checked / unchecked) is the answer; the label is the question's noun, not the full question.
- **Concise** — a few words. The label is paired with the control, not floating prose.
- **Sentence case** — consistent with Atlas's typography conventions.
- **Affirmative** — *Email notifications* toggles on for *enabled*; avoid double-negatives like *Don't send emails* which invert the user's mental model.

**How to Apply**

1. **Pick the noun phrase or action being toggled:**
   - *Dark mode* (noun phrase — a named feature)
   - *Email notifications* (noun phrase — a named system)
   - *Auto-save* (compound noun — a named behaviour)
   - *Send me product updates* (action — describes what enabling does)
   - *I agree to the terms* (action — for legal acknowledgment, where the first-person framing is the convention)
2. **Don't ask a question.** *Do you want to enable dark mode?* / *Should we send you notifications?* / *Are you sure?* all add noise without adding information. The user knows the control toggles something; the label only needs to say what.
3. **Avoid double negatives.** *Disable notifications* toggling on for *disabled* is confusing. Use the affirmative — *Notifications* toggling on for *enabled*.
4. **Match the family.** When multiple controls in a section share a theme (a *Notifications* panel with three toggles), use consistent label voice: *Email notifications* / *Push notifications* / *SMS notifications* — not *Email* / *Receive push messages* / *Send me texts*.

**Violations**

- Switch label phrased as a question (*Do you want to enable X?*) — warning
- Switch label that doesn't describe what's being toggled (*Toggle this*, *Switch*, *On/Off*) — warning
- Checkbox label phrased as a question (*Do you agree?*) — warning (except where the first-person affirmative is the natural form, e.g. *I agree to the terms*)
- Inconsistent label voice across a group of related controls — note (e.g. one toggle says *Email notifications* and the next says *Receive push messages* — the second should match the first's noun-phrase pattern)
- Double-negative label (*Disable auto-save* that toggles off for *auto-save disabled*) — error (use the affirmative)

**Examples**

✓ *Dark mode* — noun phrase, names the feature.

✓ *Email notifications* / *Push notifications* / *SMS notifications* — consistent noun-phrase voice across a group.

✓ *Auto-save* — compound noun, names the behaviour.

✓ *Send me product updates* (checkbox in sign-up form) — action describing what enabling does.

✓ *I agree to the terms* (checkbox above *Sign up* button) — first-person affirmative, the conventional form for legal acknowledgment.

✗ *Do you want to enable dark mode?* — question form; just say *Dark mode*.

✗ *Should we send you notifications?* — question form; just say *Email notifications*.

✗ *Disable auto-save* (toggling on for *auto-save disabled*) — double-negative; use *Auto-save* with the toggle on for enabled.

✗ One toggle labelled *Email notifications* and the next labelled *Receive push messages* — inconsistent voice; align to noun-phrase pattern across the group.

---

## Related Rules

- [`../design-rules/components/forms/toggle-switch.md`](../design-rules/components/forms/toggle-switch.md) — the toggle component itself (anatomy, states, sizing, validation behaviour, accessibility). Selection sub-family sibling.
- [`../design-rules/components/forms/checkbox.md`](../design-rules/components/forms/checkbox.md) — the checkbox component itself. Selection sub-family sibling.
- [`../design-rules/components/forms/radio-button.md`](../design-rules/components/forms/radio-button.md) — the radio component itself. Selection sub-family sibling.
- [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md) — anchor of the value-entry sub-family. The selection sub-family is documented locally rather than inherited from input.
- [`../design-rules/components/table.md`](../design-rules/components/table.md) *(pending)* — table component rules; *Avoid switches and checkboxes in tables* cross-references that file once it lands.
- [`../design-rules/components/status.md`](../design-rules/components/status.md) *(pending)* — Status component for item-state display in tables (alternative to switches/checkboxes per Rule 2).
- [`../design-rules/components/status-chip.md`](../design-rules/components/status-chip.md) *(pending)* — Status Chip for editable per-row state (the small-N alternative to per-row Dropdown).
- [`../design-rules/components/labels.md`](../design-rules/components/labels.md) — Label component for type / category display, sometimes used in tables.
- [`validation-feedback.md`](validation-feedback.md) — form-level validation rules; checkbox and radio participate in form-submit validation, switch does not (it commits immediately, so error feedback is post-action — see [`toggle-switch.md`](../design-rules/components/forms/toggle-switch.md) *Validation behaviour*).

---

## Open Questions

- **`status-chip.md` drafting.** *Avoid switches and checkboxes in tables* recommends Status Chip as the preferred control for editable per-row state, but the component is undocumented and missing a formal Figma design (current sketch in the [Atlas Component Development Workfile](https://www.figma.com/design/vCb2O3BLUotY1JdJ6rCBFf/Atlas-Component-Development--Workfile-?node-id=5094-19516)). Needs (a) Figma library entry with formal anatomy / states / sizing, (b) `status-chip.md` rule file once the Figma lands, (c) Astro React component if not already shipped.
- **`table.md` cross-reference.** Once drafted, the table component file should cross-reference this rule's *Avoid switches and checkboxes in tables* for state-display columns (Status components, Tags, Labels, Status Chip). Currently the cross-reference is forward-only.
- **`status.md` drafting.** Rule 2 recommends a Status component for item-state display, but `status.md` is currently a stub. Drafting it completes the *what to use instead of a cell-level switch* answer for the display-only case.
- **Label voice as a wider pattern.** *Writing labels for switches and checkboxes* covers label voice for the two controls specifically; the same voice principles apply broadly across Atlas form components. Worth considering whether to extract the rule into a wider `patterns/form-labels.md` once 3+ form-field rules reference it. Atlas's TextVault may already cover this domain — verify and consolidate.
- **Master-toggle pattern.** Some product flows would benefit from a *master toggle* pattern (one parent toggle controls + reflects N children). [`toggle-switch.md`](../design-rules/components/forms/toggle-switch.md) *Multiple toggles together* explicitly says no `SwitchCollection` because there's no shared state; a master-toggle pattern would re-open that question. Filed as a tracked possibility.


---

## patterns/chips-vs-buttons.md

# Chips Vs Buttons Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document when to use an interactive chip and when to use a button — covers selection, filtering, and action contexts.

---

## patterns/data-density.md

# Data Density Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document when to use compact vs. comfortable layouts in tables, lists, and forms.

---

## patterns/dependent-pickers.md

# Dependent Pickers

> **Status: DRAFT — pending team review per decision #64.**

A **dependent picker** is a Select, Dropdown, or Combobox whose options are scoped by another picker's selection. The classic shape is a chain: *Product → Category → Tax code*. This file is the cross-component home for the flow — how the pickers coordinate, what happens when the user changes an upstream selection, and how to decide whether a chain is the right shape.

Per-picker behaviour lives in [`../design-rules/components/forms/dropdown.md`](../design-rules/components/forms/dropdown.md), [`../design-rules/components/forms/select.md`](../design-rules/components/forms/select.md), and [`../design-rules/components/forms/combobox.md`](../design-rules/components/forms/combobox.md) *(pending)*. Per-row drawer behaviour lives in [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md). **NN/g** is the primary cited UX source.

---

## Out of scope

- Per-picker trigger and drawer rules — owned by the picker files.
- Native HTML cascading `<select>` — Atlas doesn't use native rendering.
- Multi-step wizards (each step on its own page or panel) — see [`../design-rules/components/stepper.md`](../design-rules/components/stepper.md) *(pending)*.
- Form-level error summary composition — see [`validation-feedback.md`](validation-feedback.md).

---

## Rule: Hard vs soft dependency

**Description**

Classify the dependency before applying any of the rules below. Test question: *"If I asked the user the downstream picker first, in isolation, would there be a valid set of options to show?"*

- **No** → **hard dependency**. Downstream options don't exist until upstream is picked. Example: per-product tax codes literally scoped per product.
- **Yes, but most options would be wrong** → **soft dependency**. Options exist as a global set; only some are valid given the upstream. Example: all tax codes exist; only some apply per product.

Hard dependencies use the trigger-disabled flow. Soft dependencies use the row-level flow. The two are mutually exclusive.

**Violations**

- Picker pair where the classification flips at runtime (data-dependent) — error (fix the data model upstream, not the UI)
- Hard treated as soft (trigger enabled, drawer opens with invalid options) — error
- Soft treated as hard (trigger disabled when options exist) — warning (over-restricts; the user can't preview the universe)

**Examples**

✓ Hard: *Product* picker with 50 products; each product has its own *Variant* picker (sizes, capacities) — without a product the variants are undefined.

✓ Soft: *Country* (195 countries); *VAT scheme* (8 schemes total); only some apply per country, but all 8 exist regardless.

✗ A *Currency* picker disabled until *Country* is picked when all currencies exist independently.

---

## Rule: Hard-dependency flow

**Description**

For hard dependencies, the downstream trigger renders disabled until its upstream is picked. The tooltip names the immediate prerequisite. The drawer never opens.

**How to Apply**

- Disable each downstream trigger until its immediate upstream is picked. Disabled-state mechanics from [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md) *Disabled state*.
- Tooltip names the immediate prerequisite (*"Pick a product first"*, *"Pick a category first"*). Owned by Text Vault.
- Chain semantics: in A → B → C → D, each downstream is gated by its immediate upstream, not the chain head. Re-picking A invalidates B, then C, then D in sequence (see *Upstream change after downstream is picked*).
- Don't hide downstream pickers entirely — per NN/g, hidden pickers hurt discoverability.
- Don't enable downstream pickers prematurely — per NN/g, leads to error-driven flows.

**Violations**

- Downstream enabled before its upstream is picked, drawer opens empty — error (the trigger should have been disabled; drawers never open empty per [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) *Empty state*)
- Downstream hidden entirely until upstream is picked — error (breaks discoverability)
- Disabled downstream without a tooltip — warning
- Tooltip blames the chain head instead of the immediate upstream — warning

**Examples**

✓ Three-step chain: *Category* and *Tax code* disabled with *"Pick a product first"* / *"Pick a category first"*. User picks a product; *Category* enables. User picks a category; *Tax code* enables.

✓ Re-picking the chain head: with all three picked, user changes *Product* — *Category* invalidates per *Upstream change after downstream is picked*; *Tax code* also invalidates because its immediate upstream did.

✗ A *Tax code* picker hidden entirely until a product is picked.

---

## Rule: Soft-dependency flow

**Description**

For soft dependencies, the downstream trigger stays enabled. The drawer handles relevance at the row level: filter the visible rows (high-cardinality) or show all with non-relevant ones disabled (low-cardinality).

**How to Apply**

- **High-cardinality (50+ options)**: filter the visible rows to relevant only. Carbon makes this its default at scale.
- **Low-cardinality (under ~50, fits without scrolling)**: show all rows; non-relevant ones use the disabled row state per [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) *Row states*. Per-row tooltip explains why (*"Not valid for {product}"*).
- Disabled rows are not focusable by keyboard (per [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md)).
- Don't mix filter and disable in the same drawer — pick one shape per picker.
- Optional cross-picker indicator: the picker's label or helper text can name the filter (*"Tax codes valid for product 'Acme'"*).

**Violations**

- Soft dependency where the downstream trigger is disabled — warning
- Drawer mixes filtered and disabled rows — error
- High-cardinality drawer showing all rows with non-relevant ones disabled — warning (use filter)
- Low-cardinality drawer filtering when seeing the full set would inform the user — warning
- Disabled rows without per-row tooltips — warning

**Examples**

✓ Low-cardinality + disable: *VAT scheme* (8 schemes); user picked *Country = Norway*; 5 apply, 3 don't — drawer shows all 8; the 3 inapplicable ones disabled with *"Not valid for Norway"*.

✓ High-cardinality + filter: *Tax code* (200+ codes); user picked *Product = Acme*; 12 apply — drawer shows only those 12. Helper text: *"Tax codes valid for product 'Acme'"*.

✗ A *Currency* picker (4 currencies total) filtering 2 out — user can't tell whether the missing ones don't exist or just aren't valid right now.

---

## Rule: Upstream change after downstream is picked

**Description**

When the user changes an upstream picker after a downstream has been picked, the downstream may become invalid. Atlas default: **invalidate + warn** — clear the validity but keep the visual reference, show an inline error.

**How to Apply**

Three options for handling the change:

- **Invalidate + warn (default)** — keep the previous downstream value visible; show inline error. Example: *Tax code* shows the previous value with *"Not valid for the new product. Pick a different tax code."*
- **Invalidate + clear** — clear the downstream entirely. Use only when keeping the previous value would be more confusing than clearing.
- **Cascade clear** — clear the downstream and all further-downstream pickers. Use when intermediate state isn't recoverable.

Atlas defaults to invalidate + warn for most flows.

- **Confirmation modal** required when the change would cascade-clear 3+ downstream selections: *"Changing the product will clear Category, Tax code, and 2 other fields. Continue?"* See [`modal-usage.md`](modal-usage.md) *Confirmation modals*.
- Error styling follows [`validation-feedback.md`](validation-feedback.md).
- Don't silently update the downstream to a "best guess" — never pick on the user's behalf.

**Violations**

- Silent invalidation (downstream becomes invalid, no inline error) — error
- Silent reselection (Atlas picks a new value on the user's behalf) — error
- Cascade clear of 3+ selections without a confirmation modal — warning
- Invalidate + clear used as default when invalidate + warn would preserve the reference — warning
- Downstream that remains valid but is unnecessarily cleared — error

**Examples**

✓ Invalidate + warn: user picked Product=Acme, Category=Tools, Tax code=T-12. Changes Product to Beehive. *Category* shows *"Tools"* with *"Not valid for Beehive. Pick a different category."* *Tax code*: same treatment.

✓ Cascade clear: user has 5 dependent pickers picked. Changes the chain head. Confirmation modal: *"Changing Project will clear 4 other selections. Continue?"* User confirms; all downstreams clear.

✗ Silent: user changes Product; *Tax code* silently switches from T-12 to T-08 because the system inferred a match.

✗ Stale: user changes Product; *Category* still shows *"Tools"* but is now invalid; form submits and backend rejects — no inline error.

---

## Rule: Before committing to a chain

**Description**

A design-review prompt, not a hard rule. Per NN/g, chained pickers compound friction — every dependency adds a step. Before committing to a chain, check whether the chain is the right shape.

**How to Apply**

Ask the following; answers should justify (not just rationalize) the chain:

- **Single combined picker?** If the joint cardinality is manageable, a single picker over the joint domain (e.g. *Product + Variant* as one row: *"Acme — 500ml"*) eliminates the dependency.
- **Wizard / multi-step form?** If steps are semantically distinct, a wizard ([`../design-rules/components/stepper.md`](../design-rules/components/stepper.md) *(pending)*) makes the order explicit.
- **Flatter data model?** If users intuit a flat list, the chain may be forcing the developer's mental model on them.
- **Known answer or exploration?** Chains work for known answers. Chains hurt exploration (the user wants to see the option universe without committing upstream).
- **Failure mode?** If users frequently change upstream after committing downstream, the chain is fighting their workflow.

If the answers don't justify the chain, document a different shape.

**Violations**

This rule has no lint violations — it's a design-review prompt. The closest is a chained-picker design landing in production without this review — a process gap, not a rule gap.

**Examples**

✓ A team proposed *Country → State → City* (3-step). Review found users almost always know the full address; replaced with a single Combobox autocompleting full addresses.

✓ A team proposed *Customer → Project → Task* (3-step). Review found experienced users know all three at the start; replaced with one combined picker for experienced users and a wizard for new users.

✓ A team proposed *Product → Tax code* (2-step). Review confirmed the chain: tax codes are per-product, exploration without committing isn't a real use case.

---

## Related Rules

- [`../design-rules/components/forms/dropdown.md`](../design-rules/components/forms/dropdown.md) *Disabled trigger when no content to show* — per-picker piece for hard dependencies.
- [`../design-rules/components/forms/select.md`](../design-rules/components/forms/select.md) *Disabled trigger when no content to show* — same for Select.
- [`../design-rules/components/forms/combobox.md`](../design-rules/components/forms/combobox.md) *(pending)* — picks up the same when drafted.
- [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) *Row states* — disabled rows for soft dependencies.
- [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) *Empty state* — drawers never open empty.
- [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md) *Disabled state* — disabled mechanics.
- [`validation-feedback.md`](validation-feedback.md) — inline error composition into form-level summary.
- [`modal-usage.md`](modal-usage.md) *Confirmation modals* — confirmation modal for cascade-clear.
- [`../design-rules/components/stepper.md`](../design-rules/components/stepper.md) *(pending)* — wizard alternative.

---

## Open Questions

- **Atlas `DependentPicker` component / hook** — should Atlas formalize a reusable React primitive? Team decision once 2–3 flows ship with the pattern.
- **Cascade-clear threshold** — 3+ is a starting heuristic; measure once instrumented.
- **High-vs-low cardinality cutoff** — 50 is the heuristic; may differ per content type (country lists vs tax-code lists).
- **Mid-chain change with downstream still valid** — default is to leave it alone; confirm.
- **Combobox create-new in a chain** — should create-new know about the upstream context?


---

## patterns/destructive-actions.md

# Destructive Actions Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document how to handle delete, archive, and other irreversible actions — when to use confirmation modals, inline warnings, or undo patterns.

---

## patterns/empty-states.md

# Empty States Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document messaging, imagery, and calls-to-action for empty states (no search results, no data, no content).

---

## patterns/error-handling.md

# Error Handling Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document error messages, error states, recovery actions, and when to use errors vs. warnings.

---

## patterns/feedback-button-usage.md

# Feedback Button Usage Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document when and when not to use feedback buttons across the product — covers placement, frequency, and context rules to avoid overuse.

---

## patterns/icon-usage.md

# Icon Usage Rules

> **Status: PARTIAL.** Meta-rules below are stable; the icon-to-action mapping table is not yet drafted — see *Open Questions*.

Icons help users recognise actions quickly, especially in icon buttons where there's no label. The system relies on **one canonical Atlas icon per action**, used consistently across pages, products, and teams. For Atlas's icon **source** (the Atlas library, Material as fallback, the selection process for new icons), see [`design-rules/foundations/icons.md`](../design-rules/foundations/icons.md).

---

## Rule: Same action always uses the same icon

**Description**

Once Atlas maps an action to an icon, every Tripletex product uses that same icon for that action. Inconsistent icon choices fragment users' mental models — if *Save* is a disk in one product and a cloud arrow in another, users have to relearn the iconography in each context.

**How to Apply**

When you need an icon for an action:

1. **Identify the action** (Save, Delete, Settings, Add, Search, Edit, Download, etc.).
2. **Check the icon-to-action mapping table below.** If the action is mapped, use the listed Atlas icon.
3. **If the action isn't mapped yet**, follow the icon-selection process in [`foundations/icons.md`](../design-rules/foundations/icons.md) *Icon source — Atlas first*: check the Atlas library; if no Atlas icon fits, find a Material starting point; coordinate with the Astro design system team to add it. Once approved, the team updates the table below.

**Violations**

- Same action using different icons across products — error
- New icon introduced for an existing action without coordinating with the Astro design system team — error
- Icon used that contradicts an established Atlas mapping — error

**Examples**

✓ *Save* uses the same Atlas icon in every Tripletex product.

✗ Product A uses a disk icon for *Save*, Product B uses a cloud-arrow icon for *Save*.

---

## Icon-to-action mappings

**Status:** not yet drafted.

The table will list one canonical Atlas icon per common action — Save, Delete, Add, Settings, Close, Search, Edit, Download, and others. Until it lands, browse the Atlas library directly per [`foundations/icons.md`](../design-rules/foundations/icons.md).

| Action | Atlas icon | Notes |
|---|---|---|
| *Pending* | | The team is drafting this mapping. |

---

## Related Rules

- [`design-rules/foundations/icons.md`](../design-rules/foundations/icons.md) — icon source-of-truth, selection process, Atlas vs Material relationship.
- [`design-rules/foundations/tokens.md`](../design-rules/foundations/tokens.md) — icon size tokens.
- [`design-rules/components/buttons.md`](../design-rules/components/buttons.md) — icon buttons; icon placement inside labelled buttons; back-button carve-out.
- [`design-rules/components/forms/input.md`](../design-rules/components/forms/input.md) — type indicators (icons per input type).
- [`popover-usage.md`](popover-usage.md) — icon-button tooltips.

---

## Open Questions

- **Icon-to-action mapping table** — the canonical list of (action → Atlas icon) pairs isn't drafted yet. Once the team agrees on the common-action set, populate the table above. Tracked in `TODO.md`.
- **Mapping update process** — when a new action is mapped, is the workflow Slack discussion → Figma update → PR to this file, or all three in lockstep? Confirm and document.


---

## patterns/loading-states.md

# Loading States Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document when to use spinner vs. skeleton vs. progress indicator — page-level vs. component-level loading, minimum display durations.

---

## patterns/modal-usage.md

# Modal Usage Rules

> **Status: DRAFT — pending team review per decision #44.**

When to reach for a modal — and when not to. Modals are the most interrupting surface in Atlas: they take the user out of the flow they were in and demand attention. That makes them powerful for focused tasks and a source of fatigue if overused. The component-level rules for *what a modal looks like and how it behaves* live in [`../design-rules/components/modal.md`](../design-rules/components/modal.md); this file is about *when* a modal is the right answer.

The general principle: **a modal is an interruption — its cost is the user's flow.** Use one when interrupting the user is the helpful thing to do, not when it's merely convenient for the developer or designer.

For what happens to user-entered data when a modal is dismissed, see [`state-preservation.md`](state-preservation.md).

---

## Rule: When to use a modal vs alternatives

**Description**

A modal is the right component when an action genuinely needs the user's full attention, has a clear start and end, and would be served less well by any of the less-interrupting alternatives in Atlas. If you can't say yes to all three, the modal is probably the wrong choice — Atlas has six other patterns designed to communicate without breaking flow.

**How to Apply**

Before adding a modal, run the **three-question pre-flight**:

1. **Focused attention** — does the user genuinely need to be interrupted from the page they're on (not *"would be nice to highlight,"* but *"must address before continuing"*)?
2. **Discrete task** — does the action have a clear start and clear end, rather than being a continuous workflow or browsing experience?
3. **Better than alternatives** — would none of the less-interrupting patterns (inline edit, inline-editable table row, drawer, banner, notification, alert, full page) serve the user better?

If any of those is **no**, use a different pattern. The alternatives table:

| Pattern | Use when… |
|---|---|
| **Inline edit** | A small edit to a single field on a record without leaving context. |
| **Inline-editable table row** | Editing structured data inline (e.g. invoice line items) where the row is the natural unit. |
| **Drawer** | Browsing or editing detail in a side panel without leaving the parent context. Many drawer-friendly tasks are also modal-friendly — choose drawer when *staying in context* matters more than focusing the user. |
| **Banner** | System-level information relevant to most users on the page — see [`banner-usage.md`](banner-usage.md). |
| **Notification** | Transient confirmation after an action completes — auto-dismissing, top-right. |
| **Alert** | Inline message scoped to a single section or component. |
| **Page (full route)** | A complex multistep workflow that has its own URL — the user navigated there, it isn't an interruption. |
| **Modal** | A focused, interrupting task with a clear start and clear end. |

**Violations**

- Modal used for content a banner, alert, or notification would have communicated — warning
- Modal used for a continuous workflow that should be its own page — warning
- Modal used to highlight or promote content the user didn't ask to see — error (also covered by *Don't open modals unsolicited* below)

**Examples**

✓ A *Lock accounting period* modal — irreversible, focused, discrete. Alternatives wouldn't fit.

✓ An *Edit comment* modal opened from a comment row — user clicked Edit; the task is focused and short.

✗ A modal showing recent activity on a record — better as a drawer (browsing-style, in-context).

✗ A modal walking the user through a five-step onboarding sequence — better as a dedicated page or a guided in-context flow.

---

## Rule: Never stack modals (no modal-from-modal)

**Description**

Only one modal is on screen at a time. An action inside a modal must not open another modal on top of the first. Stacking modals confuses dismissal (which one does Esc close?), defeats the focused-attention rationale (the user is now juggling two interruptions), and creates ambiguous z-order. The *Modal stack order* rule in [`../design-rules/components/modal.md`](../design-rules/components/modal.md) already forbids two modals coexisting; this rule covers the *flow design* implication: don't lay out a task that requires it.

**How to Apply**

When a flow inside an open modal seems to need a second modal — a confirmation, a related sub-edit, a *details* expansion — redesign instead. Pick one of:

1. **Stepper inside the same modal** — multi-step content stays in one surface, with Next / Previous controls per [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Modal footer button group* (stepper exception).
2. **Inline body swap** — the modal's outer chrome (title, footer) stays; the content area swaps to the next state. Useful for confirm-inside-edit flows.
3. **Close-and-reopen** — close the first modal, then open the second with the relevant context. Best when the second modal is a genuinely separate task.

Modals and drawers are also mutually exclusive (per `modal.md` *Modal stack order*). The same redesign rules apply if a flow seems to need a drawer-on-top-of-modal or modal-on-top-of-drawer.

**Violations**

- Two modals open at the same time — error (also enforced by [`modal.md`](../design-rules/components/modal.md) *Modal stack order*)
- A button inside a modal opens a second modal — error
- A modal opening a drawer (or vice versa) — error
- Designing a flow whose only working implementation requires nested modals — warning

**Examples**

✓ A multi-step *Bulk import customers* modal uses a built-in stepper — the same modal showing each step in turn.

✓ An *Edit customer* modal with a Delete button — clicking Delete swaps the modal body to a confirmation state (*Delete this customer?*), keeping the same modal chrome and footer.

✓ *Manage tags* modal closes, then *New tag* modal opens with the relevant prefilled context.

✗ An *Edit customer* modal whose Delete button opens a separate *Are you sure?* modal on top.

✗ A modal whose action button opens a drawer to edit a related record.

---

## Rule: Don't open modals unsolicited

**Description**

A modal must be opened in response to a user action — a click, a key press, a form submission, an explicit choice. Opening a modal because the page loaded, because the user scrolled, because a timer fired, or because of a marketing campaign is unsolicited interruption and is forbidden. The user is in the middle of doing something; reaching out to grab their attention without their consent is the design equivalent of a phone call from a stranger.

A narrow set of system-initiated cases are allowed because they're still anchored to the user's task — see *Allowed exceptions* below.

**How to Apply**

**Forbidden triggers** — the modal *must not* open on:

- Page load (NPS surveys, marketing announcements, *What's new* prompts, onboarding tours that start before the user did anything).
- Scroll position.
- Idle timer (except as part of the session-expiry exception below).
- Time of day.
- Marketing campaign / A/B-tested promotion.
- Any condition the user didn't directly cause.

**Allowed exceptions** — system-initiated but anchored to the user's current task:

1. **Re-authentication** when the user's session has expired *and they're attempting an authenticated action* (so the modal is anchored to their click, not to an idle timer). Inline alternatives — banner with redirect, full-page sign-in — should be considered first; only use a modal when staying on the current page is meaningfully better than redirecting.
2. **Session-expiry warning** for long-form workflows where automatic save isn't possible and losing the work would harm the user (e.g. tax-return draft about to time out). Warn early enough that the user can act, never after the data is already lost.
3. **Critical task-blocking error** that the user must acknowledge before they can continue (e.g. permission revoked mid-action, server-side validation failure that requires user choice to recover). Consider a full-page error state or inline alert first; the modal is the last resort when the user genuinely cannot proceed without an active acknowledgment.

For non-task-blocking system messages (releases, news, recommended setting changes, upsells) use a banner, notification, or — when commercial — the Product Spotlight Banner per [`product-spotlight-banner-usage.md`](product-spotlight-banner-usage.md).

**Violations**

- Modal opens on page load to show an announcement, NPS prompt, or marketing message — error
- Modal opens because the user scrolled past a threshold — error
- Modal opens after an idle timer alone — error (the session-expiry exception above is the only sanctioned use of an idle-anchored modal, and only when paired with the user's active task)
- Modal used for a re-auth flow where the user wasn't actively trying to do an authenticated action — warning (the prompt is unsolicited because it isn't anchored to the user's intent)
- *"Don't show again"* checkbox used to make an otherwise-forbidden unsolicited modal acceptable — error (the rule is about whether the modal should open at all, not how often)

**Examples**

✓ User clicks *Lock period* → confirmation modal opens.

✓ User submits a form whose token has expired → re-authentication modal opens, anchored to the submit attempt; on success the original submit retries.

✓ User has been working on an unsaved tax return for 55 minutes; a session-expiry warning modal appears at the 55-minute mark with a *Save and continue* action — *not* at the 60-minute mark when the data is already gone.

✗ User logs in and the dashboard greets them with a *Welcome back! Try our new feature* modal.

✗ User scrolls 60% down the article and a *Subscribe to our newsletter* modal opens.

✗ An NPS survey modal opens 30 seconds after the user lands on a page.

✗ A re-auth modal opens because the user has been idle, even though they haven't tried to do anything.

---

## Rule: Confirmation modals

**Description**

A confirmation modal asks the user to confirm an action before it runs. Use one when the action is irreversible, has wide blast radius, or could be misinterpreted from context. Don't use one for trivially reversible actions or routine saves — the friction of an extra click outweighs the protective value when undo is cheap.

The action button label **mirrors the action verb** so the user can read the modal and understand what saying *"yes"* means without having to back-reference the title. Generic labels like *OK* or *Yes* are forbidden because they decouple the click from the action.

Destructive-confirmation specifics — typed-name confirmation for high-risk actions, danger-styled action buttons, additional friction patterns — live in [`destructive-actions.md`](destructive-actions.md) *(not yet documented; see `TODO.md`)*. This rule covers when and how to use a confirmation modal in general; the destructive-action subset has its own pattern file.

**How to Apply**

Use a confirmation modal when **at least one** is true: the action is **irreversible** (cannot be undone — delete without trash, archive without restore, lock period, finalize), has a **wide blast radius** (affects many records, locks a workflow for other users, moves money), or is **ambiguous from context** (a user could click the action button without realizing what it does — small icon, terse label, ambiguous placement).

Don't use one when the action is trivially reversible (toggle a setting, change a value, edit a draft — users undo by the same path they used to make the change), when the action is a routine save (the save button + success notification is enough), or when the user has already confirmed earlier in the same flow (don't double-confirm).

**Anatomy:**

1. **Title** — question form (*Delete this customer?*) or imperative (*Confirm period lock*). Avoid passive or vague phrasing (*This action will…*).
2. **Action button label** — mirrors the action verb. *Delete*, *Archive*, *Lock period*, *Move to inbox* — never *OK*, *Yes*, or *Confirm* alone.
3. **Cancel button label** — *Cancel* (or the Text Vault equivalent for the locale). Cancel is required per [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Modal footer button group* for any modal with user-mutable state.
4. **Body** — state what the action does and what the consequence is. Include any specifics that affect the decision (number of affected records, irreversibility, who else is affected).
5. **Destructive specifics** — for high-risk actions (mass delete, account closure, period lock with downstream effects), follow the additional rules in [`destructive-actions.md`](destructive-actions.md) *(pending)*. At minimum, the action button uses the result-state error colour from [`../design-rules/components/buttons.md`](../design-rules/components/buttons.md) once that destructive-button rule lands.

**Violations**

- Confirmation modal action button labelled *OK*, *Yes*, or *Confirm* alone — error
- Confirmation modal title that doesn't say what's being confirmed — warning
- Confirmation modal used for a trivially reversible action (toggle, simple edit) — warning
- Routine save preceded by a confirmation modal — warning
- Two confirmation modals in the same flow (*Are you sure you want to delete this?* → *Really sure?*) — warning (also covered by *Never stack modals* above)

**Examples**

✓ Title *Delete customer Acme AS?* / Body *This will remove the customer and all unposted invoices. This cannot be undone.* / Buttons `[Delete] [Cancel]`.

✓ Title *Lock accounting period 2026-04?* / Body *Once locked, no more transactions can be posted to this period. You can unlock it from period settings.* / Buttons `[Lock period] [Cancel]`.

✗ Title *Are you sure?* / Buttons `[Yes] [No]` — the user has to back-read the originating context to know what they're saying yes to.

✗ A confirmation modal before saving a draft note — saving a draft is trivially reversible.

✗ Action button labelled *Confirm* with no verb mirroring the action.

---

## Related Rules

- [`../design-rules/components/modal.md`](../design-rules/components/modal.md) — component-level rules: anatomy, sizing, dismissal, keyboard interactions, isolation, stack order, footer button group, form-field spacing, inline errors, async commit.
- [`state-preservation.md`](state-preservation.md) — what happens to in-modal data on dismissal vs commit vs navigation (covers modals and drawers).
- [`banner-usage.md`](banner-usage.md) — when a banner is the right answer instead.
- [`popover-usage.md`](popover-usage.md) — tooltip-vs-popover for non-interrupting rich content.
- [`destructive-actions.md`](destructive-actions.md) *(pending)* — typed-name confirmation, danger styling, friction patterns for high-risk actions.
- [`product-spotlight-banner-usage.md`](product-spotlight-banner-usage.md) — for commercial messaging that would otherwise be tempting to put in a modal.
- [`../design-rules/components/banner.md`](../design-rules/components/banner.md), [`../design-rules/components/notification.md`](../design-rules/components/notification.md), [`../design-rules/components/alert.md`](../design-rules/components/alert.md) — alternative components referenced in the alternatives table.

---

## Out of Scope of This File

- **Dialog** is a separate surface, not a modal variant. Dialog usage rules are out of scope here and not yet documented.
- **AI Assistant Modal** uses a different container with its own usage rules — see [`../design-rules/components/ai-assistant-modal.md`](../design-rules/components/ai-assistant-modal.md).
- **Drawer usage** (when to use a drawer vs alternatives) lives or will live in its own pattern file. This file references drawer in the alternatives table but does not own its rules.
- **Mobile modal behaviour** — Figma spec exists, implementation pending. Mobile triggers and dismissal behaviour are undefined until the implementation lands.


---

## patterns/navigation.md

# Navigation Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document how product teams design navigation within their own pages — active states, tabs as navigation, in-page navigation. Does not cover Spacesuit..

---

## patterns/notification-usage.md

# Notification Usage Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document when to trigger a notification, content rules, stacking behavior, and auto-dismiss timing.

---

## patterns/onboarding.md

# Onboarding Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document empty screen patterns, feature introduction, and first-use guidance.

---

## patterns/popover-usage.md

# Popover Usage Rules

Tooltips and popovers both surface additional information about an element, but they serve very different purposes. Mixing them up — putting rich content in a tooltip, or using a popover where a label would do — confuses users about what to expect when they hover or tap.

The short version:

- **Tooltip** — a label-only, non-interactive hint that appears on hover.
- **Popover** — rich, potentially interactive content (text, links, graphics, charts, AI clarifications) that appears on hover (desktop) or tap-and-hold (mobile, where it opens as a bottom sheet).

Both can coexist on the same element — e.g. an icon button with a `Save` tooltip and a popover that explains what saving will do.

**Note on terminology.** *Bottom sheet* is Atlas's term for the full-width mobile surface a popover opens into on tap-and-hold. It is distinct from the [`Drawer` component](../design-rules/components/drawer.md) (the anchored option-list surface for desktop). Atlas keeps the two terms separate to avoid the term-overload that prompted the *Popup Menu → Drawer* rename (see [`../design-rules/components/popup-menu.md`](../design-rules/components/popup-menu.md)).

---

## Rule: Tooltips for labels, popovers for rich content

**Description**

Tooltips are reserved for one job: showing the label of an element that has no visible text label, like an icon button. They contain nothing more than a short label. Anything richer — explanations, links, charts, illustrations, AI suggestions, multi-line guidance — belongs in a popover. This separation lets users learn a simple expectation: **tooltips never have anything to interact with, popovers do.**

Use a **tooltip** when the element is an icon button or other unlabelled control (every icon button must have one), and there is nothing to read or interact with beyond the label that would have appeared as visible text.

Use a **popover** when you need context beyond a simple label — interactive elements (links, buttons, inputs), graphics / illustrations / charts, AI clarifications or automation suggestions, or help / guidance for a feature.

A single element can have both: a tooltip on hover for the label, plus a popover (also on hover, or on tap-and-hold on mobile) for the richer content.

**How to Apply**

1. **Every icon button must have a tooltip** with its label — see [`../design-rules/components/buttons.md`](../design-rules/components/buttons.md) *Icon buttons*.
2. **If the element needs more than a label, add a popover** — don't pad the tooltip.
3. **Desktop:** both tooltip and popover open on hover.
4. **Mobile:** the tooltip stays on hover where applicable; the popover opens as a **bottom sheet** on tap-and-hold (full-width surface anchored to the bottom of the viewport, dismissed by tapping outside or swiping down).
5. **Keep tooltip text to one short label.** No sentences, no calls to action, no links.

**Violations**

- Icon button without a tooltip — error
- Tooltip containing more than a label (sentence, link, call to action) — error
- Popover used as a tooltip (popover with only a one-word label inside) — warning
- Complex information stuffed into a tooltip instead of a popover — warning
- Mobile-popover surface called *drawer* or *mobile drawer* in code, copy, or rules — warning (use *bottom sheet*; *Drawer* is reserved for the desktop anchored option-list surface)

**Examples**

✓ Icon button `[⋮]` with tooltip *More actions*; clicking opens a Drawer with the available actions.

✓ A *Save* button with tooltip *Save*, plus a popover on the same button explaining *Saving updates the record and syncs to all devices* with a link to learn more.

✗ Icon button with no tooltip — the user has to guess what it does.

✗ Tooltip text reads *Click here to learn more about how saving works* — that's popover content, not a label.

---

## Related Rules

- [`icon-usage.md`](icon-usage.md) — icon consistency, which is what makes the tooltip label predictable.
- [`../design-rules/components/buttons.md`](../design-rules/components/buttons.md) — icon button rules, including the tooltip requirement.
- [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) — the desktop anchored option-list surface (not the same as the mobile bottom sheet documented here).
- [`../design-rules/components/popup-menu.md`](../design-rules/components/popup-menu.md) — the *Popup Menu → Drawer* rename rationale; explains why Atlas keeps the surface-name space disambiguated.


---

## patterns/responsive.md

# Responsive Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document how layouts adapt across breakpoints and which components change behavior at mobile/tablet/desktop.

---

## patterns/saving-feedback.md

# Saving Feedback Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document page-level save patterns beyond action buttons and how to communicate save state to users.

---

## patterns/search.md

# Search Pattern

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document when to use global vs. local search, search input placement, results display, empty states, and loading behavior.

---

## patterns/state-preservation.md

# State Preservation Rules

> **Status: DRAFT — pending team review per decision #44.**

What happens to user-entered data when the user moves away from a surface that holds in-progress input — by closing a modal or drawer, committing a save, navigating off the page, or switching between tabs. The rule covers **modals**, **drawers**, and **tabs** — the contexts in Atlas where in-progress input can be lost if state isn't preserved correctly.

The general principle: **stepping away from a surface is *"not now,"* not *"throw it away."*** Users frequently switch tabs or close a modal to look at something else, then return; losing their work in that moment punishes correct behaviour.

---

## Rule: State preservation in modals, drawers, and tabs

**Description**

When a user is partway through entering data in a modal, drawer, or tab, what happens to that data depends on what the user does next — dismiss, commit, navigate away, or switch tabs. The rule below names each outcome. Persistence is in-memory only, scoped to the current browser session, and excludes sensitive fields.

**How to Apply**

Four cases. The first three are terminations; the fourth is intra-page movement that's not a termination at all.

1. **Dismissal preserves.** Closing the surface via close button, backdrop click (modals), Esc key, or any other dismissal path keeps the user's in-progress data in memory. Re-opening the same surface restores the draft, with all fields populated from where the user left off.
2. **Commit clears.** A successful save / submit / confirm drops the in-memory draft. The data is now persisted server-side and is the canonical state; re-opening the surface should pre-fill from the persisted record, not from a stale local draft. (If the commit fails, the surface stays open and the draft is still in memory — see [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Async commit behaviour* for the modal-specific case.)
3. **Navigation clears.** Navigating away from the parent page (clicking a link, hitting Back, switching to another route) clears the draft. The user has moved on; preserving the draft across navigation creates surprising *"ghost"* state that re-appears later in unexpected places.
4. **Tab switch preserves.** Switching between tabs on the same page keeps the draft state of every tab in memory. Switching away and back restores the in-progress draft exactly. A tab switch is intra-page navigation — the user hasn't left the parent page or moved on.

**Don't split a form across tabs.** Tabs work best for content organization — read-heavy navigation, related but independent sub-views. They are a poor fit for multi-step forms. If a design needs a single form to span tabs, prefer a stepper inside one tab, expandable sections, or a dedicated multi-step page. When tabs genuinely contain independent forms (e.g. settings categories), each tab's form has its own commit boundary and preservation follows the rules above.

**Sensitive fields are excluded from preservation.** Passwords, MFA / two-factor codes, payment details (card numbers, CVVs), bank account numbers, social-security-equivalent identifiers, and any field marked sensitive are explicitly cleared on dismissal regardless of which dismissal path was used. If the user dismisses a re-auth modal halfway through typing a password, re-opening it shows an empty password field — never the prior input.

**Persistence is in-memory only and within-session.** A page reload, a tab close, or a browser quit clears the draft. Atlas does not persist drafts to `localStorage` or `sessionStorage`. This is a deliberate scope choice — within-session preservation handles the dominant case (looking-and-returning) without the complexity of storage management, expiry, cross-tab sync, or the privacy implications of persisted user input.

**Violations**

- Re-opening a dismissed modal or drawer shows empty fields the user had filled in — error
- Re-opening a surface after a successful save shows the just-saved data as a draft (the commit should have cleared it) — error
- A password, MFA code, or other sensitive field is restored after dismissal — error
- A draft from one page appears in a surface on a different page — error
- Returning to a tab the user had typed into shows it empty — error
- The draft survives a page reload, tab close, or browser restart — warning (cross-session persistence is out of scope; handle as a separate, deliberate decision)
- The draft is persisted to `localStorage` or `sessionStorage` — error (Atlas opts out — see *Out of Scope* below)

**Examples**

✓ User opens an *Edit customer* drawer, types into Name and Address, clicks the backdrop. Re-opens the drawer — Name and Address are restored.

✓ User saves the customer edit. Re-opens the drawer — fields are pre-filled from the saved record; no draft state remains.

✓ User navigates from the customer page to the dashboard, then back to the customer page, then opens the edit drawer — fields pre-fill from the saved record. Any earlier draft is gone, because the user navigated away.

✓ User types a password into a re-auth modal, dismisses it via Esc, re-opens it — the password field is empty.

✓ User starts typing a comment on the *Comments* tab of an invoice page, clicks the *Activity* tab, then clicks back to *Comments* — the half-typed comment is still there.

✗ User types half a comment in a modal, presses Esc, re-opens — the comment field is empty.

✗ User types into a field on one tab, switches to another tab, comes back — the field is empty.

✗ User saves an entry and re-opens — the just-saved value is shown as a *"draft"* diff against the persisted record.

✗ User types a password, dismisses the modal, re-opens it — the password is restored from in-memory state.

✗ User starts editing a customer in a drawer, navigates to a different customer's page, opens the edit drawer there — the previous customer's draft data appears in the new drawer.

---

## Related Rules

- [`../design-rules/components/modal.md`](../design-rules/components/modal.md) — modal dismissal paths (close button, backdrop click, Esc) and async-commit behaviour.
- [`modal-usage.md`](modal-usage.md) — when to use a modal vs alternatives; this rule covers what happens after dismissal.
- [`../design-rules/components/drawer.md`](../design-rules/components/drawer.md) — drawer dismissal paths and the *Outside-click + Esc dismissal* rule.
- [`../design-rules/components/tabs.md`](../design-rules/components/tabs.md) *(pending)* — tab anatomy and switching behaviour; when `tabs.md` lands it should cross-ref this rule's *Tab switch preserves* clause.
- [`auto-save.md`](auto-save.md) *(pending)* — how page-level sync state is visualised next to the page header title. Auto-save is a different concept: it covers persisted page-level edits and the icon next to the page header title that signals sync state. State preservation is about *un-persisted* draft state inside a dismissable surface.

---

## Out of Scope of This File

- **Auto-save** is a separate concept and lives in [`auto-save.md`](auto-save.md) *(pending)*. Auto-save covers persisted page-level edits and the sync indicator next to the page header title; state preservation covers in-progress draft state inside a dismissable surface.
- **Cross-session persistence** — preserving drafts across page reload, tab close, or browser restart. Currently out of scope by deliberate decision (simplicity, no storage management, privacy). Revisit only when a real product need emerges and treat it as a new, larger rule.
- **Time-bound expiry within a session** — currently no expiry; a draft kept open for hours is still valid. Revisit if drafts can grow stale enough to mislead the user.
- **Cross-tab synchronization** — if the user opens the same record's drawer in two **browser tabs**, each browser tab's draft is independent (not the same as in-page tabs covered by *Tab switch preserves*). Cross-tab sync is out of scope.
- **Form validation state** (inline errors, dirty markers) — preserved alongside the draft in memory but not the focus of this rule. The validation-feedback contract lives in [`validation-feedback.md`](validation-feedback.md).


---

## patterns/table-usage.md

# Table Usage Rules

> **Status**: Not yet documented. See `TODO.md` for this task.

This file will document data density (compact vs. comfortable), sorting, row selection, bulk actions, empty states within tables, and pagination vs. infinite scroll.

---

## patterns/validation-feedback.md

# Validation Feedback Pattern

> **Status: DRAFT — pending team review per decision #52.** Open positions worth re-examining are tracked in the *Future Review* section at the foot of the file (single-field-form summary behaviour and live-re-validation cadence are the two most worth team input on).

How form validation is communicated to the user — the form-level error summary on a failed submit, the per-field inline errors, how the two compose, and what happens as the user fixes invalid input. This file owns the *form-level* surface; the *field-level* visual contract (Error marker, surface tokens, opposite-side icon, below-field message) lives in `design-rules/components/forms/input.md` § "Content type markers" and is referenced rather than restated here.

The general principle: **point the user at the problem, then get out of the way.** A failed submit produces two surfaces working together — a summary that names what's wrong and lets the user navigate to it, and per-field markers that show the user what to fix once they're there. Neither surface alone is enough; both surfaces together is the rule.

For when to use a modal vs. validation feedback (you don't), see [`modal-usage.md`](modal-usage.md). For the field-level Error marker contract, see [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md). For the Alert component used as the summary container, see [`../design-rules/components/alert.md`](../design-rules/components/alert.md).

**Note for high-stakes submissions.** This rule covers form validation feedback — the input-correction layer. For high-stakes submissions, additional patterns layer on top of this one:

- **Review / confirm before final submit.** Flows under [WCAG 2.2 SC 3.3.4 — Error Prevention (Legal, Financial, Data)](https://www.w3.org/WAI/WCAG22/Understanding/error-prevention-legal-financial-data.html) — invoicing, payroll, banking, tax, year-end reports — require either reversibility, a checked-and-correctable input step, or an explicit review/confirm screen before the submission becomes final. The validation summary covered here handles input correction; the review/confirm screen is a separate concern that needs to be layered on top.

  **Audit-delegated signing.** For some legal flows, the confirm step is *deliberately delegated to an external system* rather than hosted in Tripletex — most commonly, audit-required AS year-end submissions (Årsregnskap) are signed in Altinn after Tripletex hands the submission off. In these cases, the design job is to make the delegation legible to the user: clearly state where the signing happens, what credential they'll use there, and what state the Tripletex flow is in while waiting for the external confirmation. Don't try to host a confirm step locally for a flow that authority logic delegates externally.

- **Step-up authentication for the highest-stakes submissions.** When a successful submit moves money, creates fraud exposure, or carries significant legal weight, the user should re-prove their identity before the submit completes. The credential class should match the flow — Tripletex uses **tiered step-up auth**, not a uniform password prompt:

  | Tier | Credential | Used for |
  |---|---|---|
  | **Federated strong-auth** | ID-porten / Altinn (BankID, MinID, etc., at the government identity provider) | Tax-authority submissions: MVA-melding, Skattemelding, A-melding, year-end reports / Årsregnskap. Tripletex must redirect to ID-porten / Altinn for the actual step-up — **do not roll a custom Tripletex prompt for these flows.** |
  | **BankID at Tripletex** | BankID | First payment to a new recipient (always); all payments if the tenant has enabled BankID payment-approval. The first-time-to-new-recipient gate is distinct from amount-threshold gating — it triggers on novelty, not size. |
  | **Visma Connect password + TOTP** | Visma Connect password + 6-digit authenticator code | Money-out flows that move company funds: salary run finalisation (Lønnskjøring), payment runs / payment proposals (Utbetalinger / Betalingsforslag). Re-verification fires **per batch** — every batch, not just above a threshold. |
  | **Password re-entry in a modal** | Tripletex / Visma Connect password | Self-service profile mutations: changing one's own email address is the canonical existing example. Sufficient for the user mutating their own account, **not** sufficient on its own for money-out flows. |

  **Two purposes** the step-up serves simultaneously: (1) **fraud prevention** — an unattended or hijacked session cannot complete a high-stakes action without re-authenticating; (2) **severity awareness** — the deliberate friction makes the user keenly aware that what they're about to do is consequential. The friction is the point; do not optimise it away as "extra steps".

  **Currently re-verified in Tripletex (descriptive):** Lønnskjøring (per batch), payment runs / payment proposals (per batch), first payment to a new recipient (additional BankID gate on top), tax-authority submissions via ID-porten / Altinn, own-email-address change (password re-entry modal).

  **Should adopt step-up auth — currently aspirational:** Per support-article audit (May 2026), the following high-stakes flows do **not** currently re-verify in Tripletex and should be reviewed for parity with money-movement flows: changing the bank account used for company payouts (today the only safety net is the downstream first-payment-to-new-recipient gate, not the account-change itself); granting another user admin / accountant privileges; closing or deleting the company account. Coordinate with the security team when prioritising these — the design rule prescribes the target state, the security team owns the threshold and credential choice.

  The exact thresholds for which flows warrant which tier are product-specific and should be set in coordination with the security team and the relevant product owner. The mechanics of each credential tier (lockout behaviour, error handling, copy, biometric variants, redirect-vs-modal) are out of scope of this file and tracked under `TODO.md` § "Identity re-verification pattern (step-up authentication)".

Flag during design review of any submission with legal, financial, or data consequences whether the validation summary alone is sufficient — often it isn't, and one or more of the above patterns should be layered on top.

---

## Rule: Show a form-level error summary on a failed submit

**Description**

When the user submits a form and one or more fields are invalid, render a form-level error summary on the same page. The summary is the navigation surface for the failed submit — it names what's wrong and gives the user a one-click path to each invalid field. The summary appears only on a submit attempt; it does not pre-empt the user by appearing on initial render or while they're still typing.

**How to Apply**

The summary appears whenever the user clicks submit (or presses Enter to submit) on a form and one or more fields fail validation — regardless of how many fields are invalid, including the single-field case.

1. On submit, run all field-level validations.
2. If one or more fields are invalid:
   - Render the form-level summary (per "Container component" and "Placement" below).
   - Render the per-field Error marker on each invalid field (per `forms/input.md` § "Content type markers").
   - Move keyboard focus to the summary (per "Focus management" below).
3. If all fields are valid, proceed with submit.
4. **Do not show the summary on initial form render.** The user hasn't done anything yet; surfacing errors pre-emptively reads as accusatory.
5. **Do not show the summary while the user is typing.** Field-level validation may run on blur (when the user leaves a field), but the summary is reserved for the submit moment.

**Violations**

- Form-level summary shown on initial render before the user has attempted to submit — error
- Summary shown while the user is still typing into a field — warning
- Submit attempt with invalid fields that produces no summary (only inline errors) — error
- Summary shown for a submit that succeeded — error

**Examples**

✓ Correct: User clicks Save on a "New customer" form with three required fields empty. The summary appears above the submit button listing the three missing fields; each field gets its inline Error marker.

✗ Wrong: User opens the "New customer" form and the summary is already visible saying "3 fields need attention" — pre-emptive validation.

✗ Wrong: User clicks Save with one invalid field and the inline Error marker appears, but no summary — pairing rule violated (see "Pair with per-field errors" below).

---

## Rule: Container component — Alert

**Description**

The form-level error summary uses the **Alert** component ([`../design-rules/components/alert.md`](../design-rules/components/alert.md)), variant Error. Alert is the right component because Alert placement is free (it can live inside a form), whereas Banner placement is constrained to under the page header (per [`../design-rules/components/banner.md`](../design-rules/components/banner.md) *Banner placement*). A Banner inside a form is forbidden generally; the only tolerated case is the transitional exception documented in `banner.md`, which is a `warning` and explicitly directs new work to use Alert instead.

**Note on the extended composition.** Alert's documented anatomy is "single item with optional follow-up link" (`alert.md` § "Alert anatomy"). The validation summary composes Alert in an extended form — heading + linked list of N field errors — that departs from this anatomy. This is an explicit and documented extension, justified by Atlas's current lack of a dedicated `ErrorSummary` component. The Astro team's future ErrorSummary component (tracked in `TODO.md` § "Dedicated `ErrorSummary` component (Astro)") will replace this composition and let Alert revert to its canonical single-item shape. Until then, the validation summary is the **only** sanctioned exception to Alert's single-item rule; do not generalise this composition to other use cases.

**How to Apply**

For page-level forms — for the modal-hosted form variant, see *Modal-hosted form variant* below.

1. Use `Alert variant="error"` as the container.
2. The Alert's contents:
   - A **heading** stating what's wrong (wording per "Wording defers to Text Vault" below).
   - A **list** with one entry per invalid field. Each entry is a link whose target is the field's `id` attribute.
   - Each list-entry text mirrors the inline field error **word-for-word** (per "Wording" below).
3. The Alert inherits the Error variant's tokens (`--surface-error-*`, `--border-error`, error icon) per `alert.md` § "Alert variants".
4. **Do not** use `Banner variant="error"` for new work. Existing usage is tolerated transitionally per `banner.md` but should migrate.
5. **Do not** use a Notification for the summary. Notifications are top-right, transient, and disconnected from the form context — wrong tool.
6. **Do not** invent a custom container with hand-rolled error styling. Compose from Alert.

**Violations**

- Form-level validation summary rendered as anything other than `Alert variant="error"` — error (existing `Banner variant="error"` usage in forms is the documented warning-severity exception per `banner.md`)
- Summary list-entry text not matching the inline field error word-for-word — warning (per "Wording")
- Summary missing a heading or a list — error
- List entries that are not links to the offending field's `id` — error

**Examples**

✓ Correct: An Alert with heading "2 fields need attention" and a list of two links: "Customer name is required" → focuses `#customer-name` field, "Email is invalid" → focuses `#customer-email` field. Same wording on each field's inline Error marker.

✗ Wrong: A bespoke red `<div>` with hand-rolled styling that imitates Alert visually but isn't the component — even if visually identical, future Alert changes won't propagate.

---

## Rule: Placement (page-level forms)

**Description**

Place the summary Alert immediately above the submit button, separated by 16px on both sides — 16px below the last form field, 16px above the submit button. The principle: "near what triggers it." The user just clicked submit and is already focused there; the summary appears where their attention is, not at the top of a form they may have to scroll back to. Match the Alert width to the form's content width.

**How to Apply**

For page-level forms — for modal-hosted forms, see *Modal-hosted form variant*.

1. Vertical spacing:
   - Last form field → **16px** → Alert (summary) → **16px** → Submit button.
2. Horizontal alignment: the Alert aligns to the same edge as the form fields (left or right depending on the form's alignment).
3. Width: the Alert matches the form's content width.
4. The Alert lives **inside** the form's flow — not floating, not sticky, not overlaid.

**Violations**

- Summary placed at the top of the form instead of above the submit button — warning (acceptable only when the submit lives somewhere unusual — e.g. floating, sticky-bottom — and the team has decided top-placement reads better; otherwise prefer above-submit)
- Summary placed outside the form (e.g. under the page header) — error (use Banner under the page header for system-level messages, not validation)
- Summary spacing not 16px above and 16px below the Alert — warning
- Summary width mismatched to the form's content width — warning
- Summary rendered as floating, sticky, or overlay positioning — error

**Examples**

✓ Correct: A "Create invoice" form has eight fields. After a failed submit, the Alert appears 16px below the last field, with 16px between the Alert and the `[Save] [Cancel]` button group below.

✗ Wrong: The summary appears at the top of a long form; the user clicked Save at the bottom of the form and now has to scroll up to read it.

---

## Rule: Pair with per-field errors

**Description**

The form-level summary never appears alone. Every field listed in the summary also renders its inline Error marker per `design-rules/components/forms/input.md` § "Content type markers". The per-field error is the load-bearing message — it tells the user *what's wrong with this field*. The summary is a navigation surface — it tells the user *how many fields are wrong and lets them jump to each*. Removing the inline errors and keeping only the summary reduces validation to a list-of-titles without explanations; removing the summary and keeping only inline errors loses the navigation affordance for long forms. Both surfaces, always together.

**How to Apply**

1. Every field referenced in the summary's link list also renders its inline Error marker (icon, surface, border tokens) per [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md).
2. Every field's inline error message text matches its corresponding line in the summary, word-for-word.
3. The inline error renders as the below-field message variant from `forms/input.md` § "Content type markers" — the second valid placement for an Error marker, used because validation messages are typically too long for a popover and the user shouldn't have to hover to read them.

**Violations**

- Form-level summary present without per-field Error markers — error
- Per-field Error markers present without a form-level summary on a multi-field failed submit — error (single-field forms still get the summary per "When to Show" above)
- Summary entry wording diverging from the inline field's error wording — warning
- Inline error rendered only as the inline icon + popover, not as the below-field message — warning (long messages should be readable without hovering)

**Examples**

✓ Correct: Summary entry "Customer name is required" → field `#customer-name` shows the same text below it, with the Error marker icon and `--surface-error-*` / `--border-error` tokens applied to the field.

✗ Wrong: Summary says "Required field missing", inline message says "This field is required" — wording diverges.

---

## Rule: Wording defers to Text Vault

**Description**

The exact wording of the summary heading, each per-error string, and any standardised phrases ("This field is required", count-aware variants like "n fields need attention", any GOV.UK-style "There is a problem" equivalents) is **not specified by Atlas**. Designers and developers consult the [Text Vault](https://cdn.tripletex.no/text-vault/index.html) team for canonical copy before shipping. Atlas only specifies the *structure*: heading + linked list, identical wording between summary and inline, instructional rather than descriptive phrasing where Text Vault offers the choice.

**How to Apply**

1. Before shipping a new validation surface, contact Text Vault for the canonical phrasing.
2. Use the phrase Text Vault provides verbatim — do not paraphrase between summary and inline.
3. If Text Vault doesn't yet have a phrase for the case, request one rather than inventing.
4. Keep the structure consistent across the surfaces (summary heading + list entries + inline messages); Text Vault owns the words, Atlas owns the structure.

**Violations**

- Custom validation copy shipped without Text Vault consultation — note (mechanically a `note`, but practically the consequence is divergent copy across teams; treat consistently)
- Summary entry wording paraphrased from the inline message — warning
- Wording inconsistency between two forms in the same product for the same validation case — warning (root cause: missing Text Vault consultation)

**Examples**

✓ Correct: Designer drafts a new "Account closure" form, contacts Text Vault for the summary heading copy, receives "1 thing needs your attention before closing this account", uses it verbatim.

✗ Wrong: Two teams ship two different summary headings ("There is a problem" and "Some fields are missing") for equivalent failed-submit cases, having drafted independently.

---

## Rule: Focus management on submit

**Description**

On a failed submit, programmatic focus moves to the summary Alert. Re-focus on **every** failed submit, not just the first — if the user submits, fixes one field, submits again, and three new fields fail, focus moves back to the summary. Each summary list entry, when activated by click or keyboard, moves focus to the field it points to via the anchor link. Keyboard users navigate from the summary to the first error without hunting; screen-reader users hear the summary the moment it appears.

**How to Apply**

1. Render the summary Alert with `tabindex="-1"` so it's programmatically focusable.
2. On every failed submit, call `.focus()` on the Alert container after it renders.
3. **The page scrolls to bring the summary into view.** If the summary is outside the user's viewport when it renders — typically because the form is long, or the placement is at the top while the user clicked submit at the bottom — the document's scroll position adjusts so the summary is fully visible. This is **page scroll, not element scroll**: the page moves to bring the summary into view, the same effect as `Element.scrollIntoView({ block: 'nearest' })` from the browser API. Do not implement this as scrolling internally inside a smaller scroll container while leaving the document where it was — the user must actually be able to see the summary they were just focused on. Respect the user's `prefers-reduced-motion` preference when choosing the scroll behaviour (jump rather than smooth-scroll when reduced motion is requested).
4. Each summary list entry is an anchor link to the field's `id`; activating the link moves keyboard focus to the field per the browser's default anchor-link behaviour. The same scroll-into-view applies — clicking a link should scroll the page so the field is visible if it isn't already.
5. Do not move focus to the first invalid field directly on submit. The summary is the entry point; the user navigates from there.
6. The Alert container's `role="alert"` (already inherited from Alert's Error variant per `alert.md`) means screen readers announce the message immediately.

**Violations**

- Failed submit with no focus change — error (keyboard users have no signal that anything happened)
- Focus moved to the first invalid field instead of the summary — warning (works, but loses the navigation affordance for long forms with multiple errors)
- Summary list entry that doesn't move focus on activation — error
- Summary not focusable (missing `tabindex="-1"`) — error
- Failed submit where the summary is outside the user's viewport and the page does not scroll to bring it into view — warning (the user clicked submit, focus moved to a summary they cannot see — the scroll is what makes "focus moved to the summary" actually visible to sighted users)
- Scroll-into-view implemented as scrolling internally inside a smaller container while the document scroll stays where it was — warning (the page-level scroll is the requirement)
- Smooth scroll used without honouring `prefers-reduced-motion` — note

**Examples**

✓ Correct: User tabs to Save, presses Enter, the form fails validation, the summary appears, and the screen reader announces "3 fields need attention. Customer name is required. Email is invalid. Country is required." Keyboard focus is on the summary; pressing Tab moves to the first link.

✓ Correct: A long form where the summary is placed at the top of the form (per the Rule 3 alternative for unusual layouts). User clicks Save at the bottom of the form; focus moves to the summary and the page scrolls so the summary is visible at the top of the viewport. The user sees the message they were just told about.

✗ Wrong: Failed submit; the summary appears silently and focus stays on the Save button. Keyboard users have to hunt.

✗ Wrong: Failed submit on a long form; focus moves to the summary at the top of the form, but the page doesn't scroll. The user remains looking at the bottom of the form with no visible signal — the focus is on a summary they cannot see.

---

## Rule: Accessibility contract

**Description**

The validation-feedback surfaces have a documented a11y contract that's the floor, not the ceiling. Both the summary and each errored field must carry the right ARIA attributes so screen readers announce the right things at the right times. These attributes are not optional polish — without them, validation is silently broken for assistive-tech users.

**How to Apply**

**On the summary container:**

1. `role="alert"` — already inherited from `Alert variant="error"` per `alert.md`. The Tripletex Banner / Alert components already set this for error variants.
2. `tabindex="-1"` — so the container can receive programmatic focus (per "Focus management" above).
3. `aria-labelledby` pointing at the heading element's `id` — so the screen reader uses the heading as the accessible name.

**On each errored field:**

4. `aria-invalid="true"` — flags the field as invalid for assistive tech.
5. `aria-describedby` pointing at the inline error message's `id` — so the screen reader reads the error along with the field's label and value when the user lands on the field.

**On each summary list entry:**

6. A native `<a href="#field-id">` anchor link, not a `<button>` or `<div>` with click handlers. Anchor links carry the focus-on-activation behaviour for free.

**Colour is not the only signal.** Per [WCAG 1.4.1 — Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html), the Error variant carries text and an icon, never colour alone. The Alert's `--surface-error-*` and `--border-error` tokens are visual reinforcement; the error icon and the message text must be readable independent of colour, and the per-field Error markers must do the same (per `forms/input.md` § "Content type markers"). Users with colour-vision deficits, or anyone reading on a screen with poor colour rendering, depends on the icon-plus-text pair carrying the meaning.

**Violations**

- Summary missing `tabindex="-1"` — error (focus management can't work)
- Summary missing `aria-labelledby` — warning (screen reader announces the alert without naming what it's about)
- Errored field missing `aria-invalid="true"` — error
- Errored field missing `aria-describedby` to its inline error — error
- Summary list entry implemented as `<button>` or `<div>` instead of `<a href="#…">` — warning (works with extra JS but loses native focus-on-activation; prefer the anchor)
- Error state communicated through colour alone (no icon or text reinforcement) — error (WCAG 1.4.1 violation)

**Examples**

✓ Correct: Summary is `<div role="alert" tabindex="-1" aria-labelledby="form-error-heading">` with `<h2 id="form-error-heading">2 fields need attention</h2>`. Each field has `aria-invalid="true"` and `aria-describedby="customer-name-error"`.

✗ Wrong: Summary is `role="alert"` but with no `tabindex` or `aria-labelledby` — the alert announces but isn't focusable and isn't named.

---

## Rule: Submit button stays enabled

**Description**

The submit button (or any form's primary action) remains enabled regardless of whether required fields are filled. Clicking submit on a form with invalid input opens the validation summary; it never silently no-ops, and the button is never greyed out as a validation gate. This aligns Atlas with WCAG guidance and the consensus across Aksel, GOV.UK, Designsystemet, Atlassian, Carbon, and Material: a disabled submit removes the user's path to discover *what's wrong*. The validation surface (summary + inline errors) is what tells the user; the submit button is what triggers the check.

The only legitimate reason to disable the primary action is an in-flight async commit (the action is already running; double-submit must be prevented). This is documented in [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Modal keyboard interactions* and applies equally to non-modal forms.

**How to Apply**

1. Submit is enabled by default.
2. Clicking submit runs validation. If validation fails, render the summary + inline errors per the rules above. **The submit click is never a no-op.**
3. Submit may be disabled **only** during an in-flight async commit (i.e. the action is currently running; spinner state per `buttons.md` § "Action Buttons").
4. On submit success, follow the action-button success state per `buttons.md` and the post-commit feedback pattern (Notification on success, summary remains for repeated failures).

**Violations**

- Submit button disabled because required fields aren't filled — error (validation-gate disabling is forbidden)
- Submit button disabled because an inline field has a current error — error
- Submit click that silently no-ops without surfacing the summary — error
- Submit button disabled during an in-flight async commit (correct case) — not a violation, this is the only legitimate reason

**Examples**

✓ Correct: A "New customer" form with three empty required fields. Submit is enabled. The user clicks Save; validation runs; the summary and inline Error markers appear; focus moves to the summary.

✓ Correct: User clicks Save on a valid form. The button enters its async-commit spinner state; Save is now disabled until the request resolves. A second click during this state is correctly ignored.

✗ Wrong: Form with three empty required fields, Save is greyed out — disabled-as-validation-gate.

✗ Wrong: User clicks Save with an invalid email. The button doesn't respond, no summary appears, the field's inline error stays as it was — silent no-op.

---

## Rule: Live re-validation as the user fixes errors

**Description**

After the summary appears, the user works through the errors by editing the offending fields. As each field's value transitions from invalid to valid, the surfaces update in real time: the field's inline Error marker clears, and the field's corresponding entry in the summary disappears. If the summary's last entry is removed (all errors fixed), the summary itself disappears. If the user submits again with new errors (e.g. a server-side validation rejects a field that passed client-side), the summary re-appears with the new contents.

This live behaviour matters because the alternative — keeping the error visible until the next submit — leaves the user uncertain whether their fix worked. The error lifting on a valid value is the user's confirmation that their input is now acceptable.

The pattern is the **"Reward Early, Punish Late"** model documented by Mihael Konjević: error feedback during typing is appropriate as *re-validation* of an already-flagged field (rewarding the correction the moment it's valid), even though it would be disruptive as *initial* validation of fresh input (punishing the user before they've finished). The two cases look superficially similar but the user's mental state is different — once a field is in error state, the user is aware they made a mistake and wants confirmation it's fixed; before the first submit attempt, the user is still working and doesn't want premature interruption. NN/g's warning against keystroke-by-keystroke validation applies to the second case, not the first; this rule covers the first case only. See [Konjević — Inline validation in forms](https://medium.com/wdstack/inline-validation-in-forms-designing-the-experience-123fb34088ce).

**How to Apply**

1. Each field's inline error clears the moment its current value passes the field's validation rule (typically on `input` or `change` event, not waiting for blur).
2. The summary's entry for that field disappears at the same time.
3. The summary's heading updates if it includes a count ("3 fields need attention" → "2 fields need attention" after one fix).
4. When the last summary entry is removed, the summary container itself disappears.
5. Focus does not move during live re-validation — the user is in the field they're editing; the surfaces update around them.
6. If the user submits again and the field fails again (or new fields fail, e.g. server-side validation), the summary re-renders and focus moves to the summary per "Focus management" above.

**Violations**

- Inline error remains visible after the field's value becomes valid — warning
- Summary entry remains visible after the field's value becomes valid — warning
- Summary heading count fails to update as entries are removed — warning
- Summary remains visible after the last entry is removed — error (the user fixed everything; the surface is stale)
- Live re-validation moves focus during typing — error (disruptive)

**Examples**

✓ Correct: Summary shows "2 fields need attention" with two entries. User clicks the "Email is invalid" link, focuses the email field, types a valid address. The field's Error marker clears; the summary entry disappears; the summary heading updates to "1 field needs attention".

✓ Correct: User fixes the last error. The summary disappears. The user clicks Save; the form submits.

✗ Wrong: User fixes the email, but the inline Error marker stays red until they click Save again — the user doesn't know their fix worked.

---

## Rule: Server / async errors are a separate surface

**Description**

A server-side validation error (the API rejected a field that passed client-side validation, e.g. "username already exists"), an async network failure, or a session-expiry condition is not a validation summary. These have different mental models, different recovery paths, and different lifecycles. Render them separately from client-side validation feedback.

**How to Apply**

Whenever a submit completes its network round trip and the response is anything other than a success, five cases apply — split by *when* the error becomes known relative to the submit cycle:

**Synchronous cases — the error is known during the submit cycle (the user is still on the form):**

1. **In-form server validation error** (the server rejected a specific field's value):
   - Treat the server-rejected field as if it had failed client-side: render its inline Error marker per `forms/input.md`, and add it to the form-level summary Alert (or update the existing summary).
   - The user sees one summary, with a mix of client- and server-side errors, all uniform in appearance.
2. **In-form async/network error** (the request failed for a non-validation reason — 500, network timeout, permission denied):
   - Render an `Alert variant="error"` in the same placement as the validation summary (above the submit button).
   - This is a *different* Alert from the validation summary — different content, different lifecycle (cleared by retry, not by editing fields).
   - If both validation errors and a network error are present at once, the network error appears as a separate Alert above the validation summary (severity-ordered per `alert.md`).
3. **Page-level system error** (auth expired, network down on a non-form page):
   - Render a Banner under the page header per `banner.md`.
   - This is the page-level case the Banner is designed for; not a form-level concern.

**Asynchronous cases — the error arrives *after* the submit looked successful and the user has moved on:**

4. **Asynchronous external-validation result** (the submit was accepted by Tripletex and forwarded to an external system — Skatteetaten, Altinn, the user's bank — and the external system later returns a validation error or rejection). The Tripletex *returmelding* pattern for tax-authority submissions is the canonical case (see [Jeg får ikke hentet returmelding på a-melding](https://hjelp.tripletex.no/hc/no/articles/19212540455825) and adjacent articles):
   - The validation-summary surface from this rule does **not** apply — the user is no longer on the submission form.
   - Surface the error on the **page where the submission lives** (the MVA-melding overview, the salary run detail page, the A-melding history) as an `Alert variant="error"` at the top of that page.
   - Pair with a Notification when the user is logged in.
   - For long delays where the user may not be in-app, additionally send an email — but the in-product surface is the load-bearing one; a Notification alone is transient and easy to miss.
   - The Alert content must include enough context to act on without re-keying the original submission. Link or deep-link to the original submission's edit / re-send view.
5. **Delayed rejection of a previously-accepted submission** (the submit was accepted, the user moved on, and a downstream system later rejected — payment rejected by the bank, regulatory submission rejected after async processing). The Tripletex *betalingen ble avvist* journey is the canonical case (see [Betalingen ble avvist og jeg får feilmelding](https://hjelp.tripletex.no/hc/no/articles/17969182832273)):
   - Same surfacing rules as case 4: in-context page Alert, Notification on next login, optional email.
   - The recovery action is typically distinct from the original submission ("Retry payment", "Fix and resubmit"). **Name the recovery action explicitly** in the message rather than just describing the failure.
   - For payment-class flows, the recovery action may itself trigger step-up auth per the high-stakes rule above.

**Violations**

- Server-side validation error rendered as a Banner inside the form — error (use Alert; this is the same case as the validation-summary container rule)
- Network error and validation summary merged into the same Alert with the same heading — warning (different mental models; separate surfaces)
- Page-level system error rendered as an in-form Alert — warning (use Banner)
- Server-side validation rejection that doesn't update the form-level summary — error (the user has no visible signal that their submit failed)
- Asynchronous external-validation error (returmelding, rejected payment, etc.) surfaced only via a transient Notification, with no in-page Alert on the page where the submission lives — warning (Notifications are transient; the error must persist on the page until acknowledged or resolved)
- Delayed rejection that doesn't link or deep-link to the recovery action — warning (the user shouldn't have to hunt for "where do I retry?")
- Asynchronous error rendered as an inline form-level Alert on a form the user has already navigated away from — error (the form isn't the right surface; surface on the page where the submission now lives)
- Asynchronous error message that doesn't name the recovery action ("Retry", "Fix and resubmit") explicitly — warning

**Examples**

✓ Correct (case 1): User submits a "New customer" form. Client-side validation passes; the server rejects "email" because it's already in use. The form-level Alert appears above Save with one entry: "This email is already registered." The email field shows its inline Error marker.

✓ Correct (case 2): User submits a form. The network times out. An `Alert variant="error"` appears above Save: "Couldn't save — please try again. If the problem persists, contact support." No validation summary because nothing was rejected.

✓ Correct (case 4): User submits an MVA-melding. Tripletex accepts the submission and forwards it to Altinn. Six hours later, Altinn returns a validation error in the *returmelding*. The next time the user opens the MVA-melding overview, an `Alert variant="error"` appears at the top of that page describing the error and linking to the edit-and-resubmit flow. A Notification fires when the user logs in.

✓ Correct (case 5): User submits a salary run via Autopay. The bank accepts the file. Two hours later, one of the payments is rejected by the bank. The salary run detail page surfaces an `Alert variant="error"` listing the rejected payment, with an explicit "Retry payment" link as the named recovery action.

✗ Wrong: Network error rendered as a top-of-page Banner that the user has to scroll to see, while the form's Save button looks idle.

✗ Wrong: A *returmelding* error from Altinn surfaced only as a Notification on next login. Once the user dismisses or navigates past the Notification, they have no record that their submission failed and no path back to fix it.

✗ Wrong: A rejected payment surfaced as a vague Alert on the salary run page that says "There was a problem with one of the payments." — no name of the rejected payment, no recovery action, the user has to call support to find out what happened.

---

## Rule: Modal-hosted form variant

**Description**

When the form lives inside a modal, the form-level summary becomes an inline Alert in the modal body (per [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Errors render inline*). All content rules from the rules above still apply — heading + linked list, identical wording with inline errors, focus management, a11y contract, submit-stays-enabled, live re-validation. The only thing that changes is the visual host: instead of an Alert sitting above the submit button in a page-level form, it's an Alert sitting inside the modal body, placed before the modal's footer button group.

**How to Apply**

When the form lives inside a modal:

1. The summary is an `Alert variant="error"` placed inside the modal body, immediately above the modal's footer button group.
2. Spacing follows the modal-form spacing rule from [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Form fields inside a modal* plus the form-to-button spacing from [`button-placement.md`](button-placement.md). Working position: 24px above the Alert (matching the inter-row vertical spacing inside the modal), 16px between the Alert and the footer button row.
3. **Banners are forbidden inside modals** per `banner.md` and `modal.md`. Use Alert.
4. Focus management: focus moves to the Alert on every failed submit, identical to the page-level case.
5. **Modal re-opens with errors.** When a modal closes mid-flow and re-opens to a state with pre-existing errors (e.g. server returned errors after the modal was dismissed and re-opened, or the user navigated away and back to a draft), focus moves to the summary on open — not to the close button, not to the first field, not to the modal's title. This is the same focus-on-failed-submit rule, applied to the modal-open transition rather than the submit transition. Scroll-into-view applies inside the modal body if the modal's content scrolls — the same page-vs-element-scroll distinction from Rule 6 holds, scoped to the modal's own scroll context.
6. The modal's primary action (Save / Submit) follows the submit-stays-enabled rule; it is never disabled as a validation gate, only during an in-flight async commit.

**Violations**

- Banner used inside a modal to host a validation summary — error (this is the same violation as `banner.md` § "Banner placement", reinforced here)
- Validation summary rendered outside the modal (e.g. as a Notification or a Banner behind the modal) — error
- Modal primary action disabled because required fields aren't filled — error (per the cross-rule with `modal.md`)
- Validation summary in a modal that doesn't follow the same content / a11y / focus rules as the page-level case — warning
- Modal re-opens with pre-existing errors and focus does not move to the summary — warning

**Examples**

✓ Correct: An "Edit customer" modal. User clicks Save with two empty required fields. An `Alert variant="error"` appears inside the modal body, just above the `[Save] [Cancel]` footer group, listing the two missing fields. Focus moves to the Alert; the inline Error markers appear on each field.

✗ Wrong: A "New customer" modal renders the validation summary as a Banner under the page header (behind the modal backdrop), where the user can't see it.

---

## Future Review

The following points are open for future UX discussion and may revise the rules above:

- **Single-field forms (Rule 1).** The current position is to always show the summary, even when only one field is invalid. Aksel and GOV.UK skip the summary in this case on the basis that pointing the user at "the one error" is clearer without a wrapper. The Atlas position differs intentionally — uniformity over Aksel's optimisation — but is worth re-examining once we have usage data on whether the single-field summary feels redundant.
- **Real-time vs. on-blur field validation (Rule 9).** Live re-validation on every keystroke is the working position, mirroring Aksel. An alternative is to only re-validate on blur. Whether typing-time re-validation is worth the implementation cost vs. blur-only re-validation is open.
- **Top-of-form vs. above-submit placement (Rule 3).** GOV.UK places the summary at the top of the page; Aksel and Designsystemet place it above the submit. The Atlas position is above-submit, with top-of-form as a tolerated alternative for unusual layouts. Whether this should be tightened to "always above submit" or loosened to "team's choice" is open.
- **Dedicated `ErrorSummary` / form-error component (Astro team — for future consideration).** This rule currently composes from `Alert`, which works but leaves anatomy choices in each implementer's hands. At some point Astro should consider building a dedicated form-error component (working name: `ErrorSummary`) along the lines of Aksel's and GOV.UK's components — a single React/Figma primitive that bakes in the heading + linked-list anatomy, the `role="alert"` + `tabindex="-1"` + `aria-labelledby` contract, the focus-on-failed-submit behaviour, and the anchor-link-to-field semantics. Once that component exists, the rules in this file can be **tightened** considerably: the structural rules (anatomy, a11y attributes, focus management, list-entry-as-anchor-link) collapse into "use the component", and this file becomes shorter and more about *when and where* than *what to compose*. Aksel and GOV.UK ship a dedicated component; Atlassian, Carbon, and Designsystemet do not — the Aksel/GOV.UK side of that split is closer to the level of rigour Atlas wants. Tracking under `TODO.md` § "Dedicated `ErrorSummary` component (Astro)".

---

## Out of Scope of This File

- **Field-level Error marker visual contract** — see [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md) *Content type markers*. This file references that contract but does not own it.
- **Alert anatomy details** — see [`../design-rules/components/alert.md`](../design-rules/components/alert.md). This file specifies the contents of the Alert (heading + linked list); the visual contract (icon size, padding, dismissibility behaviour) lives in the component rule.
- **Modal-specific spacing** — see [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Form fields inside a modal* and *Errors render inline*.
- **Wording / copy** — owned by Text Vault. Atlas specifies structure only.
- **Success states** — confirmation feedback after a successful submit lives in [`../design-rules/components/notification.md`](../design-rules/components/notification.md) and [`../design-rules/components/buttons.md`](../design-rules/components/buttons.md) (*Action button success state*). This file covers failed submits only.
- **Field-level dependent validation** (*"if A is X then B must be Y"*) — the form-level surface treats each rejected field uniformly; the cross-field rule that produced the rejection is documented at the field level.

---

## Related Rules

- [`../design-rules/components/alert.md`](../design-rules/components/alert.md) — the Alert component used as the summary container; placement, variants, dismissibility.
- [`../design-rules/components/banner.md`](../design-rules/components/banner.md) — page-level counterpart to Alert; transitional exception for in-form Banner usage during migration.
- [`../design-rules/components/forms/input.md`](../design-rules/components/forms/input.md) *Content type markers* — the field-level Error marker contract.
- [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Errors render inline* — modal-hosted form variant.
- [`../design-rules/components/modal.md`](../design-rules/components/modal.md) *Modal keyboard interactions* — submit-never-disabled-as-validation-gate cross-rule.
- [`../design-rules/components/buttons.md`](../design-rules/components/buttons.md) *Action Buttons* — async commit spinner state; the only legitimate reason to disable submit.
- [`button-placement.md`](button-placement.md) *Form button placement* — form-to-button spacing.
- [`modal-usage.md`](modal-usage.md) *When to use a modal vs alternatives* — confirmation that validation feedback is *not* a modal use case.
- [`../design-rules/foundations/colors.md`](../design-rules/foundations/colors.md) — surface and border tokens for the Error Alert variant.
- [Text Vault](https://cdn.tripletex.no/text-vault/index.html) — canonical copy for validation wording.

---

## Figma

Canonical Figma examples for this pattern are not yet in the Atlas Library. See `TODO.md` § "Figma examples for the validation-feedback pattern" for the work item.
