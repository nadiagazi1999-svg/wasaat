# WASAAT website — publish-ready

This is a static website for **https://wasaat.net**.

## Fastest free publishing route: GitHub Pages

1. Create a free GitHub account if needed.
2. Create a **public** repository named `wasaat-site`.
3. Upload everything from this folder to the repository root:
   - `index.html`
   - `styles.css`
   - `script.js`
   - `assets/`
   - `CNAME`
   - `.nojekyll`
4. In the repository, open **Settings → Pages**.
5. Under "Build and deployment", choose **Deploy from a branch**.
6. Select branch `main` and folder `/ (root)`, then Save.
7. Under **Custom domain**, enter: `wasaat.net`

## Point the domain to GitHub Pages

At the DNS manager for the company where `wasaat.net` was purchased, remove any conflicting existing A/AAAA records for `@` and add these four A records:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

For `www`, add:

| Type | Name | Value |
|---|---|---|
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

Then return to **GitHub → Settings → Pages**, wait for DNS verification, and enable **Enforce HTTPS** when available.

DNS changes can take time to propagate.

## Before launch

The current website does not invent an email address. When WASAAT has an official email, replace the "Connect with WASAAT" button in `index.html` with a `mailto:` link.

The current logo is derived from the logo image supplied for the site.
