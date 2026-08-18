# lippy-articles

Articles site for [Lippy Robotics](https://patevan9.github.io/lippyrobotics.github.io/), built with Jekyll and hosted on GitHub Pages.

- **Live site:** https://patevan9.github.io/lippy-articles/
- **Theme:** matches the palette, fonts, and nav/footer style of the main Lippy Robotics site.

## Adding an article

Add a new Markdown file inside `_articles/`, with front matter like:

```
---
title: "Your Article Title"
date: 2026-08-20
---
```

...followed by the article content in Markdown. Commit and push — GitHub Pages rebuilds automatically. The article gets its own clean URL at `/articles/<filename>/`.

## Local structure

```
_config.yml          site settings
_layouts/             default.html (shared shell) and article.html (single article)
_includes/            nav.html and footer.html partials
_articles/             one Markdown file per article
assets/                logo.png and css/style.css
index.md               the articles listing page
```

No Gemfile — this relies on GitHub Pages' built-in Jekyll build (no custom plugins used), which keeps things simple with nothing extra to install or maintain.
