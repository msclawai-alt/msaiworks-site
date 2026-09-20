# MSAI Works site

A small, responsive static website for MSAI Works. It uses plain HTML, CSS, and SVG, so there are no dependencies or build step.

## Cloudflare Pages

Connect the `msaiworks-site` GitHub repository to Cloudflare Pages using Git integration. For a repository with these files at its root, use:

| Setting | Value |
| --- | --- |
| Production branch | `main` |
| Framework preset | None |
| Build command | Leave blank |
| Build output directory | `.` (repository root) |

After the first deploy, add `msaiworks.com` under the Pages project's **Custom domains**. Git integration deploys new commits pushed to `main` and provides preview deployments for pull requests. See [Cloudflare's static HTML guide](https://developers.cloudflare.com/pages/framework-guides/deploy-anything/) and [Git integration guide](https://developers.cloudflare.com/pages/get-started/git-integration/) for current dashboard steps.

The email forwarding records should remain on Cloudflare DNS when nameservers are switched: keep both Porkbun MX records and the SPF TXT record, set them to **DNS only**, and do not replace them with website records. Cloudflare Pages will provide the web DNS records when the custom domain is added.

`robots.txt` permits ordinary crawlers. Cloudflare's AI crawler controls are configured separately in the Cloudflare dashboard. The privacy page describes this site's current static setup; revise it if analytics, forms, or other data collection are added.

## Local preview

Open `index.html` in a browser, or serve this directory with any static file server. No package installation is needed.
