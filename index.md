---
layout: default
title: Home
---

<div class="blog-index">  
  {% assign post = site.posts.first %}
  {% assign content = post.content %}
    <h1 class="post-title">{{ post.title }}</h1>
  <div class="post-author">By {{post.author}}</h2>&nbsp;&nbsp;|&nbsp;&nbsp;{{ post.date | date_to_string }}</div>

  {{content}}

</div>

<div class="pagination">
{% for post in site.posts offset:1 limit:1 %}
	<a class="pagination-item older" href="{{ post.url | prepend: site.baseurl }}">Older</a>
{% endfor%}
</div>