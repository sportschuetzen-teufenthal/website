---
permalink: /goenner/
---

<div class="feature__wrapper">

{% for goenner in site.goenner %}

    <div class="feature__item--left">
      <div class="archive__item">
          <div class="archive__item-teaser">
            <img src="{{ goenner.image | relative_url }}" alt="">
          </div>

        <div class="archive__item-body">
            <h2 class="archive__item-title">{{ goenner.name }}</h2>
            <div class="archive__item-excerpt">
              {{ goenner.content | markdownify }}
            </div>
        </div>
      </div>
    </div>
  {% endfor %}

</div>
