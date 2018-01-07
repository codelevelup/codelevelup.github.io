---
layout: archive
title: "Sitemap"
permalink: /sitemap/
author_profile: false
---

A list of all the posts and pages found on the site. For you robots out there is an [XML version]({{ "sitemap.xml" | absolute_url }}) available for digesting as well.
<br><br>
<h2 class="archive__subtitle">Menu</h2>
{% for post in site.pages %}
  {% unless post.title == null or post.output == false or post.permalink == "/" or post.permalink == "/404.html" or post.permalink == "/page-archive/" or post.permalink == "/collection-archive/" or post.permalink == "/splash-page/" or post.permalink == "/sitemap/" or post.permalink == "/page-archive/" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}

<br><br>
<h2 class="archive__subtitle">Posts</h2>
{% for post in site.posts %}
  {% include archive-single.html %}
{% endfor %}

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
{% unless collection.output == false or collection.label == "posts" %}
  {% capture label %}{{ collection.label }}{% endcapture %}
  {% if label != written_label %}
  <br><br>
  <h2 class="archive__subtitle">{{ label }}</h2>
  {% capture written_label %}{{ label }}{% endcapture %}
  {% endif %}
{% endunless %}
{% for post in collection.docs %}
  {% unless collection.output == false or collection.label == "posts" %}
  {% include archive-single.html %}
  {% endunless %}
{% endfor %}
{% endfor %}
