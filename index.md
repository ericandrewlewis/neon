---
layout: page
slug: homepage
---

<h1 class="post-title" style="text-align: center">Neon</h1>

{% assign menu_items = site.pages | sort:"menu_weight" %}
{% for page in menu_items %}
{% if page.menu_weight == null %} {% continue %} {% endif %}
<h3><a class="page-link" href="{{ page.url | prepend: site.baseurl }}">{{ page.title }}</a></h3>
{% endfor %}
