---
layout: page
title: Apps
permalink: /apps/
---

## アプリ一覧

<div class="blog-grid" style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 2rem; margin-top: 2rem;">
  {% assign sorted_apps = site.apps | sort: "date" | reverse %}
  {% for app in sorted_apps %}
    <div class="card blog-card">
      <h3><a href="{{ app.app_url }}" style="color: #ffffff;">{{ app.title }}</a></h3>
      <p class="blog-date" style="color: #e5e7eb; font-size: 0.9em; margin: 0.5rem 0;">📅 {{ app.date | date: "%Y年%m月%d日" }}</p>
      <p class="blog-excerpt" style="color: #e5e7eb; margin: 1rem 0;">{{ app.excerpt | strip_html | truncatewords: 30 }}</p>
      <a href="{{ app.url }}" class="read-more" style="color: #ffffff; text-decoration: none; font-weight: bold;">詳細を見る →</a>
    </div>
  {% endfor %}
</div>
