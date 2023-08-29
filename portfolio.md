---
layout: page
title: "Portfolio"
permalink: /portfolio
---
{%- assign date_format = site.minima.date_format | default: "%b %-d, %Y" -%}
Brief descriptions of my projects. For publicaitons go [here](/publications).

<ul class="post-list">
  {% for post in site.categories.portfolio %}
    {% if post.url %}
        <h3><span class="post-meta">{{ post.date | date: date_format }}</span><br>
          {% if post.content.size > post.excerpt.size %}
          <a href="{{ post.url }}">{{ post.title }}</a>
          {% else %}
          <p>{{ post.title }}</p>
          {% endif %}
        </h3>
        <p>{{post.excerpt}}</p>
        {% if post.content.size > post.excerpt.size %}
		        <p><a href="{{ post.url }}">(more...)</a></p>
		    {% endif %}
    {% endif %}
  {% endfor %}
</ul>