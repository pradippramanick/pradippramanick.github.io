---
layout: page
permalink: /patents/
title: patents
description: Filed and granted patents.
years: [2024,2023,2019]
nav: true
nav_order: 2
---

<!-- _pages/patents.md -->

{% if site.search_enabled %}
<input type="text" id="bibsearch" spellcheck="false" autocomplete="off" class="search bibsearch-form-input" placeholder="Type to filter">
{% endif %}

<div class="publications">

{%- for y in page.years %}
  <h2 class="year">{{y}}</h2>
  {% bibliography -f patents -q @*[year={{y}}]* %}
{% endfor %}

</div>
