+++
author = "David Elvers"
title = "Setup Blog with Hugo"
date = "2019-03-05"
description = "Guide to setup a static website as blog with hugo and github actions as deployment."
categories = [
    "CI/CD"
]
tags = [
    "hugo",
    "github",
    "k3s",
    "en"
]
+++
In the last years the trend is to use static pages especialiy when there is no need for dynamic content. For me the complexity of hosting a cms just to provide you this blog, doesn't make sense. So I'm a big fan of html generators like hugo. The idea to write the content in markdown, commit the changes and push them to a repository is for me more desirable then hosting wordpress with a database and worring about new security flaws.
## Getting started with Hugo
The simplest way to use hugo, download/install it for your system, create a site, add a theme, add a post and run the integrated server to see your changes in realtime. Just folow the [Quick Start](https://gohugo.io/getting-started/quick-start/). Hugo is very flexible so read the README of the theme, because you often have to set special setttings get the theme working. In my case I had the problem that my theme needed a newer version of hugo than my linux distro provided, so I created a [container](https://github.com/delvers/hugo/pkgs/container/hugo) with the latest hugo version.
## The Hosting
In my case the hosting done by one node with k3s. So the plan is to create a container 