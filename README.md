# Business-

Lead database and private demo websites for local businesses.

## Layout

- `lead.json` - one object per business (array).
- `sites/<slug>/` - the demo website for that business (`index.html`, `images/`, ...).
- `slug` in `lead.json` = the folder name under `sites/`.

## lead.json entry

```json
{
  "slug": "example-plumbing-bristol",
  "business": "",
  "trade": "",
  "town": "",
  "region": "",
  "country": "",
  "phone": "",
  "rating": null,
  "review_count": null,
  "hours": "",
  "maps_link": "",
  "website_status": "none | facebook_only | broken | has_website",
  "website_status_note": "what happens when the existing site is opened",
  "services": [],
  "reviews": [
    { "name": "", "text": "" },
    { "name": "", "text": "" },
    { "name": "", "text": "" }
  ],
  "demo_path": "sites/<slug>/",
  "status": "draft | confirmed | sent | skipped"
}
```

Unknown values are `null` (or empty), never guessed. Reviews are verbatim.

## Hosting (Vercel)

The repo is connected to Vercel as a static site (no build step). Every push to `main` deploys automatically.

- Demo URL: `https://<vercel-project>.vercel.app/<slug>`, e.g. `/corvo-lincoln`
- `lead.json` and this README are not deployed (`.vercelignore`), so phone numbers and notes stay private.
- All pages send `noindex` and `robots.txt` blocks crawlers, so demos stay out of Google.
