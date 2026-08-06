# JusticiaAI.com landing page

Static landing page prepared for GitHub and Cloudflare Pages.

## Cloudflare Pages

- Framework preset: None
- Build command: leave blank
- Build output directory: `/`

The custom domain should be configured as `justiciai.com` after deployment.

## Acquisition form

The `Make an Offer` and `Ask a Question` buttons open an embedded acquisition
form. The browser posts JSON to `https://offers-api.justiciai.com/api/inquiry`.
The API is a separate Cloudflare Worker and uses Resend to deliver the inquiry.
Buyers are never asked to verify or confirm their email address.

Required Worker variables/secrets:

- `RESEND_API_KEY` — secret; reuse the existing Resend API key.
- `RESEND_FROM_EMAIL` — sender on the Resend-verified `quantivalue.com` domain,
  for example `JusticiaAI <offers@quantivalue.com>`.
- `INQUIRY_TO_EMAIL` — `offers@justiciai.com`.

Configure `offers-api.justiciai.com` as the Worker's custom domain. Cloudflare
Email Routing can continue forwarding `offers@justiciai.com` to the owner's
Gmail inbox.
