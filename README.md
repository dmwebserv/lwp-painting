# lwp-painting

Marketing website for LWP Painting & Decorating, a painting and decorating
business serving Essex and Suffolk.

## What this is

A static HTML/CSS site (no build step, no framework). It is deployed via
GitHub Pages, with a custom domain configured through the `CNAME` file and
DNS managed on Cloudflare.

Key files:

- `index.html` - the main landing page (services, gallery, testimonials, quote form)
- `privacy-policy.html` - the site's privacy policy
- `thanks.html` - the quote form's thank-you page (noindex)
- `css/style.css` - all site styling
- `images/` - photos, video and favicon used across the site
- `CNAME` - the custom domain served by GitHub Pages

The contact form posts to FormSubmit.co and redirects to `thanks.html` on
success; there is no backend in this repo.

## Previewing changes locally

No build tools are required. Either open `index.html` directly in a browser,
or serve the folder locally so relative paths behave the same as in
production, for example:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploying

Deployment is automatic: GitHub Pages serves whatever is on the deployed
branch (check the repository's Pages settings for which branch that is).
Push your committed changes to that branch and GitHub Pages will publish
them, usually within a minute or two. The custom domain in `CNAME` stays in
place across deploys as long as that file is present.
