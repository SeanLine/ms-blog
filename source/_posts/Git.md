---
title: Git
date: 2025-05-23 14:40:31
tags:
---

## 新建分支

- git checkout -b <branch-name>
- git fetch origin
- git checkout -b <branch-name> origin/<远程分支>
- git push origin <branch-name>

## 删除分支

- git branch -d <branch-name>
- git push origin --delete <branch-name>

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
