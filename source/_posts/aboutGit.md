---
title: Git
date: 2021-05-09 18:14:32
tags: tech
---

使用 git reflog 查看操作记录，git log 查看提交记录。

- 版本回退  
  使用 git reset --hard commit_id 来回退版本  
  
- add/commit  
 git add filename: 添加文件到暂存区  
   git commit -m "comments": 提交暂存区文件到版本库  
  
- 关于撤销  
  场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令git checkout -- file。  场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令git reset HEAD <file>，就回到了场景1，第二步按场景1操作。
  
- 删除文件  
命令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。
- 和远程库交互  
  - 把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。如 git push -u origin master
  - 把远程库的内容克隆到本地，用git clone命令。git clone git@github.com:xxxx/xxxx.git

- 查看远端仓库地址
  - git remote -v