GitHub Pages deployment

This repository includes a GitHub Actions workflow that builds the Astro site in `orbital-osiris` and deploys the output (`orbital-osiris/dist`) to GitHub Pages.

What the workflow does
- Runs on pushes to `main` or when manually triggered.
- Installs Node.js 22, runs `npm ci`, and `npm run build` inside `orbital-osiris`.
- Uploads `orbital-osiris/dist` and deploys it to GitHub Pages using the official actions.

How to enable GitHub Pages
1. In the repository settings, go to Pages.
2. The Actions deployment will publish the site; ensure GitHub Pages is enabled and the site is set to use GitHub Actions.
3. Optionally set a custom domain or enforce HTTPS.

Notes
- If you change the Astro output directory, update `.github/workflows/deploy.yml` accordingly.
- The workflow requires no secrets; it uses the repository permissions for Pages.
