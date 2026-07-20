---
title: "News"
layout: default
sitemap: false
permalink: /news/
---

## News

<div class="news-list" markdown="0">
{% for item in site.data.news %}
<div class="news-entry">
  {% if item.photo %}<img src="{{ site.url }}{{ site.baseurl }}/images/{{ item.photo }}" class="news-photo" alt="" loading="lazy">{% endif %}
  <div class="news-body">
    <div class="news-meta">
      <span class="news-date">{{ item.date }}</span>
      {% if item.category %}<span class="news-tag">{{ item.category }}</span>{% endif %}
    </div>
    <h4 class="news-title">{{ item.title }}</h4>
    {% if item.detail %}<p class="news-detail">{{ item.detail }}</p>{% endif %}
  </div>
</div>
{% endfor %}
</div>
