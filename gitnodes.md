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

## git push
从将本地的分支版本上传到远程并合并
```
git push <远程主机名> <本地分支名>:<远程分支名>
git push <远程主机名> <本地分支名> #如果本地分支名与远程分支名相同，则可以省略冒号
git push origin master
```

## git log
查看提交历史
```
git log --oneline #查看历史记录的简洁的版本
git log --reverse --oneline #用 --reverse 参数来逆向显示所有日志
git log --author=Linus --oneline #查找指定用户的提交日志
git log -2 #查看后两条
```

## git rm
删除文件（remove）
```
git rm <file>
git rm -f runoob.txt #如果删除之前修改过并且已经放到暂存区域的话，则必须要用强制删除选项 -f。
git rm --cached <file>  #如果想把文件从暂存区域移除，但仍然希望保留在当前工作目录中
```

## git mv
用于移动或重命名一个文件、目录或软连接。
```
git mv [file] [newfile]
git mv -f [file] [newfile] #如果新但文件名已经存在，但还是要重命名它，可以使用 -f 参数
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

## git checkout
撤回修改的操作
`git checkout -- <filename>`

## git reset
撤销本地提交的commit
用于回退版本，可以指定退回某一次提交的版本
```
git reset [--soft | --mixed | --hard] [HEAD]
git reset HEAD^            # 回退所有内容到上一个版本，^括号代表回退数量 或者用~加数字 
git reset HEAD^ hello.php  # 回退 hello.php 文件的版本到上一个版本  
git  reset  052e           # 回退到指定版本
git reset --soft HEAD~1    #最近的一次提交撤回到缓存区
```
* –hard 参数会删除回退点之前的所有信息

## git tag
打上标签
`$ git tag -a v1.0  #-a 选项意为"创建一个带注解的标签"`、
追加标签
`git tag -a v0.9 85fc7e7 #后面为commitId`
删除标签
`git tag -d v1.0`

## git branch
创建分支
`git branch (branchname)`
切换分支
`git checkout (branchname)`
删除分支，不能删除当前所在的分支
`git branch -d (branchname)`
创建并切换到所创建的分支
`git checkout -b test`

## git merge
合并分支到当前分支
`git merge (branchname)`
冲突时保留当前分支的代码
`git merge --abort`




