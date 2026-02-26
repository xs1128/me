# Personal Website

A static website built with [Nanoc](https://nanoc.ws/) and hosted on [GitHub Pages](https://pages.github.com/).

## Deployment Steps

After making changes to the `main` branch, follow these steps to redeploy:

### Method 1: Manual Deployment (Recommended)

```bash
# 1. Compile the site
nanoc compile

# 2. Deploy to gh-pages branch
cd output
git add -A
git commit -m "Deploy site"
git push -f origin gh-pages
cd ..
```

### Method 2: Using Nanoc Deploy Command (Not Currently Configured)

The `nanoc deploy` command requires the output directory to be a separate git repository clone. This is not currently set up.

## Project Structure

- `content/` - Source files for the website
  - `index.html` - Main English page
  - `zh.html` - Simplified Chinese page
  - `zh-TW.html` - Traditional Chinese page
  - `custom.css` - Custom styles
  - `CNAME` - Custom domain configuration
- `layouts/` - ERB templates
- `lib/` - Helper functions
- `nanoc.yaml` - Nanoc configuration
- `Rules` - Compilation rules
- `output/` - Compiled site (deployed to gh-pages branch)

## Branches

- `main` - Source code (Nanoc project)
- `gh-pages` - Compiled site (served by GitHub Pages)

## Local Development

```bash
# Install dependencies
bundle install

# Compile the site
nanoc compile

# Preview locally (requires installing nanoc-live)
gem install nanoc-live
nanoc live
```

## Domain

This site is served at https://xsooi.com
