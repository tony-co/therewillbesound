---
title:
subtitle:
navigations: main
---

{% for post in carew.posts|reverse %}
<a href="{{ carew.relativeRoot }}/{{ post.path }}">
<h1>{{ post.title }}</h1>
</a>
<article>
<p class="text-muted">
<span class="glyphicon glyphicon-calendar"></span>
{{ post.metadatas.date|date('M jS, Y') }}
</p>
{{ post.body|raw }}
<p class="go-full-post">
<a href="{{ carew.relativeRoot }}/{{ post.path }}">
Go to full post to share and comment
</a>
</p>
</article>
{% endfor %}
