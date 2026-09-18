# Current live site — extracted tokens (2026-09-18)

Source: `https://www.myjewellerystory.com.au/` static CSS (`WiseRobot/Base` theme: Bootstrap 3 + Lato).
Counts are occurrences across `base-theme.css`, `inline.css`, `home.css`. Bootstrap defaults are marked; they are
not brand.

## Colour

| Hex | Role seen | Keep? |
|---|---|---|
| `#ffffff` | page, cards | keep |
| `#323232` | headings, footer background | keep — the "black" |
| `#333333` / `#555555` / `#777777` / `#9d9d9d` | body text, muted (Bootstrap greys) | keep as a grey ramp |
| `#f8f5f0` | section border/underline, warm off-white | keep — brand cream |
| `#eadfcd` | panel background + border, warm beige | keep — brand accent |
| `#fdf0d5` | notice/callout background (with `#1979c3` text) | keep as a soft highlight |
| `#337ab7` / `#286090` | Bootstrap link/button blue | drop |
| `#006bb4` / `#1979c3` | Magento Luma blue (links, notice text) | drop |
| `#dddddd` / `#cccccc` / `#eeeeee` / `#e7e7e7` | borders, dividers | replace with one border token |
| `#a94442` `#3c763d` `#8a6d3b` `#31708f` | Bootstrap alert colours | replace with success/error tokens |

## Type

- Body: `Lato, sans-serif` (Google Fonts, 300/300i/400/700). Fallback stack on live: `"Helvetica Neue", Helvetica, Arial`.
- Icons: `Glyphicons Halflings`, `mjsIcons` (icon font) — replace with Hyvä's inline SVG icons.
- No display face in use; headings are Lato at weight 300/400.

## Logo

- `logo-myjs.jpg` 314×136 — wordmark "MYJS" + "My Jewellery Story", black on white.
- `logo-header-checkout.png` 619×91 — "MYJS | Secure Checkout" header variant.
- Favicon: `/media/favicon/default/favicon.ico`.

## Where these land in Hyvä

`app/design/frontend/Mjs/retail/web/tailwind/hyva.config.json` → `tokens.values` (currently placeholder oklch
primary/secondary) — DTCG `$value`/`$type` format is accepted via `tokens.src`; `hyva-tokens` generates
`generated/hyva-tokens.css` under `@theme` (Tailwind 4). Fonts via `tailwind-source.css`.
