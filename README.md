# 200word.org

200 Lousy words - A Hugo-based blog with automatic GitHub Pages deployment.

## About

This is a simple, markdown-based blog built with Hugo. It features:
- Modern, clean design with dark mode support
- Markdown-based content
- No comments or interactions
- Automatic deployment to GitHub Pages

## Theme

The site uses a custom modernized minimal theme with:
- **CSS Variables** for easy theming
- **Dark Mode Support** that automatically adapts to system preferences
- **Modern Typography** with improved readability
- **Subtle Animations** for better user experience
- **Responsive Design** that works on all devices
- **Enhanced Code Blocks** with proper syntax highlighting support

## Setup

This repository is already configured with:
- Hugo static site generator (v0.119.0)
- Custom modernized minimal theme
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

Visit `http://localhost:1313/200word.org/` in your browser.

## Deployment

The site automatically deploys to GitHub Pages when you push to the `main` branch. The GitHub Actions workflow handles the build and deployment process.

To enable GitHub Pages:
1. Go to repository Settings → Pages
2. Set Source to "GitHub Actions"
3. The workflow will automatically deploy on the next push to main

## Building

To build the site manually:

```bash
hugo --gc --minify
```

The generated site will be in the `public/` directory.
