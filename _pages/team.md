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
	<li data-target="#carousel" data-slide-to="1"></li>
	<li data-target="#carousel" data-slide-to="2"></li>
 	<li data-target="#carousel" data-slide-to="3"></li>
  	<li data-target="#carousel" data-slide-to="4"></li>
	    
    </ol>

    <!-- Items -->
    <div class="carousel-inner" markdown="0">

	<div class="item active">
            <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/b1.png" alt="Slide 0" />
	    <div class="carousel-caption d-none d-md-block">
    		<p>Group Photo</p>
  	    </div>  
        </div> 

	<div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/b2.png" alt="Slide 1" />
	    <div class="carousel-caption d-none d-md-block">
    		<p>Group Photo</p>
  	    </div>  
        </div> 
	
 	<div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/b3.png" alt="Slide 2" />
	    <div class="carousel-caption d-none d-md-block">
    		<p>Group Photo</p>
  	    </div>  
        </div>   
	  
	<div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/b4.png" alt="Slide 3" />
	    <div class="carousel-caption d-none d-md-block">
    		<p>Group Photo</p>
  	    </div>  
        </div> 
	    
        <div class="item">
            <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/b5.png" alt="Slide 4" />
	    <div class="carousel-caption d-none d-md-block">
    		<p>Group Photo</p>
  	    </div>  
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


## Leader

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

  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
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

{% comment %}
[Full CV (as of April 2024)](CV.pdf) 
	{% endcomment %}

## Members

{% assign number_printed = 0 %}
{% for member in site.data.team_1 %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <br>Office: {{ member.office }}<br>Tel: {{ member.tel }} <br>
  Email: <{{ member.email }}></i>
  <ul style="overflow: hidden">
		
  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}
	
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}
	
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
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
