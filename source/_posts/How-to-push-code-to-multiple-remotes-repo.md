---
title: How to push code to multiple remotes repo
date: 2022-01-14 17:06:00
tags: Git
---

# 如何在一个项目下给多个远程仓库推送代码？

列举一些可能（一定）会用到的命令：

`git remove -v`，这个命令是用来查看你当前远程的信息的，也就是查看 `git remote` 的信息。

然后使用 `vi .git/config` 查看当前项目的 git 配置；

通常来说我们会在 `origin` 中看到你配置的单个 `url` 和 `pushurl` 路径，_那么我们只需要在 config 文件中添加一栏 pushurl 即可。_
