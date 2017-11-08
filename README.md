# git-use
熟悉git使用的 练习仓库

是目前世界最先进的 分布式    版本控制系统 linux花了两周时间写的git 

分布式：
去中心化，没有中心服务器，每个人的机器上都是一个完整的库，没有权威人人平等，

版本控制系统： 
备份（记录多个版本文件的功能），记录操作时间线（查看历史操作，进行版本的回滚和前进），多端共享代码，‘自动’合并（解决多人开发冲突问题）。

将需要进行进行版本控制的文件目录叫做仓库repository

#工作区 	--->  缓存区   ---->本地仓库

git init 创建一个本地 git仓库
git clone [url]  克隆远成仓库
git add [index.html]   把工作区的index.html 推到缓存区
git add . 把工作区提交到缓存区 
git commit -m’message’ --author==’name’<Email>快照 传到本地仓库  每次快照提供一个ID
git log  查看最近找到最远仓库的文件信息
git reflog 查看版本号
git status 查看当前git 缓存区 
git diff 查看文件具体修改了哪里
git reset --hard HEAD^   回退到上次 commit  几个＾回退几次
git reset --hard ID      回退到此id时
git reset --hard bdeacd
git checkout --read.txt 工作区回复到最近一次commit  只能恢复手动误删 不能还原指						令删除
git checkout -b dev  创建的分支并且换到此分支  已有分支切换 不写 -b
git rm index.css  git指令删除index.css
git merge dev 把dev分支合并到master
在分支上边写代码 commit到master
git push  -u origin master:master  将本地仓库的master推到git上的master

原理 新建dev分支  就有一个dev指针指向新的分支   commit 之后 dev指针后移 
分支和muster合并 是muster的指针 指向最git后的仓库

$ ssh-keygen -t rsa -C "1643960119@qq.com"			生成ssh密匙
添加到 github 的setting -  
git pull origin master 将远master拉到本地 确保不再push的之前远程master有改变
git fetch origin dev:dev    将远程的dev分支搬运到本地的dev分支
大公司多人开发 push 到 自己的远程仓库 然后branch 里面提交给contributer
新建分支 gh-pages 
在网页输入																															  96weibin.github.io/player/index.html 就可以访问了



设置email
$ git config --global user.email "gudujianjsk@gmail.com"
查看是否有ssh密匙
cd~/ssh
生成密匙	可不设置密码
$ ssh-keygen -t rsa -C "gudujianjsk@gmail.com"
得到两个文件    id_rsa 和 id_rsa.pub
打开id_rsa.pub添加密匙至github  new-ssh-key




git init 
git add .
git commit -m “first commit”
git remote add origin http://github.********
git push -u origin master


先把本地的add 和 commit  再把pull一下  这时就完成自动合并   合并之后在 push  之后再改写   进度 .md