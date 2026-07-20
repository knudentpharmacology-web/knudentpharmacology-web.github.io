---
title: "News"
layout: default
sitemap: false
permalink: /news/
---

## News

<div class="section-card" markdown="0">
<div class="news-list">
{% for item in site.data.news %}
<div class="news-entry{% if item.photo %} has-photo{% endif %}">
  {% if item.photo %}<img src="{{ site.url }}{{ site.baseurl }}/images/{{ item.photo }}" class="news-photo" alt="" loading="lazy">{% endif %}
  <div class="news-body">
    <div class="news-meta">
      <span class="news-date">{{ item.date | date: "%Y. %m" }}</span>
      {% if item.category %}<span class="news-tag">{{ item.category }}</span>{% endif %}
    </div>
    <h4 class="news-title">{{ item.title }}</h4>
    {% if item.detail %}<p class="news-detail">{{ item.detail }}</p>{% endif %}
  </div>
</div>
{% endfor %}
</div>
</div>
