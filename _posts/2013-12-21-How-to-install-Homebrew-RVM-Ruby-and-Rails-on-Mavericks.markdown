---
layout: post
title: How to install Homebrew, RVM, Ruby and Rails on Mavericks
tags: [ruby, sinatra, heroku, development, github]
---

### Installing [Homebrew](http://brew.sh/)

{% highlight bash %}
$ ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
$ brew update
$ brew doctor
Your system is ready to brew.
{% endhighlight %}

if you get the message 'Your system is ready to brew.' the installation is successful.

### Installing [RVM](https://rvm.io/) with latest [Ruby](https://www.ruby-lang.org/en/) and [Rails](http://rubyonrails.org/)

{% highlight bash %}
$ \curl -L https://get.rvm.io | bash -s stable --rails --autolibs=enable
$ type rvm | head -1
rvm is a function
$ rvm -v
$ ruby -v
$ rails -v
{% endhighlight %}

it's necessary to quit and relaunch Terminal.





