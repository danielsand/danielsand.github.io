---
layout: post
title: "Mint Linux - Oracle JDK the easy way"
description: "Installing on Mint Linux the Oracle JDK in an easy way"
category: articles
tags: [linux, mint, JDK, PPA]
image:
  feature: korea_fishmarket_2012.jpg
  credit: Daniel Sand
comments: true  
---

I just want to check out some DIA related tool which needs Java.

I'm not a real Java person - i accept the fact that is there and that it's used and that i often need to maintain it form the server side like Tomcats, JBOSS or netty/jetty so i know my way around.  
  
Since Oracle has taken over SUN, it's a hassle to install Orace JDK to your systems.   

There is no download link which is easily usable with wget.  
(OK - there are hacks but often they work only some time and die because oracle invented some new **improved and better oracle-way** strategies and improve/fix the hack) 
  
Some time ago i found a Ubuntu PPA from the **WebUpd8 Team**, which does the trick.   

> Oracle JDK7 itself is not hosted in the PPA because that's not allowed by the new Java license (which is also the reason why it has been removed from the official Ubuntu repositories); the package in the PPA automatically downloads Oracle Java JDK 7 from its official website and installs it on your computer, just like the flashplugin-installer package does.

Link -> https://launchpad.net/~webupd8team/+archive/java

just add the PPA to your Desktop
{% highlight bash %}
sudo add-apt-repository ppa:webupd8team/java
{% endhighlight %}

dont forget like me to update the apt cache :P
{% highlight bash %}
sudo apt-get update
{% endhighlight %}

then choose your JDK from 6,7 or 8 - replace the number and go

{% highlight bash %}
sudo apt-get install oracle-java7-set-default
{% endhighlight %}

dont forget to update you apt cache like me :P

{% highlight bash %}
sudo apt-get update
{% endhighlight %}

and it's done

{% highlight bash %}
java -version
java version "1.7.0_40"
Java(TM) SE Runtime Environment (build 1.7.0_40-b43)
Java HotSpot(TM) 64-Bit Server VM (build 24.0-b56, mixed mode)
{% endhighlight %}

Enjoy :)
