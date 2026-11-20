# PR Labs — marketing site

The public home of PR Labs, makers of tools for working alongside AI agents, including Bumpkit and Kaarigar.

## Stack

Deliberately none. Plain HTML and one CSS file; no build step, no framework, no JavaScript.
Fonts (Cormorant Garamond, EB Garamond) load from Google Fonts.

```
index.html    the page
styles.css    all styling; design tokens at the top under :root
favicon.svg
```

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploy

Any static host works (Cloudflare Pages, Netlify, GitHub Pages, S3). Publish the repo root as-is.

## Adding a product

Copy an `<article class="feature">` block in the Products section of `index.html` and bump the numeral.

## Contact form

The Correspondence section posts to **Netlify Forms** (no email address appears on the site).
Netlify detects the `contact` form on deploy; then, in the Netlify dashboard, go to
**Site configuration → Notifications → Emails and webhooks → Form submission notifications**
and add the inbox that should receive messages. Spam is filtered by Netlify plus a honeypot field.
After submitting, visitors land on `thanks.html`. The form only works on the deployed Netlify site,
not in local preview.
