# ecoround-apex-redirect

Tiny GitHub Pages site whose only job is to redirect the apex domain
**ecoroundholsters.com** → **https://www.ecoroundholsters.com** (which is
hosted on Railway).

Why this exists: Railway serves custom domains via CNAME only, and a root/apex
domain can't be a CNAME. GitHub Pages provides stable apex IPs, so the bare
domain points here and this page bounces visitors to the `www` site,
preserving the path and query string.

- `index.html` / `404.html` — client-side redirect to the www site
- `CNAME` — tells GitHub Pages the custom domain is `ecoroundholsters.com`

DNS (in Wix): apex `@` A records point to GitHub Pages
(185.199.108.153–185.199.111.153); `www` CNAME stays pointed at Railway.
