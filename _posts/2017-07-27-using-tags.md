---
layout: post
current: post
cover:  assets/images/rhythm game main.jpg
navigation: True
title: Tune Of Heart
date: 2017-07-27 08:00:00
tags: [Rhythm game]
class: post-template
subclass: 'post'
author:  An Sung-Hyun
---


<p>[JAVA] Rhythm Game, Tune Of Heart </p>
<p>It is a rhythm game based on Java and it is implemented by utilizing all basic Java technology.</p>
<h2 id="Database">Database</h2>
<p>The database basically has member information and CD key information. Through this, members' personal information, scores, and records will be managed, and Java will link them through certain Java classes.</p>
<p>If you tag a post with both <code>News</code> <em>and</em> <code>Cycling</code> - then it appears in both sections.</p>
<p>Tag archives are like dedicated home-pages for each category of content that you have. They have their own pages, their own RSS feeds, and can support their own cover images and meta data.</p>
<h2 id="theprimarytag">The primary tag</h2>
<p>Inside the Ghost editor, you can drag and drop tags into a specific order. The first tag in the list is always given the most importance, and some themes will only display the primary tag (the first tag in the list) by default. So you can add the most important tag which you want to show up in your theme, but also add a bunch of related tags which are less important.</p>
<p><mark><strong>News</strong>, Cycling, Bart Stevens, Extreme Sports</mark></p>
<p>In this example, <strong>News</strong> is the primary tag which will be displayed by the theme, but the post will also still receive all the other tags, and show up in their respective archives.</p>
<h2 id="privatetags">Private tags</h2>
<p>Sometimes you may want to assign a post a specific tag, but you don't necessarily want that tag appearing in the theme or creating an archive page. In Ghost, hashtags are private and can be used for special styling.</p>
<p>For example, if you sometimes publish posts with video content - you might want your theme to adapt and get rid of the sidebar for these posts, to give more space for an embedded video to fill the screen. In this case, you could use private tags to tell your theme what to do.</p>
<p><mark><strong>News</strong>, Cycling, #video</mark></p>
<p>Here, the theme would assign the post publicly displayed tags of <code>News</code>, and <code>Cycling</code> - but it would also keep a private record of the post being tagged with <code>#video</code>.</p>
<p>In your theme, you could then look for private tags conditionally and give them special formatting:</p>
{% raw %}
<pre><code class="nohighlight">{{#post}}
    {{#has tag=&quot;#video&quot;}}
        ...markup for a nice big video post layout...
    {{else}}
        ...regular markup for a post...
    {{/has}}
{{/post}}
</code></pre>
<p>You can find documentation for theme development techniques like this and many more over on Ghost's extensive <a href="https://themes.ghost.org/">theme documentation</a>.</p>
{% endraw %}
