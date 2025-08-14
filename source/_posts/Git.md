---
title: Git
date: 2025-05-23 14:40:31
tags:
---

## 新建分支

- git checkout -b <branch-name>

### 基于远程建立分支

- git fetch origin
- git branch --no-track <branch-name> origin/<远程分支>
- git branch <branch-name> <本地分支>
- git checkout --no-track -b <branch-name> origin/<远程分支>

### 分支推上远程

- git push origin <branch-name>

### 拉去远程分支到本地，并跟踪远程分支

- git checkout --track origin/<branch-name>

### 修改分支名

- git branch -m <old-branch-name> <new-branch-name>

### 检测分支是否在远程

- git show-branch origin/<branch-name>

### 删除分支

- git branch -d <branch-name>
- git push origin --delete <branch-name>

### 查看本地分支关联的远程分支

- git config --get branch.<branch-name>.merge
- git config --get branch.<branch-name>.remote

###

## 提交

- git add .
- git commit -m "commit message"
- git commit -m "标题" -m "内容"

## 推送远程分支

- git push
- git push -u origin <branch-name>

## 合并分支

- git merge <branch-name>
- git merge --no-ff <branch-name>
- git config --global merge.ff false
- git config --global --unset merge.ff
- git merge origin/<branch-name>
- git merge --abort
- git commit -F ./.git/MERGE_MSG

## 撤销

- git reset --hard origin/<branch-name>
- git reset --hard HEAD^
- git reset --hard HEAD~3
- git reset --soft HEAD~
