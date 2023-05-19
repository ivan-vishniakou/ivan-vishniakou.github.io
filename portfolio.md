---
layout: page
title: "Portfolio"
permalink: /portfolio
---

Brief descriptions of my projects. For publicaitons go [here](/publications).

<div>
  {% for post in site.categories.portfolio %}
    {% if post.url %}
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <p>{{post.excerpt}}</p>
        {% if post.content.size > post.excerpt.size %}
		<p><a href="{{ post.url }}">(more...)</a></p>
		{% endif %}
		<p><br></p>
    {% endif %}
  {% endfor %}
</div>