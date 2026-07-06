# Google Subscriptions, Untangled

An interactive, single-page optimizer for Google's overlapping consumer subscriptions — Google One, the Google AI plans (Plus / Pro / Ultra), YouTube Premium / Lite / Music / TV, Google Home Premium (Nest Aware), Google Health Premium (Fitbit), Google Fi, and more.

Answer six questions and get the **cheapest combination of plans** that covers what you actually use, with links to every official sign-up page, the double-pay traps to avoid, and the purchase-channel gotchas (annual-vs-monthly, web-vs-App-Store pricing, Play billing quirks).

**Live site:** enable GitHub Pages for this repo (Settings → Pages → Deploy from branch → `main` / root) and it just works — there is no build step.

## Why

Google's subscription lineup overlaps in non-obvious ways:

- **Google AI Pro ($19.99/mo)** includes 5 TB storage, YouTube Premium Lite, Google Home Premium Standard, and Google Health Premium — pieces that cost ~$39/mo bought separately.
- Every YouTube perk bundled into Google One / AI plans is **manager-only**; family ad-free YouTube exists only as YouTube Premium Family ($26.99/mo, one household address, checked every 30 days).
- Annual billing (web-only) runs ~15–17% cheaper; iOS App Store billing runs ~30% *more*.
- AI Plus/Pro/Ultra members get 10% back in Google Store credit on hardware.

The optimizer prices every "anchor" strategy plus the add-ons needed to fill the gaps, and picks the lowest total.

## Tech

- One self-contained `index.html` — vanilla JS SPA (hash routing), no framework, no build, no dependencies beyond Google Fonts.
- Material-3-flavored design: light theme by default, dark mode toggle (persisted in `localStorage`), responsive with a bottom nav on mobile.

## Data freshness & accuracy

Prices are **US-only**, hand-compiled from Google's official plan and support pages on **July 5, 2026** (post-June-2026 YouTube price increase). Items badged "check" in the UI came from a single source. Storage on AI plans varies by membership variant (AI Plus 400 GB/2 TB, AI Pro 5/10 TB, Ultra 20/30 TB). Prices change; always confirm on the official page before subscribing. Corrections welcome — all pricing lives in the `ANCHORS`, `STORAGE_TIERS`, and inline constants near the bottom of `index.html`, plus the two tables in the Plans view.

## Disclaimer

Not affiliated with, endorsed by, or sponsored by Google LLC. Google One, Gemini, YouTube, Nest, Fitbit, Google Fi, and related marks are trademarks of Google LLC, used here only to identify the products being compared.

## License

[MIT](LICENSE)
