---
layout: default
---

{% assign img_number = 1 %}{% for galeria in site.data.galerias %}<div class="section">{% for image in site.static_files %}{% assign imgpath = 'photos/' | append: galeria.diretorio %}{% if image.path contains imgpath %}{% assign img_number = img_number | plus: 1 %}<div class="slide" id="{{galeria.diretorio | append: img_number}}"></div>{% endif %}{% endfor %}</div>{% endfor %}
