
</section>


<h3 class="archive__subtitle">Recent work</h3>

{% include group-by-array collection=site.posts field="categories" %}

<div class="cf"> 
<div class="grid__wrapper">

{% for category in group_names %}
  <!-- only research -->
  {% if category contains site.research %}
    {% assign posts = group_items[forloop.index0] %}
    {% for post in posts %}
    {% include archive-single.html type="grid" %}
    {% endfor %}
  {% endif %}
{% endfor %}

</div>
</div>

<section class="page__content cf" itemprop="text" markdown="1">

> "Nothing in life is to be feared, it is only to be understood. Now is the time to understand more, so that we may fear less."

<cite>Madame Marie Curie</cite> (1867-1934) 
{: .small}

</section>
