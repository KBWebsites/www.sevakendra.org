---
title: Gallery
layout: default
image_width: 146
image_height: 110
---
<div class="gallery-images">
    {% for i in (1..30) %}
        {% capture img_url %}//i{% cycle '0', '1', '2' %}.wp.com/{{site.domain}}/files/{{i}}.jpg{% endcapture %}
        <a rel="gallery" class="fancybox" href="{{img_url}}"><img src="{{img_url}}?resize={{page.image_width}},{{page.image_height}}" alt="" width="{{page.image_width}}" height="{{page.image_height}}" /></a>
    {% endfor %}
</div>
<script src="//cdnjs.cloudflare.com/ajax/libs/fancybox/2.1.5/jquery.fancybox.min.js"></script>
<script>$(document).ready(function(){$(".fancybox").fancybox()})</script>