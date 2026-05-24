---
layout: default
---

<div class="post-list">
{% for post in site.posts %}
  <div class="post-item">
    <h3><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h3>
    <div class="post-meta">
      {{ post.date | date: "%Y 年 %m 月 %d 日" }}
      {% if post.categories %}
        · {{ post.categories | join: " / " }}
      {% endif %}
    </div>
    {% if post.content %}
      <div class="post-excerpt">
        {{ post.content | strip_html | truncate: 120 }}
      </div>
    {% endif %}
  </div>
{% endfor %}
</div>
