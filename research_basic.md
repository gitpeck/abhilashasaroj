
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
