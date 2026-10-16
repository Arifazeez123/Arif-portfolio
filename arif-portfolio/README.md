# Muhammed Arif — Portfolio Website

A responsive, static portfolio website for GitHub Pages. Every push to `main` triggers GitHub Actions to publish the site.

## Before publishing

1. Search `index.html` for `YOUR_EMAIL@example.com` and replace it with your real email address.
2. Replace the LinkedIn homepage URL with your profile URL.
3. Update project links to the individual repositories (the current links point to your GitHub profile).
4. Verify every skill, project description, internship date, and credential. Add a certificate URL/year for the NPTEL credential and only list completed certifications as completed.
5. Optionally add a PDF resume and link it from the page.

## Publish with GitHub Actions

1. Create a public repository named `arif-portfolio` on GitHub. Do not initialize it with a README if you plan to push this folder as-is.
2. Open a terminal in this folder and run:

   ```bash
   git init
   git add .
   git commit -m "Build personal portfolio"
   git branch -M main
   git remote add origin https://github.com/Arifazeez123/arif-portfolio.git
   git push -u origin main
   ```

3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment → Source**, select **GitHub Actions**.
5. Open the **Actions** tab and watch `Deploy portfolio to GitHub Pages`. The first deployment can take a few minutes.
6. Your site should be available at `https://arifazeez123.github.io/arif-portfolio/`.

## How the automation works

- A push to `main` starts `.github/workflows/deploy.yml`.
- `actions/checkout` downloads the repository contents to the runner.
- `actions/upload-pages-artifact` packages the static site files.
- `actions/deploy-pages` publishes the artifact to GitHub Pages.
- Future pushes to `main` deploy automatically. You can also run it manually from **Actions → Deploy portfolio to GitHub Pages → Run workflow**.

This is a static HTML/CSS/JavaScript site, so no Node.js build step is required.
