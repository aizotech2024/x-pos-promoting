# x-pos-promoting

Marketing materials for **X-POS** by AizoTech — POS, multi-branch stock, online store, staff & payroll for Sri Lankan businesses. Everything is in English and Sinhala.

| Folder | What's inside |
|---|---|
| `site/` | Landing page — `index.html` (English), `si/index.html` (සිංහල). Static HTML + one CSS file, no build step. |
| `deck/` | 10-slide sales deck. `x-pos-deck.html` (press **L** or add `?lang=si` for Sinhala) + ready PDFs `X-POS-Deck-EN.pdf` / `-SI.pdf` |
| `ads/` | `facebook-campaign.md` — ad sets, targeting, budgets, EN + SI copy, WhatsApp greeting. `creatives/` — 1080×1080 ad images |
| `brochure/` | One-page A4 brochure — PDFs to print, PNGs to send on WhatsApp, `brochure.html` source |

The PDFs and PNGs are rendered from the HTML files. After filling the placeholders, re-export: open the HTML in Chrome → Print → Save as PDF (background graphics on).

## Before going live — fill the placeholders

Search the repo for `[` and replace:

- `[PHONE]`, `[EMAIL]`, `[WEBSITE]`, `[WHATSAPP_NUMBER]` — contact details (WhatsApp in international format, no `+`, e.g. `9477xxxxxxx`)
- `[LANDING_URL]` — where the site is hosted (used in the ad copy)
- `[LKR —]` / `[රු. —]` — plan prices

```bash
grep -rnE '\[(PHONE|EMAIL|WEBSITE|WHATSAPP_NUMBER|LANDING_URL|LKR|රු)' --include='*.html' --include='*.md' .
```

## Preview the site locally

```bash
cd site && python3 -m http.server 8080
# open http://localhost:8080  and  http://localhost:8080/si/
```

## Publish the site

Any static host works — point it at the `site/` folder:

- **Cloudflare Pages / Netlify** — connect this repo, build command: *none*, output directory: `site`
- **GitHub Pages** — Pages only serves from `/` or `/docs`, so rename `site/` to `docs/`, then Settings → Pages → branch `main`, folder `/docs`. (Pages on a private repo needs a paid GitHub plan.)

## Feature claims

Every feature listed is taken from the X-POS code (`aizotech-x-pos`, `woodx` branch, Nov 2026). If a module is removed or renamed, update the copy here too.
