---
layout: default
title: Blog
permalink: /blog
---

<ul>
  {% for post in site.posts %}
  <li>
    <h3><a href="{{ post.url }}" class="post-preview">{{ post.title }}</a></h3>
    {{post.date}}
    {{post.excerpt}}
  </li>
  {% endfor %}
</ul>
