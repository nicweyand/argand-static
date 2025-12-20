# Argand Static Site Editing Guide
**By Nic Weyand!**

Quick reference for updating content on argand.org.

## File Location

```
/home/nicweyand/RustroverProjects/argand-static-site/index.html
```

## Key Sections to Edit

| Content | Search for |
|---------|-----------|
| Tagline | `<h1>` and `<p class="subtitle">` |
| Service cards | `<div class="service-card">` blocks |
| Feature tags | `<span class="feature-tag">` elements |
| Under the Hood | `<section class="tech">` and `.tech-item` blocks |
| Philosophy | `<section class="philosophy">` |
| Footer | `<footer>` section |
| "What's an Argand?" tooltip | Search for `argand-tooltip-text` |

## Deployment Workflow

```bash
cd ~/RustroverProjects/argand-static-site

# Edit with any editor
kate index.html
# or: code index.html
# or: nvim index.html

# Commit and push
git add index.html
git commit -m "Update: <what you changed>"
git push
```

DigitalOcean auto-deploys within ~1-2 minutes after push.

## Tips

- Preview locally first: `xdg-open index.html`
- CSS is inline in `<style>` tags at the top
- JavaScript is inline at the bottom in `<script>` tags
- Colors use CSS variables (search `:root` for the palette)
