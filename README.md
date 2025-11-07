# 200word.org

200 Lousy words - A Hugo-based blog with automatic GitHub Pages deployment.

## About

This is a simple, markdown-based blog built with Hugo. It features:
- Clean, minimal design
- Markdown-based content
- No comments or interactions
- Automatic deployment to GitHub Pages

## Setup

This repository is already configured with:
- Hugo static site generator (v0.119.0)
- Custom minimal theme
- GitHub Actions workflow for automatic deployment

## Creating New Posts

To create a new blog post:

```bash
hugo new content/posts/your-post-name.md
```

Then edit the file in `content/posts/` and set `draft = false` when ready to publish.

## Local Development

To run the site locally:

```bash
hugo server -D
```

Visit `http://localhost:1313/` in your browser.

## Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch. The GitHub Actions workflow handles the build and deployment process.

To enable GitHub Pages:
1. Go to repository Settings → Pages
2. Set Source to "GitHub Actions"
3. The workflow will automatically deploy on the next push to main

### Custom Domain Setup

This repository is configured to use the custom domain `200word.org`. To complete the setup:

1. Configure DNS settings for your domain:
   - **Option A (Recommended)**: Add A records pointing to GitHub Pages IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - **Option B**: Add a CNAME record pointing to `nthapa13.github.io`

2. In repository Settings → Pages:
   - The custom domain should automatically be detected from the CNAME file
   - Enable "Enforce HTTPS" (recommended, may take time to provision certificate)

3. Wait for DNS propagation (can take up to 24-48 hours)

The CNAME file in the `static/` directory tells GitHub Pages to use the custom domain.

## Building

To build the site manually:

```bash
hugo --gc --minify
```

The generated site will be in the `public/` directory.
