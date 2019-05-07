---
layout: page
title: Tags
permalink: /tags/
sitemap:
  priority: 0.7
---
<h1 style="display:inline;">랜덤 태그: </h1>
<h1 style="display:inline;">
    <a href="" id="tagLink"></a>
</h1>
<input type="button" value="다시" onclick="reload();" style="color:#404040;" />
<script type="text/javascript">
	var allTags = [{% for tag in site.tags %}"{{ tag.name | escape }}",{% endfor %}""];
	allTags.pop();
  var tag = document.getElementById("tagLink");
  function reload() {
    var random = Math.floor(Math.random() * allTags.length);
    tag.href = "{{ site.baseurl }}/tags/"+allTags[random];
    tag.innerHTML = allTags[random];
  }
  reload();	
</script>
<ul>
  <li><p><a href="{{ site.baseurl }}/tags/동방">동방</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방_동인지">동방_동인지</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방_동인지／ㄴ이쪽_번역">동방_동인지／ㄴ이쪽_번역</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방_웹코믹">동방_웹코믹</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방_웹코믹／ㄴ이쪽_번역">동방_웹코믹／ㄴ이쪽_번역</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／동인지(백합)">동방／동인지(백합)</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／동인지">동방／동인지</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／동인지／이쪽_번역">동방／동인지／이쪽_번역</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／번역．동인지">동방／번역．동인지</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／번역．웹코믹">동방／번역．웹코믹</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／웹코믹&영상(백합)">동방／웹코믹&영상(백합)</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동방／웹코믹">동방／웹코믹</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/동인지">동인지</a></p></li>
  <li><p><a href="{{ site.baseurl }}/tags/웹코믹">웹코믹</a></p></li>
  <hr>
{% for tag in site.tags %}
  <li>
  	<p>
  	  <a href="{{ site.baseurl }}/tags/{{ tag.name | escape }}">{{ tag.name }}</a>
    </p>
  </li>
{% endfor %}
</ul>