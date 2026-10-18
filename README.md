# FuTech — Client-ready website bundle

This bundle contains the FuTech marketing site, cinematic interactive case-study gallery for six concept projects, responsive styles, shared JavaScript, and the guided chatbot assets.

## Run locally
1. Extract the complete ZIP.
2. Open the folder in VS Code.
3. Start `index.html` with VS Code Live Server (or any static HTTP server).
4. Test the navigation, project filters, all six case studies, estimator, customizer, FAQ, enquiry form, and chatbot on desktop and mobile.

## Required launch configuration
Before publishing, open `script.js` and update the `CONFIG` object at the top:
- `WHATSAPP_NUMBER`: your business WhatsApp number in international digits-only format (example format: `919876543210`). Until configured, WhatsApp buttons will guide visitors to the contact section rather than opening a broken `wa.me` URL.
- `FORMSPREE_URL`: optional form endpoint, such as your real Formspree form URL. Without it, the form validates and offers WhatsApp delivery only when a valid number is configured; it does not pretend to send enquiries to a server.
- `NEWSLETTER_URL`: optional endpoint for the newsletter. Leave empty unless a real endpoint is connected.

Open `chatbot.js` and set `CHAT.API_URL` only after deploying the optional backend. The chatbot works in guided mode without an AI backend. Never put private API keys in browser JavaScript.

## Before client launch
- Replace demo business details, contact information, pricing, delivery timelines, and any sample copy with approved real information.
- Confirm that package prices in `index.html`, `script.js`, and `chatbot.js` match your actual offers.
- Replace or remove any unverified performance numbers, testimonials, client claims, and illustrative analytics. The six portfolio entries are clearly labelled concept projects and must not be presented as paid client work.
- Add the real production domain to Open Graph metadata and provide a social share image.
- Test form delivery end-to-end after configuring the endpoint; check success and failure states.
- Test at common mobile widths, keyboard-only navigation, focus visibility, and reduced-motion settings.
- Compress and license-check all images and fonts; use HTTPS on hosting.
- Add a privacy policy and cookie notice if your analytics, forms, or third-party services require them.

## Deployment
The site is static and can be deployed to Netlify, Cloudflare Pages, GitHub Pages, or another static host. The optional AI chatbot backend source and Wrangler configuration are in `worker/`. Deploy it separately only if you want AI mode; it is not enabled by default.
