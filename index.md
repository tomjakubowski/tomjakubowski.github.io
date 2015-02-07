---
layout: page
title: Hello World!
tagline: Supporting tagline
---

I'm Tom Jakubowski and this is my home on the World Wide Web.  This is where I post
stuff about computer programming and things like that.

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


