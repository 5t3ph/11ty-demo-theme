---
layout: base.njk
title: Welcome
templateEngineOverride: md, njk
eleventyComputed:
  meta:
    description: "Template level description override"
---

Hello stream viewers!

## My Posts

<ul>
{%- for post in collections.posts -%}
  <li>
    <h3><a href="{{ post.page.url }}">{{ post.data.title }}</a></h3>
    {{ post.content | excerpt }}
  </li>
{%- endfor -%}
</ul>
