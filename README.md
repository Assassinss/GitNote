
#git 常用命令记录
参考自：[廖雪峰官网](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

##一些git学习资料:
[Git Community Book 中文版](http://gitbook.liuhui998.com/index.html)<br>
[Git远程操作详解](http://blog.jobbole.com/71091/)<br>
[Git工作流指南：Forking工作流](http://blog.jobbole.com/76861/)<br>
[开发者日常使用的 Git 命令](http://blog.jobbole.com/54184/)<br>
[如何创建你自己的 Git 服务器](http://blog.jobbole.com/60505/)<br>
[Git分支管理是一门艺术](http://blog.jobbole.com/13916/)<br>

##内容会不定期更新

###**如果你有好的资料想分享可以先fork,然后再pull request**


git init: 创建并初始化一个 git 仓库,接着你就可以往里面塞东西，就像冰箱一样可以往里面塞各种食品;
###add,log,status和commit 操作
git add .:用来添加多个文件到暂存区中;

git add --all:一次将多个文件夹或者是文件添加到暂存区中;

git add file_name: 添加一个文件到 git 的 暂存区中, file_name 表示一个文件，比如readme.txt, 又或者是 LearnGit.Java 文件等等，需要注意的是不能添加 二进制 文件，像 word 文档里文件;

git status: status 中文翻译为状态，不用猜都知道是查看 git 工作仓库中的状态变化，比如，add 了什么文件，还没 commit 修改后的文件等等;

git log: 查看往 git 仓库中 commit(提交) 日志信息，如果 git log 信息太多，并且后面还有很多日志信息想退出怎么办呢，这个可以通过按 Q 键退出日志查看;

git commit file_name: 将 git add file_name 命令中添加到暂存区中东西提交到master 分支上或者是新建的分支上，可以将一些修改后，或者是添加新文件提交到 master 分支上，或者提交到你自己新创建的分支上;
###reset 操作
git reset --hard HARD^: 这个是 git 中有着后悔药一样神奇的功能，它可以将当前 git 仓库版本回滚到上一个 git 仓库版本，接着就又可以愉快撸代码了;

git reset --hard commit_id:这个命令作用就是回滚到 commit_id git 仓库版本，commit_id 则是 每次 commit， git 都会自动生成一个很长 id 来记载 commit 信息，id 可以用 git log 去查看，当然，你嫌信息多的话，可以用 git log --pretty=oneline 去查看，用了之后你会感到相当的整洁明了;
###分支操作
git branch:用来查看git 仓库中分支信息，* 后面跟着一个单词就是你的分支名称;

git checkout -b dev:用来创建一个名为 dev 的 git 分支，当然名称可以根据自己需求所定，创建 dev 分支并切换到dev 分支;

git checkout 分支名称:这个无须多言，用来切换到哪个 git 分支;

git merge 分支名称:如果你当前的分支在 master 上，并且你有一个 dev 的分支，你想将 dev 分支合并到 master 分支上， 那么你便可以用这个命令;

git branch -d 分支名称:当你不要这个分支后，你可以用这个命令去删除这个分支;

git checkout -- <file_name>:当你在 add 之前，而这个时候你又想撤销的话可以用这个命令去撤销你的代码添加到暂存区;
###远程操作
git remote add origin (你的github项目地址链接):关联远程仓库到本地上，远程仓库就是github项目地址;

git push -u origin master:把本地的所有内容推送到远程库上，由于第一次推送，所以远程库是空的，所以要加上 -u 参数，origin 就是远程库的名字，master 就是你要推送的分支;

git remote:查看远程库的信息;

git remote -v:查看更加详细远程库的信息;

git pull:把最新的提交从远程库的分支上抓取到本地上;

git clone (你的github项目的地址链接):从远程仓库中克隆一个到本地上;

git remote show origin:查看远程仓库的状态;

git branch -v:查看远程分支;

git branch -a:查看所有分支;

git merge origin/master:在本地分支上合并远程分支，这个命令表示在当前分支上，合并origin/master;

git fetch <远程主机> <分支名>:将远程主机上的某个分支取回到本地, 例如：git fetch origin master ，就是取回origin 主机上的 master 分支到本地上;
###stash 操作
git stash apply:恢复暂存区的内容;

git stash drop:删除暂存区的内容;

