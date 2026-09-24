---
layout: page
title: Activities
subtitle: School activities and resources
permalink: /activities/
---

<div class="post-list">
{% assign items = site.activities | sort: 'date' | reverse %}
{% for activity in items %}
  <article class="tag-entry">
    <h3><a href="{{ activity.url | relative_url }}">{{ activity.title }}</a></h3>
    {% if activity.excerpt %}<div>{{ activity.excerpt | strip_html | truncatewords: 40 }}</div>{% endif %}
    {% if activity.date %}<div class="entry-date"><time datetime="{{ activity.date | date_to_xmlschema }}">{{ activity.date | date: "%B %-d, %Y" }}</time></div>{% endif %}
  </article>
{% endfor %}
</div>
