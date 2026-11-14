# Eslam Senosy Mahmoud — Media Buyer Portfolio

Personal portfolio site for Eslam Senosy Mahmoud, Media Buyer (Egypt & GCC).

- **Live site:** https://mediabuyer.tech
- **Stack:** single-file `index.html` (EN + AR), GSAP + ScrollTrigger, no build step.
- **Admin panel:** open `https://mediabuyer.tech/?admin=1` — edits save to the browser's localStorage only. To publish admin edits, export the JSON backup from the panel and send it to Muse; it gets baked into the site defaults and deployed.

## Structure

```
index.html            # the whole site (content lives in the C object, EN + AR)
assets/
  logos/              # 25 brand logos (webp)
  logos/companies/    # 4 experience company logos (webp)
  platform/           # Google Ads / Meta / TikTok / Snapchat / Shopify icons (svg)
  js/                 # GSAP + ScrollTrigger (local copies)
  fonts/              # Anton font CSS (Google Fonts @font-face)
```

## Deploy

The site is served from this repo on the VPS (nginx behind Traefik) at
`mediabuyer.tech`. A cron pulls `main` every 5 minutes, so any push here goes
live automatically within ~5 minutes.
