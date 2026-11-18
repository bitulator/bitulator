# ₿ Bitulator — BTC/SATs Calculator

A free Bitcoin calculator that runs entirely in the browser. Convert dollars to sats at the live BTC price, follow the chart, plan a DCA, and explore Bitcoin's network — no sign-up, no tracking, no accounts.

**Live site:** https://bitulator.xyz

## What it does

18 cards, all computing live in your browser:

- **Calculator** — USD ⇄ sats converter at the live price (21 fiat currencies, SAT/BTC switch, custom price entry)
- **Live BTC chart** — minute to all-time ranges, 200-week moving average, log view, fullscreen
- **Historical prices** — what BTC cost on any date back to July 2015
- **DCA calculator** — dollar-cost-average simulator, with a DCA vs. lump-sum comparison
- **Bitcoin network** — block height, halving countdown, current send fees (incl. the dollar cost of a typical send)
- **Fear & Greed** — the daily sentiment index on a gauge
- **Mayer Multiple & ATH** — price vs. its 200-day average, all-time high and distance from it
- **What $100 did** — cash vs. Bitcoin over time, inflation-adjusted
- **Stack goal** and **My stack at a future price** — plan and project a stack
- **Moscow Time** — sats per dollar, Blockclock-style
- **Bitcoin supply** — mined total, % of 21M, remaining supply, current inflation rate
- **Difficulty adjustment** — blocks to the next retarget, epoch progress, estimated change
- **Your hour in sats** — an hourly wage expressed in sats, now and in past years
- **What 1 BTC buys** — gold, silver, oil and everyday goods priced against one bitcoin
- **House down payment** — how much BTC you'd need, and whether a monthly stacking plan gets there
- **Bitcoin-only YouTube** — five Bitcoin-only channels with an in-page player (Pleb Underground, BTC Sessions, Bram Kanstein, The Jack Mallers Show, Canadian Bitcoiners)
- **Bitcoin resources** — the white paper and classic learning links

Cards can be reordered (drag or ↑/↓ buttons), switched between stacked and tile layouts, jumped to from the nav header, and shared to X with their live figures. Your layout is remembered on your device.

## Run it yourself

**Option 1 — standalone page.** Open `index.html` in a browser, or host that single file anywhere (GitHub Pages, Netlify, Cloudflare Pages, any web server). It is the complete calculator: markup, styles and scripts in one file. Note: opening it as a local file works in a desktop browser; on a phone, serve it over http(s) — some mobile file viewers block its data feeds.

**Option 2 — Carrd.** The live site runs on Carrd, which caps each Embed element at ~16,384 characters, so the code ships as 13 parts in the `carrd/` folder:

| File | Goes in Carrd as |
| --- | --- |
| `part-1-css.html` | Embed → Hidden → Head (meta tags, CSS, structured data) |
| `part-2-html.html` | Embed → Inline (header + all card markup) |
| `part-3-js.html` … `part-13-js11.html` | Embed → Hidden → Body End, in order |

`index.html` is assembled from exactly these parts, so both routes run identical code.

## Data sources

All data comes from free public APIs, fetched directly by the browser — no API keys, no backend:

- Prices: Coinbase (primary), CoinGecko and Kraken (fallbacks)
- Network, fees, difficulty: mempool.space (Blockstream fallback)
- Fear & Greed: Alternative.me
- Gold/silver (in "What 1 BTC buys"): CoinGecko (PAX Gold / Kinesis Silver)
- Inflation adjustment: US CPI-U (BLS)

## Privacy

No analytics, no cookies set by the calculator, no accounts. The only thing stored is your card layout, in your own browser's local storage.

## License

MIT — see `LICENSE`. Use it, fork it, learn from it.

---

By **[Unit of A Count](https://x.com/countbitcoin)** · Donations: [coinos.io/bitulator](https://coinos.io/bitulator/receive)
