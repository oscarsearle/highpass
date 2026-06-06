# HIGHPASS — Shopify Theme Build

You are building a custom Shopify theme for HIGHPASS, a premium cycling accessories brand from Wanaka, New Zealand. The theme is forked from Shopify's Dawn theme and written in Liquid.

## The Brand

HIGHPASS sells premium cycling accessories DTC via highpass.nz. Launch product: HIGHPASS FLOW 1 — a portable electric bike pump. The brand is quiet, technical, and confident. It does not explain itself twice.

## Design Philosophy

Inspired by Thuono Audio (thuonoaudio.com/en/products/th400) — a premium Italian hi-fi brand. The design approach:
- Product is the singular focal point
- What is absent conveys confidence
- Technical precision language
- No clutter, no urgency, no decoration

This is NOT a generic Shopify store. It must feel like a premium DTC brand, not a dropship site.

## Colour System

| Token | Hex | Use |
|---|---|---|
| --color-background | #11120D | Primary background (Smoky Black) |
| --color-foreground | #FFFBF4 | Primary text (Floral White) |
| --color-secondary | #565449 | Supporting UI, borders (Olive Drab) |
| --color-accent | #D8CFBC | Hover states, tags (Bone) |

Dark background throughout. No white backgrounds except checkout (Shopify controlled).

## Typography

- Headings: Monument Extended Bold — all caps, letter-spacing: -0.02em
- Body: Inter Regular — sentence case, line-height: 1.6, min 15px
- Load via Google Fonts: Inter. Monument Extended via @font-face from assets/
- No italics. No mixing weights in one line.

## Site Structure

Pages to build:
1. Homepage — hero + product feature strip + product section + social proof
2. Product page (FLOW 1) — gallery left, specs right, expandable feature sections below
3. FAQ page — branded, minimal, accordion style
4. Shipping/Refund policy pages — clean, minimal
5. Contact page — single email link, no form clutter

## Product Page Layout (Priority — build this first)

Mirror the Thuono Audio TH400 product page structure exactly, adapted for HIGHPASS:

### Above fold (two-column layout):
- LEFT: Full-height image gallery. Large primary image. Thumbnail rail below. Click thumbnails to switch main image. Arrow navigation on mobile.
- RIGHT: Product name (HIGHPASS FLOW 1), short technical description paragraph, specs table (two columns: spec name left, value right), Add to Cart button (full width, --color-foreground bg, --color-background text)

### Below fold:
- Expandable feature sections (click + to expand, like Thuono). Each section has:
  - Section title (left, all caps)
  - + / - toggle (right)
  - Body: description paragraph left, technical illustration/image right
  - Divider line between sections

Feature sections for FLOW 1:
1. "PRECISION INFLATION: AUTO-STOP TECHNOLOGY" — explains the auto-stop at preset PSI
2. "120 PSI BRUSHLESS MOTOR" — explains the motor, inflation speed, performance
3. "USB-C RECHARGEABLE: 20+ INFLATIONS PER CHARGE" — battery, charging spec
4. "UNIVERSAL VALVE COMPATIBILITY" — Schrader and Presta, how to switch

## Specs Table Content (FLOW 1)

| Spec | Value |
|---|---|
| Max Pressure | 120 PSI |
| Motor | Brushless DC |
| Battery | USB-C rechargeable |
| Inflations per charge | 20+ |
| Valve types | Schrader, Presta |
| Auto-stop | Yes — preset PSI |
| Weight | TBC |
| Dimensions | TBC |
| Price | $99.99 NZD |

## Navigation

Minimal nav: HIGHPASS wordmark left (links to homepage), SHOP right (links to product). Nothing else. Nav background matches page background. On scroll: nav stays fixed at top, subtle border-bottom appears.

## Rules

- Never use em dashes (—) in copy. Use colons or rewrite.
- No gradients anywhere.
- No exclamation marks in any copy.
- No fake urgency (countdown timers, "only 3 left", etc.)
- All copy in NZ English.
- Mobile-first. Most traffic comes on mobile. Test every section at 390px width.
- Modify Dawn Liquid files directly — do not create workarounds or inline styles when a proper Liquid/CSS solution exists.
- Use CSS custom properties (variables) for all colours — never hardcode hex values in CSS.

## Reference

Design reference: thuonoaudio.com/en/products/th400
Brand guidelines: ../ops/brand-guidelines.md
Store PRD: ../ops/store-prd.md
