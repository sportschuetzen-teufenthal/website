---
permalink: /vorstand/
---

<div class="feature__wrapper">

{% for staff_member in site.vorstand %}

    <div class="feature__item--left">
      <div class="archive__item">
          <div class="archive__item-teaser">
            <img src="{{ staff_member.image | relative_url }}" alt="">
          </div>

        <div class="archive__item-body">
            <h2 class="archive__item-title">{{ staff_member.name }}</h2><b>{{ staff_member.position }}</b>
            <div class="archive__item-excerpt">
              {{ staff_member.content | markdownify }}
            </div>
        </div>
      </div>
    </div>
  {% endfor %}

</div>
