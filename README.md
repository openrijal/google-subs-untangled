# Google Subscriptions, Untangled 🧾

**Live site: [openrijal.github.io/google-subs-untangled](https://openrijal.github.io/google-subs-untangled/)**

An interactive, single-page optimizer for Google's overlapping consumer subscriptions — Google One, the Google AI plans (Plus / Pro / Ultra $100 / Ultra $200), YouTube Premium / Lite / Music / TV, Google Home Premium (formerly Nest Aware), Google Health Premium (formerly Fitbit Premium), Google Fi, and more.

Answer seven questions and get the **cheapest combination of plans** that covers what you actually use — with links to every official sign-up page, the double-pay traps to avoid, and the purchase-channel gotchas.

## Features

- **Plan optimizer** — a swipeable seven-question quiz with a live "receipt" that prices every anchor strategy (no bundle / AI Plus / AI Pro / AI Ultra $100 / $200) plus the add-ons needed to fill the gaps, and picks the lowest monthly total.
- **Auto-include cascade** — pick an AI plan and everything it bundles (storage, YouTube, Home, Health) is auto-selected and badged *included*; downgrade and your original answers come back.
- **Monthly ↔ annual toggle** — shows the monthly price struck through next to the effective annual price (~15–17% off), only on plans Google actually sells annually, with the no-pro-rata-refund caveat.
- **Bundle map & full price catalog** — every subscription, its sharing rules (family limits, same-address requirements, manager-only perks), and every overlap.
- **Ten overpay traps** — real redundancies in Google's own plan structure, each with a fix and an official "read more" link.
- **Where-you-subscribe guide** — web vs. iOS App Store (~30% markup) vs. Google Play billing vs. carrier billing, and which one to use.
- Material-3-flavored design, light theme by default with a dark-mode toggle, fully responsive (bottom navigation + floating total on mobile).

## Why this exists

Google's subscription lineup overlaps in non-obvious ways:

- **Google AI Pro ($19.99/mo)** includes 5 TB storage, YouTube Premium Lite, Google Home Premium Standard, and Google Health Premium — pieces that cost ~$39/mo bought separately.
- Every YouTube perk bundled into Google One / AI plans is **manager-only**; family ad-free YouTube exists only as YouTube Premium Family ($26.99/mo, one household address, electronically checked every 30 days).
- Annual billing (web-only) runs ~15–17% cheaper; iOS App Store billing runs ~$5/mo *more*.
- AI plan members get 10% back in Google Store credit on hardware (expires after 365 days).

## Tech

One self-contained `index.html` — vanilla JS SPA with hash routing. No framework, no build step, no dependencies beyond Google Fonts. Deployed straight to GitHub Pages from the repo root.

Run locally: open `index.html` in a browser, or `python3 -m http.server` and visit `localhost:8000`.

## Data freshness & accuracy

Prices are **US-only**, compiled from Google's official plan and support pages on **July 5, 2026** (post-June-2026 YouTube price increase; post-I/O-2026 AI plan restructure). Items badged "check" in the UI came from a single source. Storage on AI plans varies by membership variant (AI Plus 400 GB/2 TB, AI Pro 5/10 TB, Ultra 20/30 TB). Prices change — always confirm on the official page before subscribing.

**Contributing a correction:** all optimizer pricing lives in the `ANCHORS`, `STORAGE_TIERS`, and inline constants near the bottom of `index.html`; the display tables are in the Plans view markup. PRs welcome.

## Disclaimer

Not affiliated with, endorsed by, or sponsored by Google LLC. Google One, Gemini, YouTube, Nest, Fitbit, Google Fi, and related marks are trademarks of Google LLC, used here only to identify the products being compared. This is community-maintained information, not financial advice.

## License

[MIT](LICENSE)
