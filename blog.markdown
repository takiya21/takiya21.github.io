---
layout: page
title: Blog
permalink: /blog/
---
## 投稿一覧

<ul>
  {% for post in site.blogs %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%Y-%m-%d" }}
    </li>
  {% endfor %}
</ul>