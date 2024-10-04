# 4248 Github Pages Theme

A theme based on the minimal theme and modified to follow the 4248 color scheme.

## Installation

Create the following workflow file in your repository at `.github/workflows/pages.yml`:

```yaml
name: Deploy Jekyll with GitHub Pages dependencies preinstalled

on:
  push:
    branches: ["main"]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup 0x4248 theme
        run: curl https://raw.githubusercontent.com/0x4248/4248_github_pages_theme/refs/heads/main/setup.sh > setup.sh && sh setup.sh
      - name: Setup Pages
        uses: actions/configure-pages@v5
      - name: Build with Jekyll
        uses: actions/jekyll-build-pages@v1
        with:
          source: ./
          destination: ./_site
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3

  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

Or run this on your project root:

```bash
mkdir -p .github/workflows
curl https://raw.githubusercontent.com/0x4248/4248_github_pages_theme/refs/heads/main/pages.yml > .github/workflows/pages.yml
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 3.0 Unported License](http://creativecommons.org/licenses/by-sa/3.0/). Please see the original author of this theme [here](https://github.com/orderedlist/minimal).
