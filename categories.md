---
layout: default
title: Categories
permalink: /categories/
---

<h1>Categories</h1>

{% for category in site.categories %}
  <h2 id="{{ category | first }}">{{ category | first }}</h2>
  <ul>
    {% for post in category | last %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
