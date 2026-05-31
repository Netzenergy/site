# Netz Energy — UAE site

Static marketing site for **Netz Energy**, the UAE arm of a French energy and
environmental engineering group. Independent advisory practice for the UAE built
environment: BACS audits, ISO 50001 advisory, commissioning &amp; retro-Cx, and
PV feasibility studies.

## Stack

Pure static HTML, CSS and a sliver of vanilla JavaScript &mdash; no build step,
no framework, no dependencies. Hosted as-is.

## Structure

```
.
├── index.html          # Home — hero, value pillars, track-record marquee, FAQ
├── about.html          # About — positioning, methodology, French parent
├── services.html       # Services overview
├── sectors.html        # Sectors / target clients
├── team.html           # Team
├── contact.html        # Contact form
├── services/
│   ├── bacs-audits.html
│   ├── iso-50001.html
│   ├── commissioning.html
│   └── pv-feasibility.html
└── assets/
    ├── style.css       # Single stylesheet (v6 minimalist + v7 overrides)
    ├── animations.js   # Reveal-on-scroll, live UAE clock, hero video FX
    ├── logo.png        # Logo for light backgrounds
    ├── logo-light.png  # Logo for dark backgrounds (nav, footer)
    └── logos/          # Client logos used in the track-record marquee
```

## Local preview

Open `index.html` directly in a browser. No server needed.

For a closer-to-production preview (font loading, relative paths, etc.) :

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Deploying to GitHub Pages

1. Create an empty repo on GitHub (public or private with Pages enabled).
2. From this folder :

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin git@github.com:<your-account>/<repo-name>.git
   git push -u origin main
   ```
3. On GitHub → repo **Settings → Pages** → Source : `Deploy from a branch` →
   Branch : `main` / folder : `/ (root)` → Save.
4. The site will be live a minute later at
   `https://<your-account>.github.io/<repo-name>/`.

To use a custom domain (e.g. `netzenergy.ae`) add a `CNAME` file at the root
with one line (the domain) and add the matching DNS records in your registrar.

## External assets used

- Google Fonts &mdash; Inter Tight, JetBrains Mono
- Unsplash photos &mdash; hero / page-head backgrounds (UAE construction &
  desert)
- Pexels videos &mdash; hero video band (autoplays muted, with image fallback)
- Clearbit logo CDN &mdash; fallback for client logos not yet in `assets/logos/`

All external assets are loaded over HTTPS and degrade gracefully if blocked.

## Editorial conventions

- All advisory references use international frameworks
  (ISO 50001/14001, EN ISO 52120, IPMVP, BREEAM In-Use, ASHRAE Guidelines,
  CSRD, EU Taxonomy) plus UAE codes (Estidama Pearl, Mostadam, RSB).
- France-only regulations (Décret Tertiaire, Décret BACS, RE2020, Loi APER,
  etc.) are deliberately excluded.
- Brand strapline : **Independent advisory · Vendor-neutral · No EPC
  commissions**.

## Client references

The track-record marquee on the home page surfaces real references from the
parent group&rsquo;s European portfolio :
SOMFY, IKEA, FNAC Darty, GXO Logistics, Grape Hospitality, APHP,
P&ocirc;le Emploi, CEREMA, Fondation Bellan.

---

&copy; 2026 Netz Energy &mdash; All rights reserved.
