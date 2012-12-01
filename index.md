---
layout: default
title: Dear Bill Murray
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
  <li>
    <article>
      <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
      <time datetime="{{ post.date }}" pubdate="pubdate">{{ post.date | date_to_string }}</time>
    </article>
  </li>
{% endfor %}
</ul>