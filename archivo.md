---
layout: default
title: Archivo
---

Archivo
-------

<ol id="archive">
  {% for post in site.posts offset:0 %}
    <li>
      <time datetime="{{ post.date | xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
      <p><a href="{{ post.url }}">{{ post.title }}</a></p>
    </li>
  {% endfor %}
</ol>
{% include footer.html %}

