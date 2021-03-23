---
title: Publications
layout: gridlay
excerpt: Publications.
sitemap: false
permalink: "/publications/"
---

# Publications
### 2021
{% for publi in site.data.publist_21 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>  <em>{{ publi.submit }} </em><br /> 

{% endfor %}

### 2020
{% for publi in site.data.publist_20 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>  <em>{{ publi.submit }} </em><br /> 

{% endfor %}
### 2019 and before
{% for publi in site.data.publist_19 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

{% for publi in site.data.publist_0 %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}
