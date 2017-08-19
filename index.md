---
layout: default
---



<div class="share-box">
<h5>Share this:</h5>
<a href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-facebook-official fa"> facebook</i></a>
        <a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter fa"> twitter</i></a>
        <a href="https://plus.google.com/share?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-google-plus fa"> google</i></a>
        <a href="http://www.reddit.com/submit?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-reddit fa"> reddit</i></a>                           <a href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{site.baseurl}}{{ page.url }}&title={{ page.title }}&summary={{ page.desc }}&source=webjeda" onclick="window.open(this.href, 'mywin',
'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-linkedin fa"> linkedin</i></a>                         <a href="mailto:?subject={{ page.title }}&amp;body=Check out this site {{ site.url }}{{site.baseurl}}{{ page.url }}"><i class="fa fa-envelope fa"> email</i></a>                          
</div>


## How do they get the URL of current page?
The links are built using liquid code. They look for current page URL and insert into the share link. So doesn't matter where you place them, they work!

## Code

{% highlight html %}
/* Call Fontawesome in the head section or in the location where you place the share bar */
<link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">

<div class="share-box"> 
    <h5>Share this:</h5>
    /* Facebook button */
    <a href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-facebook-official fa"> facebook</i></a>
     
    /* Twitter button */             
    <a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter fa"> twitter</i></a>
     
    /* Google button */       
    <a href="https://plus.google.com/share?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-google-plus fa"> google</i></a>
    
    /* Reddit button */        
    <a href="http://www.reddit.com/submit?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-reddit fa"> reddit</i></a>    
    
    /* LinkedIn button */
    <a href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{site.baseurl}}{{ page.url }}&title={{ page.title }}&summary={{ page.desc }}&source=webjeda" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-linkedin fa"> linkedin</i></a>
    
    /* eMail button */                         
    <a href="mailto:?subject={{ page.title }}&amp;body=Check out this site {{ site.url }}{{site.baseurl}}{{ page.url }}"><i class="fa fa-envelope fa"> email</i></a>  
                            
</div>
{% endhighlight %}

## Style
Use a style that suits your needs. Here is what I have used.

{% highlight css %}
.share-box p {
    margin: 0;
}

.share-box .fa {
    -webkit-box-shadow: 0 0 1px #777;
    box-shadow: 0 0 1px #777;
    padding: 5px 12px;  
}
.share-box .fa:hover {
    -webkit-box-shadow: 0 0 4px #777;
    box-shadow: 0 0 4px #777;
}


.share-box .fa-facebook-official {
    color: #3b5998;
}
.share-box .fa-facebook-official:hover {
    background-color: #3b5998;
    color:white;
}

.share-box .fa-google-plus {
    color: #d34836;
}
.share-box .fa-google-plus:hover {
    background-color: #d34836;
    color: white;
}

.share-box .fa-linkedin {
    color: #0077b5;
}
.share-box .fa-linkedin:hover {
    background-color: #0077b5;
    color: white;
}

.share-box .fa-envelop {
    color: #444444;
}
.share-box .fa-envelope:hover {
    background-color: #444444;
    color: white;
}


.share-box .fa-reddit {
    color: #ff5700;
}
.share-box .fa-reddit:hover {
    background-color: #ff5700;
    color: white;
}


.share-box .fa-twitter {
    color: #4099FF;
}
.share-box .fa-twitter:hover {
    background-color: #4099FF;
    color: white;
}



{% endhighlight %}


## A complete html file 

{% highlight html %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Webjeda Sharebar</title>
    <link href="https://maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
</head>
<body>
    
 <div class="share-box"> 
    <p>Share this:</p>
    /* Facebook button */
    <a href="https://www.facebook.com/sharer/sharer.php?u={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-facebook-official fa"> facebook</i></a>
     
    /* Twitter button */             
    <a href="https://twitter.com/intent/tweet?text={{ page.title }}&url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;"><i class="fa fa-twitter fa"> twitter</i></a>
     
    /* Google button */       
    <a href="https://plus.google.com/share?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-google-plus fa"> google</i></a>
    
    /* Reddit button */        
    <a href="http://www.reddit.com/submit?url={{ site.url }}{{site.baseurl}}{{ page.url }}" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=900,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-reddit fa"> reddit</i></a>    
    
    /* LinkedIn button */
    <a href="https://www.linkedin.com/shareArticle?mini=true&url={{ site.url }}{{site.baseurl}}{{ page.url }}&title={{ page.title }}&summary={{ page.desc }}&source=webjeda" onclick="window.open(this.href, 'mywin',
    'left=20,top=20,width=500,height=500,toolbar=1,resizable=0'); return false;" ><i class="fa fa-linkedin fa"> linkedin</i></a>
    
    /* eMail button */                         
    <a href="mailto:?subject={{ page.title }}&amp;body=Check out this site {{ site.url }}{{site.baseurl}}{{ page.url }}"><i class="fa fa-envelope fa"> email</i></a>  
                            
</div>   
 
    
<style>

.share-box p {
    margin: 0;
}

.share-box .fa {
    -webkit-box-shadow: 0 0 1px #777;
    box-shadow: 0 0 1px #777;
    padding: 5px 12px;  
}
.share-box .fa:hover {
    -webkit-box-shadow: 0 0 4px #777;
    box-shadow: 0 0 4px #777;
}


.share-box .fa-facebook-official {
    color: #3b5998;
}
.share-box .fa-facebook-official:hover {
    background-color: #3b5998;
    color:white;
}

.share-box .fa-google-plus {
    color: #d34836;
}
.share-box .fa-google-plus:hover {
    background-color: #d34836;
    color: white;
}

.share-box .fa-linkedin {
    color: #0077b5;
}
.share-box .fa-linkedin:hover {
    background-color: #0077b5;
    color: white;
}

.share-box .fa-envelop {
    color: #444444;
}
.share-box .fa-envelope:hover {
    background-color: #444444;
    color: white;
}


.share-box .fa-reddit {
    color: #ff5700;
}
.share-box .fa-reddit:hover {
    background-color: #ff5700;
    color: white;
}


.share-box .fa-twitter {
    color: #4099FF;
}
.share-box .fa-twitter:hover {
    background-color: #4099FF;
    color: white;
}



</style>   
    
</body>
</html>
{% endhighlight %}


[Read the article](https://blog.webjeda.com/share-buttons-jekyll/)

[Fork](https://github.com/sharu725/webjeda-sharebar)