# metagap-landing

The "coming soon" page for **https://metagap.online**, hosted free on GitHub Pages
(published from the `main` branch, root folder).

## Files

| File | What it is |
| --- | --- |
| `index.html` | The page. Edit the text here. |
| `style.css` | Colours and layout, with a dark mode. |
| `favicon.svg` | The tab icon (also drawn inline in `index.html`). |
| `404.html` | Shown for any address that does not exist. |
| `CNAME` | Tells GitHub Pages the custom domain. Do not delete or edit it. |
| `.nojekyll` | Tells GitHub to serve the files exactly as they are. |

To change the page, edit a file, commit and push to `main`. The live site
updates within a minute or two.

## DNS (Spaceship > the domain > Advanced DNS)

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `mynameisaaah.github.io` |

No other A, AAAA or CNAME records may exist on `@` or `www`; Spaceship's
parking page adds some by default, and they must be removed. The addresses
come from GitHub's own list: `gh api meta --jq .pages`.

## HTTPS

GitHub issues the certificate on its own once the DNS above resolves. After
that, turn on **Settings > Pages > Enforce HTTPS** (or
`gh api -X PUT repos/mynameisaaah/metagap-landing/pages -F https_enforced=true`).
