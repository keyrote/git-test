# git笔记
---
## git config
配置个人用户名和邮箱地址
```
$ git config --global user.name "runoob"
$ git config --global user.email test@runoob.com
```
检查已有的配置信息
`git config --list`
```
git config -e    # 针对当前仓库 
$ git config -e --global   # 针对系统上所有仓库
```

## git status
查看仓库当前的状态，显示有变更的文件。
可以列出当前目录所有还没有被git管理的文件和被git管理且被修改但还未提交(git commit)的文件。

## git remote
添加远程源
`git remote add origin *****`
删除远程源
`git remote rm origin`

## git init
初始化git仓库

## git add
提交所有文件至缓存区
`git add .`
添加一个或多个文件到暂存区：
`git add [file1] [file2] ...`
添加指定目录到暂存区，包括子目录：
`git add [dir]`

## git commit
将暂存区内容添加到仓库中。
`git commit -m 说明`

## git log
查看提交历史
```
git log --oneline #查看历史记录的简洁的版本
git log --reverse --oneline #用 --reverse 参数来逆向显示所有日志
git log --author=Linus --oneline #查找指定用户的提交日志
git log -2 #查看后两条
```

## git clone
从现有的git仓库中拷贝项目
```
git clone <repo>
git clone <repo> <directory> #克隆到指定的目录
```
* **repo**:Git 仓库。
* **directory**:本地目录。

## touch
创建文件

