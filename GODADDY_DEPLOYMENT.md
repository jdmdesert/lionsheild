# GoDaddy deployment guide

Lion Shield is a portable static website. It requires no database, server runtime, build process, appointment system, or third-party application.

## Exact deployment: GoDaddy Web Hosting (cPanel)

Use this option to preserve the website exactly as designed.

1. Open the GoDaddy product dashboard.
2. Under **Web Hosting**, select **Manage** for the applicable account.
3. Open **File Manager** for the domain.
4. Open the domain's web root, normally `public_html` for the primary domain.
5. Upload `releases/lion-shield-godaddy.zip`.
6. Extract the ZIP directly in the web root.
7. Confirm that `index.html`, `styles.css`, `script.js`, and the `assets` folder are directly inside the web root—not inside another `dist` folder.
8. Visit the domain and verify the home page, navigation, images, and mobile layout.

The ZIP contains only files needed by GoDaddy. The OpenAI Sites hosting manifest and repository metadata are intentionally excluded.

## Airo AI Builder: rebuild workflow

Airo AI Builder does not accept a custom-code or file upload. It can instead rebuild a site from a published URL or screenshots.

1. Publish the current site somewhere Airo can access.
2. In Airo AI Builder, choose **Rebuild my site**.
3. Provide the published site URL. The current private preview may require public access before Airo can read it.
4. Choose the option to keep a similar look.
5. Ask Airo to preserve the logo, images, colors, and fonts.
6. Paste the brief from `AIRO_REBUILD_BRIEF.md` into the additional-details field.
7. Compare Airo's result with the supplied reference screenshot and this repository's `dist/index.html`.

Airo will generate a new site inspired by the source rather than importing the exact code. Navigation, spacing, typography, and responsive behavior may need to be adjusted inside Airo.

## Source files

The production-ready static files remain in `dist/`:

- `index.html`
- `styles.css`
- `script.js`
- `assets/hero-barbershop.png`
- `assets/barber-at-work.png`

