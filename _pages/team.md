---
title: People
layout: gridlay
excerpt: 'Team members'
sitemap: false
permalink: "/team/"
---


<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="5000" data-pause="hover" >
	
    <!-- Menu -->
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
	    
    </ol>

    <!-- Items -->
    <div class="carousel-photo-inner" markdown="0">

        <div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/gp2021.jpg" alt="Slide 1" />
        </div>
        
    </div>
  <a class="left carousel-control" href="#carousel" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>


## Group Leader

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

## Current Group Members

{% assign number_printed = 0 %}
{% for member in site.data.team_1 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="28%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>Email: {{ member.email }}</i>
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

### Master and Undergraduate Students
{% for member in site.data.team_2 %}
  <h5>{{ member.name }},       <i>{{ member.info }}</i></h5>
{% endfor %}

### Alumni
{% for member in site.data.team_3 %}
  <h5>{{ member.name }},       <i>{{ member.info }},      Now: {{ member.now }}</i></h5>
{% endfor %}
