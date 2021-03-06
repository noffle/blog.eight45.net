# Quick and Easy READMEs with vmd

> 2015-10-24 08:37:25

The `view` subcommand of `npm` is pretty cool. It will happily print any
property of the package to standard output.

{% highlight bash %}
$ npm view twitter-rss-server dependencies
 
{ configstore: '^1.2.1',
  prompt: '^0.2.14',
  rss-twitter: '0.0.2' }
{% endhighlight %}

This extends to the project's README, too!

{% highlight bash %}
$ npm view prompt readme | head
 
 # prompt [![Build Status](https://secure.travis-ci.org/flatiron/prompt.svg)](http://travis-ci.org/flatiron/prompt)

 A beautiful command-line prompt for node.js

 ## Features

 * prompts the user for input
 * supports validation and defaults
 * hides passwords
{% endhighlight %}

Combine this with the markdown viewer [vmd](http://github.com/yoshuawuyts/vmd), which reads markdown on standard input and creates an Electron window with its parsed output:

{% highlight bash %}
$ npm view prompt readme | vmd
{% endhighlight %}

<center><img src="/static/vmd.png"/></center><br/>

Super handy for referring to a project's documentation without needing to fire
up the browser and go searching.

Happy hacking!

