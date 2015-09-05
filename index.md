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
  {% if paginator.next_page %}
    <a class="pagination-item older" href="{{ paginator.next_page_path | prepend: site.baseurl }}">Older</a>
  {% endif %}
  {% if paginator.previous_page %}
    <a class="pagination-item newer" href="{{ paginator.previous_page_path | prepend: site.baseurl }}">Newer</a>
  {% endif %}
</div>