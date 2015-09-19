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

<div id="disqus_thread"></div>
<script type="text/javascript">
/* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */
var disqus_shortname = 'theruqahproject'; // required: Zeynep Akay
var disqus_identifier = '{{ post.permalink }}';
/* * * DON'T EDIT BELOW THIS LINE * * */
(function() {
var dsq = document.createElement('script'); dsq.type = 'text/javascript'; dsq.async = true;
dsq.src = '//' + disqus_shortname + '.disqus.com/embed.js';
(document.getElementsByTagName('head')[0] || document.getElementsByTagName('body')[0]).appendChild(dsq);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="http://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
