# Claude Design handover — MJS retail storefront (Hyvä)

What David uploads to claude.ai/design, and the brief to paste. Prepared 2026-09-18.
Output comes back as a handoff bundle → TASK to the website seat → `Mjs/retail` theme.

## 1. Upload as the design system source (Settings → Design systems → new)

| Item | Where | Why |
|---|---|---|
| `logo-myjs.jpg`, `logo-header-checkout.png` (this dir) | live site | the wordmark: thin geometric black caps "MYJS", "My Jewellery Story" beneath |
| `tokens-current-site.md` (this dir) | extracted from live CSS | current palette + type, so it starts from real values |
| GitHub repo `https://github.com/hyva-themes/magento2-default-theme` | import from GitHub | Hyvä's component vocabulary — header, minicart, product card, PLP filters, PDP gallery/options, cart. Design *with* these, not against them |
| 8–10 product photos (rings, earrings, necklaces; white background + lifestyle) | media / live site | mockups look like our store, not stock |
| Screenshots of the live site: home, `/rings/rings-all.html`, one PDP, cart — desktop + phone | David, browser | "the feel to keep"; also what to leave behind |

## 2. Brief to paste into the design-system chat

> Build a design system for **My Jewellery Story (MYJS)**, an Australian fine-jewellery retailer (rings, earrings,
> necklaces, bracelets, bridal, lab-grown diamonds, personalised pieces). Customers are retail buyers on mobile
> first. The storefront is **Magento 2 with the Hyvä theme: Tailwind CSS utility classes, Alpine.js, server-rendered
> HTML** — no React. Use the imported `hyva-themes/magento2-default-theme` repo as the component vocabulary and keep
> its structure; restyle, don't reinvent.
>
> Brand: the MYJS wordmark (attached), black on white, thin geometric sans. Keep the current feel — clean, white,
> warm cream accents (`#f8f5f0`, `#eadfcd`, `#fdf0d5`), near-black text (`#323232`), Lato-style humanist sans —
> but drop the Bootstrap blues (`#337ab7`, `#006bb4`, `#1979c3`); pick one accent that reads "fine jewellery" and
> use it sparingly for primary actions. Photography carries the page; UI stays quiet.
>
> Deliver: colour tokens (primary, secondary, on-primary, on-secondary, surface, text, border, success/error),
> type scale (one display face for headings if you propose one, body = Lato or a close open-source stand-in),
> spacing/radius, and components: button (primary/secondary/ghost), product card (image, name, price, colour
> swatches, "add to cart"), price (regular/sale), swatch group (colour + size), input/select, badge, minicart row,
> breadcrumb, accordion (PDP details/shipping), toast. Also export the colour + type tokens as a **DTCG JSON**
> (`$value` / `$type`) so they drop straight into Hyvä's `hyva.config.json`.

## 3. Screens to design (wireframe first, then polish) — mobile + desktop

1. Product card + PLP (`/rings/rings-all.html`): filters, sort, 2-up mobile / 4-up desktop grid, quick colour swatches.
2. PDP: gallery, configurable options (colour, size, engraving where applicable), price, Afterpay line, add-to-cart
   sticky on mobile, details/shipping/returns accordion, related.
3. Home: hero, category tiles, featured collection, trust strip (AU-made, returns, secure).
4. Cart + minicart.
5. Header (nav, search, account, minicart) and footer.

**Do not design checkout.** It is Hyvä Checkout, which inherits these tokens through the theme.

## 4. Handoff back

Export → "send to local coding agent"; the website desk turns the bundle into the `Mjs/retail` theme.
