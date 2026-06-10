# TSQA Website

**Protecting People, Perfecting Process**

A static website for TSQA — HSEQ consulting services and software platform.

---

## Files

```
tsqa-site/
├── index.html        ← Homepage
├── consulting.html   ← Consulting services page
├── platform.html     ← Software platform + login section
├── contact.html      ← Contact form
├── style.css         ← Shared stylesheet
├── logo.png          ← TSQA logo
└── README.md         ← This file
```

---

## How to Publish on GitHub Pages

1. **Create a new GitHub repository**
   - Go to [github.com](https://github.com) → New repository
   - Name it `tsqa-website` (or anything you like)
   - Set visibility to **Public**
   - Click **Create repository**

2. **Upload all files**
   - Click **Add file → Upload files**
   - Drag and drop ALL files from this folder (including `logo.png` and `style.css`)
   - Click **Commit changes**

3. **Enable GitHub Pages**
   - Go to your repository → **Settings** → **Pages**
   - Under "Source", select **Deploy from a branch**
   - Branch: `main` — Folder: `/ (root)`
   - Click **Save**

4. **Your site is live**
   - After a minute or two, your site will be at:
   - `https://YOUR-GITHUB-USERNAME.github.io/tsqa-website/`

---

## Things to Update Before Going Live

- **Contact email** — in `contact.html`, replace `info@tsqa.co.nz` with your real email
- **Phone number** — in `contact.html`, replace the placeholder phone number
- **Google Reviews link** — search `TSQA+reviews` in the three review buttons and replace with your actual Google Business review URL
- **Platform login URL** — in `platform.html`, find the "Sign in to Platform" button and replace `href="#"` with your real platform URL
- **Contact form backend** — the form currently shows a success message but doesn't send email. To make it functional, sign up for [Formspree](https://formspree.io) (free tier available) and update the form action

### Connecting Formspree (free contact form emails)
1. Sign up at formspree.io
2. Create a new form — copy your form endpoint URL (looks like `https://formspree.io/f/xxxxxxxx`)
3. In `contact.html`, change:
   ```html
   <form id="contactForm" onsubmit="handleSubmit(event)">
   ```
   to:
   ```html
   <form id="contactForm" action="https://formspree.io/f/YOUR_CODE" method="POST">
   ```
4. Remove the `onsubmit` handler and the `handleSubmit` JavaScript function

### Custom Domain (optional)
If you have a domain like `tsqa.co.nz`:
1. In GitHub Pages settings, enter your custom domain
2. With your domain registrar, add a CNAME record pointing to `YOUR-USERNAME.github.io`

---

## Customisation Notes

- All colours are defined as CSS variables at the top of `style.css` — easy to tweak
- The font is Inter (body) + Barlow Condensed (headings) — loaded from Google Fonts
- The site is fully responsive down to mobile
- No build tools, no dependencies — pure HTML/CSS/JS
