---
name: fish-flight-brand
description: Apply Fish Flight Entertainment's brand — colors, typography, logo usage, and voice/tone — when writing copy, building UI, or choosing which logo file to use for Fish Flight Entertainment. Use whenever a task mentions Fish Flight Entertainment, its brand kit, or asks for on-brand marketing/UI copy or assets for it.
---

# Fish Flight Entertainment Brand

Reference for producing on-brand output — copy, UI, decks, social assets — for Fish Flight Entertainment. Exact machine-readable values live in `design-tokens.json` in this repo; read it when you need precise hex/rgb values or the full logo file list rather than retyping numbers from memory.

## Who they are
A boutique Vancouver game studio founded by Paul Furminger and Sabrina Furminger, with roots across TV, film, and gaming, now focused on gaming and interactive entertainment. Parent company of YVR Screen Scene (a digital magazine/podcast on the Vancouver film & TV industry).

**Name origin**: the legendary 5am YVR→LAX "Fish Flight" that once carried fresh seafood to LA restaurants and, in the analog era of Hollywood North, film reels of VFX/animation footage for same-day studio feedback — the industry's lifeline before digital delivery. Use this story as the go-to brand anchor when copy needs texture (about pages, pitch decks, investor intros) — don't over-explain it in short-form copy (nav labels, buttons, social captions).

## Voice & tone
Pioneering, independent, boutique, craft-focused, adventurous, community-rooted. Write like industry veterans who chose passion over routine: confident, a little irreverent, proud of Vancouver film-industry roots, comfortable describing ambitious bets in plain, vivid language — e.g. "not afraid to jump off the cliff and build our wings on the way down."

Avoid: corporate-speak, hedging, generic "innovative synergy" language, and anything that undersells the risk-taking self-image.

## Color
| Name | Hex | Usage |
|---|---|---|
| Fish Flight Teal | `#125C77` | Primary accent — the 'ENTERTAINMENT' wordmark, the FF monogram, links, small accent details |
| Fish Flight Black | `#000000` | Primary background / primary text-on-light. Most lockups are built for black. |
| Fish Flight White | `#FFFFFF` | Primary text-on-dark / secondary background |

Default surface is black with white text and teal accents — not a generic light theme. Full detail in `design-tokens.json` → `color`.

## Typography
- **Headline**: bold, condensed/block uppercase face (e.g. Archivo Black), echoing the "FISH FLIGHT" wordmark. Headlines and hero statements only.
- **Subhead/label**: a lighter weight, letter-spaced uppercase (e.g. Jost 500, `letter-spacing: 0.12em`), echoing "ENTERTAINMENT" under the wordmark. Section labels, nav, eyebrows.
- **Body**: the same companion face at regular weight for long-form copy.

Full detail in `design-tokens.json` → `typography`.

## Logo usage
- Prefer the transparent-background PNG lockups (`Fishflight_logo_ALPHA.png` for dark surfaces, `Fishflight_logo_ALPHA_Black_Text.png` for light surfaces) over the flattened JPGs when compositing onto a colored or photographic background.
- Use the horizontal lockup (`Fishflight_logo_horizontal.jpg`) only where vertical space is constrained (e.g. a page header); the stacked lockup is the default.
- Use the icon-only monogram (`Fishflight_logo_icon_alpha.png` / `_BW.png`, or the pre-cropped `_16x16`/`_32x32`/`_48x48`/`_128x128` PNGs) for square/small placements — favicons, avatars, app icons — never the full wordmark below ~120px wide.
- Don't recolor the monogram or wordmark, don't stretch/skew the lockup, and don't place the color logo on a background close to `#125C77` (insufficient contrast).
- Full file list with variant, intended background, and minimum width is in `design-tokens.json` → `logo`.

## When generating something on-brand
1. Pull exact colors/fonts from `design-tokens.json` rather than approximating.
2. Default to black background / white text / teal accents unless the surface genuinely requires a light-background variant — then use one of the light-background logo files above.
3. Keep copy in the voice described above; lean on the Fish Flight origin story for longer-form "about" content.
4. Pick the logo file by matching `background` and `minWidthPx` in the tokens file to the actual placement.
