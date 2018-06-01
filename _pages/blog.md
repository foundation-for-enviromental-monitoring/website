---
permalink: /blog/
title: ffem Blogs
layout: default
---

{% for post in site.posts %}
<p><strong><a href="{{ post.url }}">{{ post.title }}</a></strong><br><small>Posted by <strong>{{ post.author }}</strong> on {{ post.date }}</small><br>{{ post.excerpt }}<br>&nbsp;&nbsp;<a href="{{ post.url }}">Full post</a></p>
{% endfor %}

