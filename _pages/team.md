---
title: People
layout: gridlay
excerpt: 'Team members'
sitemap: false
permalink: "/team/"
---

# Current Group Members

### Group Leader

{% assign number_printed = 0 %}
{% for member in site.data.team_0 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <br>Office: {{ member.office }}<br>Tel: {{ member.tel }}      <br>
		Email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}
		
	</ul>
</div>
	
{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


### PhD Students
{% assign number_printed = 0 %}
{% for member in site.data.team_1 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="28%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>Office: {{ member.office }}<br>Email: {{ member.email }}</i>
  <ul style="overflow: hidden">
		
	</ul>
</div>
	

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

### Master and Undergraduate Students
{% for member in site.data.team_2 %}
  <h4>{{ member.name }}</h4>  <i>{{ member.info }}<br></i>
{% endfor %}
