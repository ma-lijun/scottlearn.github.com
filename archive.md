---
layout: page
title: "Archive"
---


<ul class="listing">
{% for post in site.posts %}
  {% capture y %}{{post.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>

<ul class="listing">
{% for ief in site.iefs %}
  {% capture y %}{{ief.date | date:"%Y"}}{% endcapture %}
  {% if year != y %}
    {% assign year = y %}
    <li class="listing-seperator">{{ y }}</li>
  {% endif %}
  <li class="listing-item">
    <time datetime="{{ ief.date | date:"%Y-%m-%d" }}">{{ ief.date | date:"%Y-%m-%d" }}</time>
    <a href="{{ ief.url }}" title="{{ ief.title }}">{{ ief.title }}</a>
  </li>
{% endfor %}
</ul>