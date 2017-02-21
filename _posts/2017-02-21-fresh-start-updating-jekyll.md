---
layout: post
title: "Fresh Start - updateing to jekyll 3"
description: "just updating jekyll to revive my blog again"
category: articles
tags: [jekyll, update, blog, fresh start]
image:
  credit: Daniel Sand
comments: true
---
After some time i wanted to re-activate my blog again.

{% highlight bash %}
bundle install
{% endhighlight %}

i realized that i hadn't pinned down the versions of gems inside the Gemfile

{% highlight bash %}
jekyll s
Configuration file: /Users/dsa/private/danielsand.github.io/_config.yml
       Deprecation: The 'pygments' configuration option has been renamed to 'highlighter'. Please update your config file accordingly. The allowed values are 'rouge', 'pygments' or null.
       Deprecation: Please change 'use_coderay' to 'enable_coderay' in your configuration file.
Configuration file: /Users/dsa/private/danielsand.github.io/_config.yml
       Deprecation: The 'pygments' configuration option has been renamed to 'highlighter'. Please update your config file accordingly. The allowed values are 'rouge', 'pygments' or null.
       Deprecation: Please change 'use_coderay' to 'enable_coderay' in your configuration file.
            Source: /Users/dsa/private/danielsand.github.io
       Destination: /Users/dsa/private/danielsand.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
       Deprecation: You are using 'kramdown.coderay' in your configuration, please use 'syntax_highlighter_opts' instead.
       Deprecation: You are using 'coderay_line_numbers'. Normalizing to line_numbers.
       Deprecation: You are using 'coderay_line_numbers_start'. Normalizing to line_numbers_start.
       Deprecation: You are using 'coderay_tab_width'. Normalizing to tab_width.
       Deprecation: You are using 'coderay_bold_every'. Normalizing to bold_every.
       Deprecation: You are using 'coderay_css'. Normalizing to css.
  Dependency Error: Yikes! It looks like you don't have pygments or one of its dependencies installed. In order to use Jekyll as currently configured, you'll need to install this gem. The full error message from Ruby is: 'cannot load such file -- pygments' If you run into trouble, you can find helpful resources at http://jekyllrb.com/help/!
  Liquid Exception: pygments in /Users/dsa/private/danielsand.github.io/_posts/2013-10-03-mint-linux-install-oracle-jdk-the-easy-way.md
             ERROR: YOUR SITE COULD NOT BE BUILT:
                    ------------------------------------
                    pygments
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
