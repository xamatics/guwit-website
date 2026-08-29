# guwit.com

Website for **Guwit Technology Solutions Ltd** (RC 9040112), Badagry, Lagos State, Nigeria.

Static HTML and CSS. No build step, no framework, no dependencies. Open any `.html` file in a
browser and it works.

---

## Files

```
index.html          Home
about.html          About the company
services.html       The four core services + wider registered trade
work.html           Case studies: Learn Gungbe, Owa Delivery, language work
contact.html        Contact form and company details
privacy.html        Privacy policy (NDPA 2023)
terms.html          Terms of service
404.html            Not-found page

assets/style.css    All styling. Brand colours are the CSS variables at the top.
assets/main.js      Mobile menu toggle and the footer year. That is all it does.
assets/logo.svg     The mark, redrawn as vector
assets/favicon.svg  Browser tab icon
assets/img/         Drop real photos and screenshots here (see the README inside)

CNAME               Tells GitHub Pages the domain is guwit.com
.nojekyll           Stops GitHub reprocessing the files
robots.txt          Search engine instructions
sitemap.xml         Page list for search engines
humans.txt          Credits
site.webmanifest    Icon and colour for phone home screens
```

---

## Publishing on GitHub Pages

**1. Create the repository**

On github.com, create a new **public** repository. Name it `guwit-website` (any name works).

**2. Upload the files**

Either drag the whole folder into GitHub's upload page, or from a terminal:

```bash
cd guwit
git init
git add .
git commit -m "Guwit website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/guwit-website.git
git push -u origin main
```

**3. Turn on Pages**

Repository → **Settings** → **Pages** → under *Build and deployment*, set Source to
**Deploy from a branch**, branch `main`, folder `/ (root)`. Save.

The site appears at `https://YOUR-USERNAME.github.io/guwit-website/` within a minute or two.

**4. Point guwit.com at it (Namecheap)**

In Namecheap → Domain List → **Manage** next to guwit.com → **Advanced DNS**.
Delete the parking records that are there, then add these five:

| Type | Host | Value | TTL |
|---|---|---|---|
| A Record | @ | 185.199.108.153 | Automatic |
| A Record | @ | 185.199.109.153 | Automatic |
| A Record | @ | 185.199.110.153 | Automatic |
| A Record | @ | 185.199.111.153 | Automatic |
| CNAME Record | www | YOUR-USERNAME.github.io. | Automatic |

Then back in GitHub → Settings → Pages → **Custom domain**, enter `guwit.com` and save.
Wait for the DNS check to pass (usually under an hour, occasionally up to 24), then tick
**Enforce HTTPS**.

The `CNAME` file in this repository already contains `guwit.com`, so GitHub will pick it up
automatically.

---

## Before you go live — a short checklist

- [ ] **Contact form.** It posts to Formspree but has a placeholder ID. Create a free form at
      [formspree.io](https://formspree.io), then in `contact.html` replace `YOUR_FORM_ID` in the
      form's `action` with the ID they give you. Until you do, the form will not deliver —
      the email and WhatsApp buttons next to it work regardless.
- [ ] **Play Store link.** In `work.html`, the Learn Gungbe button points at a Play Store search.
      Replace it with the app's real listing URL.
- [ ] **Social image.** Add `assets/img/og-cover.png` at 1200 × 630 so links shared on WhatsApp,
      LinkedIn and X show a proper card.
- [ ] **Screenshots.** Add real app and WhatsApp screenshots to `assets/img/` and swap them into
      the `.shot` blocks in `work.html` (instructions in `assets/img/README.txt`).
- [ ] **Legal dates.** `privacy.html` and `terms.html` say *Last updated: 1 January 2026*. Change
      to the date you publish.
- [ ] **Payment terms.** `terms.html` section 5 says deposit up front, balance on delivery, 14-day
      invoices. Change it if that is not how you work.
- [ ] **Office hours.** `contact.html` says Mon–Fri 9–6, Sat 10–2. Correct it if needed.
- [ ] **Google Search Console.** Add guwit.com and submit `sitemap.xml`.
- [ ] **Google Business Profile.** Worth claiming for a Badagry address — it is how local clients
      will find you.

---

## Changing things

**Brand colours** live at the top of `assets/style.css`:

```css
--plum:#7B5C9D;    /* the ring in the logo */
--leaf:#8ED486;    /* the arc */
--amber:#DCA22C;   /* the dot */
```

Change those three and the whole site follows.

**Adding a page.** Copy `about.html`, change the `<title>`, the `<meta name="description">`, the
`<link rel="canonical">` and the content between `<main>` and `</main>`. Add the new file to
`sitemap.xml`. If it belongs in the menu, add a link to the `<nav>` in every page's header.

**Typefaces** are Newsreader (headings), Plus Jakarta Sans (body) and IBM Plex Mono (small labels),
loaded from Google Fonts in each page's `<head>`.

---

© Guwit Technology Solutions Ltd (RC 9040112). All rights reserved.
