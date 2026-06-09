# Inspire & Educate Website

Static website for Inspire & Educate, a Bay Area menstrual equity nonprofit. The site explains the mission, routes donations to Givebutter, and supports volunteer, product-drive, partnership, and contact inquiries.

Live deployment: https://lustrous-hamster-fabafc.netlify.app/

## Structure

```text
index.html          Homepage and cited need statement
about.html          Origin story, mission, board, advisory council
get-involved.html   Donation tiers, volunteer options, product-drive CTA
contact.html        Netlify-powered contact form and FAQ
styles.css          Shared design system
netlify.toml        Netlify static deployment configuration
robots.txt          Search crawler hints
sitemap.xml         Basic sitemap for deployed pages
```

## Donation integration

The donation UI is centralized through a Givebutter campaign placeholder in `get-involved.html`:

```js
const GIVEBUTTER_CAMPAIGN_URL = 'https://givebutter.com/REPLACE-WITH-CAMPAIGN';
```

Replace this with the live Givebutter campaign URL before launch. Donation buttons preserve amount and frequency through query parameters where supported by Givebutter. If Givebutter ignores those parameters, the links still route donors to the campaign page.

## Contact form

`contact.html` uses Netlify Forms:

```html
<form name="contact" method="POST" data-netlify="true" netlify-honeypot="bot-field">
```

After deployment, submit one test message and confirm it appears in the Netlify Forms dashboard.

## Citation policy

Public factual claims on the homepage are cited inline with numbered superscripts and linked references. Any new statistic, epidemiologic statement, or health-risk claim must be added to the reference list before launch.

Current reference categories:

1. World Bank menstrual hygiene management evidence
2. Santa Clara County Point-in-Time homelessness reports
3. Peer-reviewed period poverty / menstrual hygiene needs article
4. FDA tampon safety guidance

## Launch checklist

- [ ] Replace Givebutter placeholder URL
- [ ] Complete a test donation
- [ ] Confirm Netlify form submission
- [ ] Replace placeholder social links with real profiles or email links
- [ ] Verify 501(c)(3) / tax-deductibility language before public launch
- [ ] Add custom domain and update `sitemap.xml`
- [ ] Add Open Graph preview image
- [ ] Test on mobile Safari and Chrome
