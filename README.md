# Samuel D. Martin — Portfolio Site

A single self-contained `index.html` (no build step, no dependencies except Google Fonts via CDN). Dark, modern tech/SaaS aesthetic.

## What's inside
- **Hero** — positioning as an Agile & AI change agent
- **About** — narrative + three operating principles (Interactions over Artifacts / Methods over Rituals / Adaptation over Adherence)
- **Expertise** — Agile Transformation, Applied AI, Product Engineering
- **Portfolio** — BearingCPM, PI Planning Studio, HQ Companion (each with feature set + technical stack + live link)
- **Contact** + footer

---

## ✅ Personalized (already done)
- **Contact** wired to LinkedIn profile (`https://www.linkedin.com/in/samueldmartin/`).
- **Real product screenshots** embedded for all three products (in `assets/`), shown in browser-style frames.
- Feature sets rewritten to match what each app's UI actually shows (earned-value + resource leveling + AI orchestration for BearingCPM; capacity-aware iteration planning + confidence vote for PI Planning Studio; illustrated champion sheets + stat orbs for HQ Companion).

## ⚠️ Optional — things you may still want to confirm/personalize
- **Bio claims** — Hero section reflects highest certifications ("Google Gen AI Leader" and "Scaled Agile Practitioner (SPC)"). Adjust wording or add your current title/employer if you like.
- **Product roles** — labeled "Founder & Builder" / "Creator." Change if your actual role differs.
- **HQ Companion disclaimer** — the app itself carries an "unofficial / not affiliated with Hasbro" notice; add it here too if you want.
- **Profile photo / favicon** — not yet included.

---

## Deploy to Bluehost (shared hosting)

Once your domain is set up in Bluehost:

### Option A — File Manager (easiest)
1. Log in to **Bluehost → Hosting → cPanel → File Manager**.
2. Open the **`public_html`** folder (this is your web root). For an add-on/secondary domain, open that domain's document root instead.
3. **Upload** `index.html` **and the entire `assets/` folder** into `public_html` (keep them side-by-side — the screenshots are referenced as `assets/…`).
   - If there's an existing `default.html` / placeholder `index.html`, delete or rename it so yours loads.
4. Visit your domain — the site is live. `index.html` is served automatically at the root.

### Option B — FTP (SFTP/FTP client like FileZilla)
1. In cPanel, create/find your **FTP account** credentials.
2. Connect with host = your domain or server IP, your FTP user/pass, port 21 (FTP) or 22 (SFTP).
3. Upload `index.html` into `public_html/`.

### Notes
- **No server config needed** — this is pure static HTML/CSS/JS. No PHP, no database, no Node.
- **HTTPS**: Bluehost provisions a free Let's Encrypt SSL cert. In cPanel enable **SSL/TLS Status → Run AutoSSL** if it isn't already, so the site loads over `https://`.
- **Fonts** load from Google Fonts CDN (needs internet — fine for a hosted site). To make it fully offline/self-hosted, download the font files and swap the `<link>` for local `@font-face`.
- **Caching**: after re-uploading edits, hard-refresh (Ctrl+F5) to bypass browser cache.

---

## Editing
Everything is in one file. Open `index.html` in any editor:
- Colors live in the `:root { ... }` CSS variables at the top (`--accent`, `--bg`, etc.).
- Text content is plain HTML in the `<body>` — search for the section you want (e.g. `id="about"`, `BearingCPM`).

Verified: renders cleanly in-browser, zero console/JS errors, responsive down to mobile, and all content is visible even if JavaScript is disabled (animations are purely additive).
