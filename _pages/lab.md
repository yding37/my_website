---
layout: page
permalink: /lab/
title: Lab
description: 
nav: true
nav_order: 1
people_categories: [Doctoral, Masters, Undergraduate, Visiting Researcher]
horizontal: true
---
<div style="text-align: center">
        {% include figure.html path="assets/img/lab-pc-building-2023.jpeg" class="img-fluid rounded z-depth-1" width="75%" %}
    </div>
<div class="caption">
    Students building our new server in 2023!
</div>
<!-- 
<!-- ### PhD Students -->
<!-- Uthman Jinadu (PhD, started Fall 2022)\
Anjila Budathoki (PhD, starting Fall 2023) -->

<!-- ### Masters Students -->
<!-- Jesse Annan (MS, started Fall 2022) -->

<!-- ### Undergraduate Students -->
<!-- Preetham Thelluri (BS, Class of 2024) -->


<div class="projects">
  <!-- Display categorized projects -->
  {%- for category in page.people_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_people = site.lab | where: "category", category -%}

  {%- if categorized_people %}
  {%- assign sorted_people = categorized_people | sort: "importance" %}
  <!-- Generate cards for each project -->
  <div class="container row g-1">
    {%- for person in sorted_people -%}
    <!-- <div class="row g-1"> -->
    <div class="float-left col-md-6">
      {% include people_horizontal.html %}
    </div>
    {%- endfor %}
  </div>
  {% endif %}
  {% endfor %}
</div>



