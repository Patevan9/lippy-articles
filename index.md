---
layout: default
title: Articles
---
<div class="hero">
  <span class="hero-eyebrow">Lippy Robotics</span>
  <h1 class="hero-title">Articles &amp; <em>Updates</em></h1>
  <p class="hero-sub">News, notes, and writing from the team behind Scout.</p>
</div>

<div class="articles-wrap">
  {% assign articles = site.articles | sort: "date" | reverse %}
  {% if articles.size > 0 %}
    {% for article in articles %}
    <a class="article-card" href="{{ article.url | relative_url }}">
      <span class="article-card-date">{{ article.date | date: "%B %-d, %Y" }}</span>
      <h2 class="article-card-title">{{ article.title }}</h2>
      {% if article.excerpt %}
      <p class="article-card-excerpt">{{ article.excerpt | strip_html | truncate: 160 }}</p>
      {% endif %}
    </a>
    {% endfor %}
  {% else %}
    <p class="articles-empty">No articles yet — check back soon.</p>
  {% endif %}
</div>
