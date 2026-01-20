---
layout: page
title: Blog
permalink: /blog/
---

## 投稿一覧

<div class="blog-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 2rem; margin-top: 2rem;">
  {% assign sorted_blogs = site.blogs | sort: "date" | reverse %}
  {% for post in sorted_blogs %}
    <div class="card blog-card">
      <h3><a href="{{ post.url }}" style="color: #ffffff;">{{ post.title }}</a></h3>
      <p class="blog-date" style="color: #e5e7eb; font-size: 0.9em; margin: 0.5rem 0;">📅 {{ post.date | date: "%Y年%m月%d日" }}</p>
      <p class="blog-excerpt" style="color: #e5e7eb; margin: 1rem 0;">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ post.url }}" class="read-more" style="color: #ffffff; text-decoration: none; font-weight: bold;">続きを読む →</a>
    </div>
  {% endfor %}
</div>