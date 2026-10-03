---
layout: post
title:  "Hellow to myblog"
published: false
---

이미지 넣기 : 
![My helpful screenshot](/myblog/assets/images/sicho.png)

파일 추가 : 
... you can [get the PDF](/myblog/assets/file/mydoc.pdf) directly.


url 추가 :
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>