---
layout: page
title: ಸಂಗ್ರಹ
permalink: /archive.html
---
<p>ಈ ವರೆಗೆ ನಲ್ಲಿಕಾಯಿ ಅಂಗಳದಲ್ಲಿ ಪ್ರಸಾರವಾದ ಎಲ್ಲಾ ಲೇಖನಗಳೂ ಇಲ್ಲಿವೆ. ಓದಿ ಆನಂದಿಸಿ. ಲೇಖನಗಳು ಬೇಗನೆ ನಿಮ್ಮ ಕೈ ಸೇರಲು <a href="https://feedburner.google.com/fb/a/mailverify?uri=articlesnallikayi&amp;loc=en_US" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;">ಚಂದಾದಾರರಾಗಿ</a></p><br>
<section id="archive">
  <h2><i class="fa fa-leanpub fa-2x"></i> ಈ ವರ್ಷದ ಬರಹಗಳು</h2>
{% for post in site.posts %}
  {% unless post.next %}
  <ul class="this">
  {% else %}
  {% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
  {% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
  {% if year != nyear %}
  </ul>
  <h2>{{ post.date | date: '%Y' }}</h2>
  <ul class="past">
  {% endif %}
  {% endunless %}
    <li><time>{{ post.date | date:"%d %b" }}</time>&nbsp;<a href="{{ post.url }}">{{ post.title }}</a></li>
{% endfor %}
  </ul>
</section>