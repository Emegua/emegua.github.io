---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order. <br/>* = equal contribution.
years: [2024, 2023, 2022, 2021]
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<div class="publications">

{% assign sorted_years = page.years | sort: 'reverse' %}
{% for year in sorted_years %}
  <h2>{{ year }}</h2>
  {% bibliography --query @*[year={{ year }}]* %}
{% endfor %}

</div>
