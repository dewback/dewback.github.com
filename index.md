---
layout: default
title: Home
---

Referencias
-----------

Algunas referencias mientras sale algo interesante acá.

* Website: [fabianarias.com][web]
* Twitter: [@dewback][twit]
* Blog: [dewback.cl][blog]

[web]: http://fabianarias.com
[twit]: http://twitter.com/dewback
[blog]: http://www.dewback.cl

<article>
  <time datetime="{{ site.posts.first.date | xmlschema }}">{{ site.posts.first.date | date: "%d %b" }}</time>
  <h2><a href="{{ site.posts.first.url }}">{{ site.posts.first.title }}</a></h2>
  {{ site.posts.first.content }}
</article>
<hr>
<h2>Archivo</h2>
<ol id="archive">
  {% for post in site.posts offset:1 %}
    <li>
      <time datetime="{{ post.date | xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
      <p><a href="{{ post.url }}">{{ post.title }}</a></p>
    </li>
  {% endfor %}
</ol>
{% include footer.html %}
