# GroSuite

Static site. No build step.

```
index.html      page
css/style.css   styles
js/scene.js     Three.js hero (ES module, loaded from jsdelivr)
js/main.js      nav toggle, scroll reveal
assets/         favicon
serve.mjs       local dev server
```

## Run locally

```
node serve.mjs
```

Open http://127.0.0.1:8091. A server is required: browsers block ES modules over `file://`.

## Deploy

Upload everything except `serve.mjs` and `.claude/` to any static host.

GitHub Pages: every push to `main` runs `.github/workflows/pages.yml`, which copies the site files to the `gh-pages` branch. Live at https://nikhil-sudhan.github.io/GroSuite/
