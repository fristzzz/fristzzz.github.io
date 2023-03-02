---
title: git notes
date: 2023-03-02 18:47:21
categories: 
    - coding
tags:
---

以前没怎么用git，也就clone，push，add，commit这些，最近两个电脑同步笔记，要用不少git操作。发现以前看的全忘光了，再重新复习一下。

---

# 分支内操作

## 创建仓库, 提交修改

`git init` 在当前目录创建仓库
`git init filename` 在指定目录下创建仓库

`git add .` 将修改添加到暂存区
`git status` 可以查看仓库状态，git会告诉你暂存区有无修改正在等待提交
`git commit -m "some describe"` 将修改提交到目录树，-m参数为日志内容，linux下用单引号，windows下用双引号

如果`git status`告诉你有文件被修改过，用`git diff`可以查看修改内容。


## 版本回退

### 回退

`git log` 可以查看提交日志(commitment log) 
`git log --pretty=oneline` 查看精简版，只有id和提交信息


回退到上一个版本： `git reset --hard HEAD^` 其中 `HEAD^` 即上一个版本
上上个版本为 `HEAD^^`

### 撤销回退

如果回退之后想要撤销回退，使用 `git reflog` 查看head记录
并用 `git reset --hard <id>` 来回到之前的版本