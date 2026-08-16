# keycapgaming.com

Static site for KeyCap Games. Two pages, no build step.

- `index.html` — landing page, support email, link to the policy
- `privacy.html` — privacy policy for SpeedyKeys
- `CNAME` — tells GitHub Pages to serve this at keycapgaming.com

## Publishing

1. Create a new **public** GitHub repo (e.g. `keycapgaming-site`) and push these files to `main`.
2. Repo → Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Under Settings → Pages → Custom domain, enter `keycapgaming.com` and save.
4. At your registrar, point DNS at GitHub Pages:
   - `A` records for the apex `@` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - `CNAME` for `www` → `<your-github-username>.github.io`
   - If using Cloudflare, set these records to **DNS only** (grey cloud) so GitHub can issue the certificate.
5. Wait for "Enforce HTTPS" to become available in Settings → Pages, then tick it.

## URLs the stores will ask for

- Privacy policy: `https://keycapgaming.com/privacy.html`
- Support / marketing: `https://keycapgaming.com`
