# JusticiaAI.com landing page

Static landing page prepared for GitHub and Cloudflare Pages.

## Cloudflare Pages

- Framework preset: None
- Build command: leave blank
- Build output directory: `/`

The custom domain should be configured as `justiciai.com` after deployment.

## Acquisition form

The `Make an Offer` and `Ask a Question` buttons open an embedded acquisition
form. Submissions are delivered to `offers@justiciai.com` through FormSubmit.

After deploying this version, submit the form once and approve FormSubmit's
one-time confirmation email. Cloudflare Email Routing must already be active
for `offers@justiciai.com` so that confirmation and future inquiries reach the
destination inbox.
