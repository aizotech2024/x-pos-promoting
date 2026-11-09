# x-pos-promoting

Marketing materials for **X-POS** by AizoTech — POS, multi-branch stock, online store, staff & payroll for Sri Lankan businesses. Everything is in English and Sinhala.

| Folder | What's inside |
|---|---|
| `site/` | Landing page — `index.html` (English), `si/index.html` (සිංහල). Static HTML + one CSS file, no build step. |
| `deck/` | Sales pitch deck (English + Sinhala) |
| `ads/` | Facebook / Instagram ad campaign — audiences, ad copy, budget plan |
| `brochure/` | One-page brochure (print + WhatsApp) |

## Before going live — fill the placeholders

Search the repo for `[` and replace:

- `[PHONE]`, `[EMAIL]`, `[WHATSAPP_NUMBER]` — contact details (WhatsApp in international format, no `+`, e.g. `9477xxxxxxx`)
- `[LKR —]` / `[රු. —]` — plan prices

```bash
grep -rn '\[PHONE\]\|\[EMAIL\]\|\[WHATSAPP_NUMBER\]\|\[LKR\|\[රු' .
```

## Preview the site locally

```bash
cd site && python3 -m http.server 8080
# open http://localhost:8080  and  http://localhost:8080/si/
```

## Publish the site

Any static host works — point it at the `site/` folder:

- **Cloudflare Pages / Netlify** — connect this repo, build command: *none*, output directory: `site`
- **GitHub Pages** — Settings → Pages → deploy from branch `main`, folder `/site` is not offered, so either move `site/` to `docs/` or use a Pages Actions workflow

## Feature claims

Every feature listed is taken from the X-POS code (`aizotech-x-pos`, `woodx` branch, Nov 2026). If a module is removed or renamed, update the copy here too.
