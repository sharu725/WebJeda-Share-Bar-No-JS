---
layout: default
---



<div class="share-box">
<h5>Share this:</h5>

<a class="f" href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-facebook-official fa"></i><span> facebook</span></a>

<a class="t" href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter fa"></i><span> twitter</span></a>
        
<a class="g" href="https://plus.google.com/share?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-google-plus fa"></i><span> google</span></a>
        
<a class="r" href="http://www.reddit.com/submit?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-reddit fa"></i><span> reddit</span></a>

<a class="l" href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{site.baseurl}}{{ page.url }}&title={{ page.title }}&summary={{ page.desc }}&source=webjeda" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-linkedin fa"></i><span> linkedin</span></a>                         

<a class="e" href="mailto:?subject={{ page.title }}&amp;body=Check out this site {{ site.url }}{{site.baseurl}}{{ page.url }}"><i class="fa fa-envelope fa"></i><span> email</span></a>                          
</div>


## How do they get the URL of current page?
The links are built using liquid code. They look for current page URL and insert into the share link. So doesn't matter where you place them, they work!

## Code

{% highlight html %}
{% raw %}
/* Call Fontawesome in the head section or in the location where you place the share bar */
<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">

<div class="share-box">
<h5>Share this:</h5>

<a class="f" href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-facebook-official fa"></i><span> facebook</span></a>

<a class="t" href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter fa"></i><span> twitter</span></a>
        
<a class="g" href="https://plus.google.com/share?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-google-plus fa"></i><span> google</span></a>
        
<a class="r" href="http://www.reddit.com/submit?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-reddit fa"></i><span> reddit</span></a>

<a class="l" href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{site.baseurl}}{{ page.url }}&title={{ page.title }}&summary={{ page.desc }}&source=webjeda" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-linkedin fa"></i><span> linkedin</span></a>

<a class="e" href="mailto:?subject={{ page.title }}&amp;body=Check out this site {{ site.url }}{{site.baseurl}}{{ page.url }}"><i class="fa fa-envelope fa"></i><span> email</span></a>                          
</div>
{% endraw %}
{% endhighlight %}

## Style
Use a style that suits your needs. Here is what I have used.

{% highlight css %}

.share-box a {
  display: inline-block;
  -webkit-box-shadow: 0 0 1px #777;
  box-shadow: 0 0 1px #777;
  padding: 5px 12px;
  margin-right: 5px;
  margin-bottom: 5px;
  text-decoration: none; }
  .share-box a:hover {
    text-decoration: none;
    -webkit-transition: background-color 200ms linear;
    -ms-transition: background-color 200ms linear;
    transition: background-color 200ms linear; }

.f {
  color: #3b5998; }
  .f:hover {
    color: #fff;
    background-color: #3b5998; }

.t {
  color: #4099FF; }
  .t:hover {
    color: #fff;
    background-color: #4099FF; }

.g {
  color: #d34836; }
  .g:hover {
    color: #fff;
    background-color: #d34836; }

.r {
  color: #ff5700; }
  .r:hover {
    color: #fff;
    background-color: #ff5700; }

.l {
  color: #0077b5; }
  .l:hover {
    color: #fff;
    background-color: #0077b5; }

.e {
  color: #444444; }
  .e:hover {
    color: #fff;
    background-color: #444444; }

{% endhighlight %}


## A complete html file 

{% highlight html %}
{% raw %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Webjeda Sharebar</title>
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
</head>
<body>
    
 <div class="share-box">
<h5>Share this:</h5>

<a class="f" href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-facebook-official fa"></i><span> facebook</span></a>

<a class="t" href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter fa"></i><span> twitter</span></a>
        
<a class="g" href="https://plus.google.com/share?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-google-plus fa"></i><span> google</span></a>
        
<a class="r" href="http://www.reddit.com/submit?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-reddit fa"></i><span> reddit</span></a>

<a class="l" href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{site.baseurl}}{{ page.url }}&title={{ page.title }}&summary={{ page.desc }}&source=webjeda" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-linkedin fa"></i><span> linkedin</span></a>

<a class="e" href="mailto:?subject={{ page.title }}&amp;body=Check out this site {{ site.url }}{{site.baseurl}}{{ page.url }}"><i class="fa fa-envelope fa"></i><span> email</span></a>                          
</div> 
 
    
<style>

.share-box a {
  display: inline-block;
  -webkit-box-shadow: 0 0 1px #777;
  box-shadow: 0 0 1px #777;
  padding: 5px 12px;
  margin-right: 5px;
  margin-bottom: 5px;
  text-decoration: none; }
  .share-box a:hover {
    text-decoration: none;
    -webkit-transition: background-color 200ms linear;
    -ms-transition: background-color 200ms linear;
    transition: background-color 200ms linear; }

.f {
  color: #3b5998; }
  .f:hover {
    color: #fff;
    background-color: #3b5998; }

.t {
  color: #4099FF; }
  .t:hover {
    color: #fff;
    background-color: #4099FF; }

.g {
  color: #d34836; }
  .g:hover {
    color: #fff;
    background-color: #d34836; }

.r {
  color: #ff5700; }
  .r:hover {
    color: #fff;
    background-color: #ff5700; }

.l {
  color: #0077b5; }
  .l:hover {
    color: #fff;
    background-color: #0077b5; }

.e {
  color: #444444; }
  .e:hover {
    color: #fff;
    background-color: #444444; }
</style>   
</body>
</html>
{% endraw %}
{% endhighlight %}


[Read the article](https://blog.webjeda.com/share-buttons-jekyll/)

[Fork](https://github.com/sharu725/webjeda-sharebar)