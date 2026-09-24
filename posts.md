---
layout: page
title: Posts
subtitle: News, stories and articles from Sahyadri Connect
permalink: /posts/
---

<div class="post-list">
{% assign items = site.posts | sort: 'date' | reverse %}
{% for post in items %}
  <article class="tag-entry">
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    {% if post.subtitle %}<p>{{ post.subtitle }}</p>{% endif %}
    {% if post.date %}<div class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %-d, %Y" }}</time></div>{% endif %}
  </article>
{% endfor %}
</div>
