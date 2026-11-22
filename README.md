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
