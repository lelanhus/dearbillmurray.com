---
layout: default
---
{% assign first_post = site.posts.first %} 
{{ first_post.content }}

<div class="signature">
  <p>
    Thanks,
  </p>
  <p>
    The guy that wrote this.
  </p>
</div>
<hr />
<ul class="posts">
{% for post in site.posts offset:1 %}
  <li>{{ post.date | date_to_string }} &raquo; <a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
</ul>