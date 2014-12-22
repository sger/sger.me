---
layout: post
title: Use the Raspberry Pi as a private Git Server
tags: [ruby, sinatra, heroku, development, git, raspberrypi]
---

### Create new User and Group

{% highlight bash %}
$ adduser --system --shell /bin/bash --gecos 'git version control by Raspberry Pi' --group --home /home/git git
{% endhighlight %}
you can choose your own directory for example in my pi i'm hosting all the git projects under /mnt/git just replace /home/git with your path.

### Change the password for the user

{% highlight bash %}
$ passwd git
{% endhighlight %}

next step switch users with

{% highlight bash %}
$ su git
{% endhighlight %}

let's create an empty Git repository under /home/git

{% highlight bash %}
$ cd /home/git
$ mkdir repo.git
$ cd repo.git
$ git --bare init
{% endhighlight %}
push some to git repository

{% highlight bash %}
$ cd repo
$ git remote add pi git@yourserver:/home/git/repo.git
$ git add .
$ git commit -m "Initial Commit"
$ git push pi master
{% endhighlight %}

if you want to clone your git project into another machine type

{% highlight bash %}
$ git clone git@yourserver:/home/git/repo.git
{% endhighlight %}





