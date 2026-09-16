# newproj.github.io

This project is configured as a static Vite site that can be published to GitHub Pages.

## Local development

```bash
npm install
npm run dev
```

## GitHub Pages publishing

- The Vite config uses a relative base path so assets continue to load when the site is served under a repository subpath.
- Production builds output to the `docs/` directory, which GitHub Pages can publish directly.
- To publish:
  1. Run `npm run build`
  2. Commit the generated `docs/` folder changes
  3. In GitHub repository settings, set Pages source to `Deploy from a branch` and choose the `main` branch with the `/docs` folder

If you prefer a workflow-based deployment, GitHub Actions can also deploy the generated `docs/` directory to Pages.