---
title: 使用Travis CI自动部署到Github pages上
date: 2017-10-26 17:04:12
tags: Travis CI
---

# 什么是Travis CI

> Travis CI 是目前新兴的开源持续集成构建项目，它与jenkins，GO的很明显的特别在于采用yaml格式，同时他是在在线的服务，不像jenkins需要你本地打架服务器，
简洁清新独树一帜。目前大多数的github项目都已经移入到Travis CI的构建队列中，据说Travis CI每天运行超过4000次完整构建。对于做开源项目或者github的使用者，
如果你的项目还没有加入Travis CI构建队列，那么我真的想对你说out了。

然后根据大佬们的文章
* [使用 Travis CI 自动更新 GitHub Pages](http://notes.iissnan.com/2016/publishing-github-pages-with-travis-ci/)

以及

* [手把手教你使用Travis CI自动部署你的Hexo博客到Github上](http://blog.csdn.net/woblog/article/details/51319364)

就完成了小博客的自动提交部署了。

我的yml设置文件

参考这里[.travis.yml](https://github.com/marzlia/blogCI/blob/master/.travis.yml)

注意的是在这里[Online YAML Parser](http://yaml-online-parser.appspot.com/)可以验证你的yml 文件的正确性。



