# Mindforge Public Site (GitHub Pages)

A simple, static, privacy-friendly website for the Mindforge project:

- `index.html` — homepage: what Mindforge does, how it works, privacy-first design
- `privacy.html` — the Privacy Policy (Google OAuth, `youtube.upload` scope, GitHub Actions Secrets, retention & deletion)
- `style.css` — one shared stylesheet; **no external assets, no cookies, no trackers, no analytics**

Nothing here connects to or modifies the `mindforge-automation` repository.

## Publish it (one-time, ~3 minutes)

1. Create a new **public** GitHub repository named `mindforge-privacy`
   (github.com/new — do not initialize it with a README).
2. Push this folder to it:
   ```
   cd C:\Users\hamza\mindforge-privacy
   git remote add origin https://github.com/YOUR_USERNAME/mindforge-privacy.git
   git push -u origin main
   ```
3. Enable Pages:
   **Settings → Pages → Build and deployment → Source: "Deploy from a branch" →
   Branch: `main`, Folder: `/ (root)` → Save.**
4. Wait 1–2 minutes. The site goes live at:
   `https://YOUR_USERNAME.github.io/mindforge-privacy/`
   (Each push to `main` redeploys automatically.)

## Before publishing — fill in the contact email

The email in **both** `index.html` and `privacy.html` is a placeholder:
`YOUR-CONTACT-EMAIL@EXAMPLE.COM`. Replace it in both files after the owner
confirms the real address (grep for `YOUR-CONTACT-EMAIL`).

## Google verification notes (OAuth branding)

- GitHub Pages URLs can be verified in **Google Search Console** as a
  **URL-prefix property** — enter the full Pages URL (including the
  `/mindforge-privacy/` path) and verify with the **HTML file** method: drop
  Google's `googleXXXX.html` file in this folder's root and push.
- For the OAuth consent screen's homepage/privacy-policy links, Google checks
  that the domains are verified properties in Search Console. A verified
  GitHub Pages URL prefix is generally accepted.
- **Honest caveats:** Google recommends (and for full production verification
  of sensitive scopes may effectively require) a **custom domain you own at
  the top level** (e.g. `mindforge.example`). Path-based github.io URLs can be
  rejected in some verification reviews, and approval is never guaranteed.
  If Google's review insists, buy a cheap domain and point it at Pages
  (Settings → Pages → Custom domain).
- Important context: while the automation is used **only by its owner**
  (unverified app, "Go to app (unsafe)" bypass), **no verification is
  required at all**. Branding verification only becomes relevant if other
  people authorize the app or Google requests it.
