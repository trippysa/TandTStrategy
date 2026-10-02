# TandTStrategy.com

Source for [tandtstrategy.com](https://tandtstrategy.com), hosted on GitHub Pages.

Everything in `site/` is published. Pushing to `main` deploys automatically via
`.github/workflows/deploy.yml`.

## One-time setup

1. **Create `main`** — on GitHub, create a `main` branch from
   `claude/tandtstrategy-github-setup-apmrkg` and make it the default branch
   (Settings → General → Default branch).
2. **Enable Pages** — Settings → Pages → *Build and deployment* → Source:
   **GitHub Actions**.
3. **Custom domain** — Settings → Pages → Custom domain: `tandtstrategy.com`,
   then Save. Once the DNS check passes, tick **Enforce HTTPS**.
4. **DNS records** at your domain registrar:

   | Type  | Host / Name | Value                 |
   |-------|-------------|-----------------------|
   | A     | `@`         | `185.199.108.153`     |
   | A     | `@`         | `185.199.109.153`     |
   | A     | `@`         | `185.199.110.153`     |
   | A     | `@`         | `185.199.111.153`     |
   | AAAA  | `@`         | `2606:50c0:8000::153` |
   | AAAA  | `@`         | `2606:50c0:8001::153` |
   | AAAA  | `@`         | `2606:50c0:8002::153` |
   | AAAA  | `@`         | `2606:50c0:8003::153` |
   | CNAME | `www`       | `trippysa.github.io`  |

   Remove any existing "parking" A/CNAME records on `@` and `www` first.
   DNS can take up to 24–48 hours to propagate.
5. **(Recommended)** Verify the domain to prevent takeover: your GitHub
   profile → Settings → Pages → *Add a domain*, then add the TXT record it gives you.
