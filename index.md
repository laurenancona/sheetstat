---
layout: default
title: Data Platform Prototype
---

<br>
The Sustainable Development Goals (SDGs) are an intergovernmental set of aspiration Goals with 169 targets. Cras eu ullamcorper tellus, vitae elementum est. Maecenas eu sem a felis vulputate rhoncus eget nec dolor. Aliquam consectetur augue quis nulla pretium, nec iaculis arcu laoreet. In ut gravida sem. Cras odio lorem, mattis faucibus pellentesque non, convallis sit amet mi. Proin et malesuada dui. Donec gravida faucibus arcu, eget sodales lectus tincidunt ac. 

<section class="goals-list">
{% assign sdg_goals = site.data.sdg_goals %}

{% for goals in sdg_goals %}

{% assign img_path = goals.goal | plus:0 %}

{% if img_path < 10 %}
    {% assign img_path = 0  %}
{% else %}
    {% assign img_path = ''  %}
{% endif %}

<img class="goal-icon" src="{{ site.baseurl }}/assets/TGG_Icon_Color_{{ img_path }}{{ goals.goal }}.png" />

{% endfor %}

</section>

<h2>About the Data Platform Prototype</h2>
Aliquam sed risus nec arcu bibendum porttitor a in urna. Suspendisse pretium felis enim, in hendrerit sapien feugiat vitae. Nulla semper vehicula faucibus. Duis eget sem elementum, tempus tellus at, interdum neque. Donec at ex massa. 

<h2>About the Application</h2>

<p>This is an open source project based on the work of the City of Philadelphia and existing tools including Jekyll, Leaflet.js, and Chartist.js. </p>



[View the original source code](https://github.com/CityOfPhiladelphia/community-health-explorer)

<h5>Download the Data:</h5>

- [Planning Districts]({{ site.basurl }}/_data/planning_district.csv)
- [Racial Disparity]({{ site.basurl }}/_data/racial_disparity.csv)
- [Citywide Over Time]({{ site.basurl }}/_data/citywide_over_time.csv)
- [Top 10 Cities]({{ site.basurl }}/_data/top_10_cities.csv)

<br>

{% include footer.html %}