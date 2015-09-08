
#git 常用命令记录
参考自：[廖雪峰官网](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

##内容会不定期更新

###**如果各位大大发现有错,欢迎指出**


git init: 创建并初始化一个 git 仓库,接着你就可以往里面塞东西，就像冰箱一样可以往里面塞各种食品;

git add file_name: 添加一个文件到 git 的 暂存区中, file_name 表示一个文件，比如readme.txt, 又或者是 LearnGit.Java 文件等等，需要注意的是不能添加 二进制 文件，像 word 文档里文件;

git status: status 中文翻译为状态，不用猜都知道是查看 git 工作仓库中的状态变化，比如，add 了什么文件，还没 commit 修改后的文件等等;

git log: 这个就是查看往 git 仓库中 commit(提交) 日志信息，如果 git log 信息太多，并且后面还有很多日志信息想退出怎么办呢，这个可以通过按 Q 键退出日志查看;

git commit file_name: 这个命令便是将 git add file_name 命令中添加到暂存区中东西提交到master 分支上或者是新建的分支上，可以将一些修改后，或者是添加新文件提交到 master 分支上，或者提交到你自己新创建的分支上;

git reset --hard HARD^: 这个是 git 中有着后悔药一样神奇的功能，它可以将当前 git 仓库版本回滚到上一个 git 仓库版本，接着就又可以愉快撸代码了;

git reset --hard commit_id:这个命令作用就是回滚到 commit_id git 仓库版本，commit_id 则是 每次 commit， git 都会自动生成一个很长 id 来记载 commit 信息，id 可以用 git log 去查看，当然，你嫌信息多的话，可以用 git log --pretty=oneline 去查看，用了之后你会感到相当的整洁明了;

git branch:这是用来查看git 仓库中分支信息，* 后面跟着一个单词就是你的分支名称;

git checkout -b dev:用来创建一个名为 dev 的 git 分支，当然名称可以根据自己需求所定，创建 dev 分支并切换到dev 分支;

git checkout 分支名称:这个无须多言，用来切换到哪个 git 分支;

git merge 分支名称:如果你当前的分支在 master 上，并且你有一个 dev 的分支，你想将 dev 分支合并到 master 分支上， 那么你便可以用这个命令;

git branch -d 分支名称:当你不要这个分支后，你可以用这个命令去删除这个分支;

git checkout -- <file_name>:当你在 add 之前，而这个时候你又想撤销的话可以用这个命令去撤销你的代码添加到暂存区;

git add .:这个命令则是用来添加多个文件到暂存区中;

git add --all:这个是一次将多个文件夹或者是文件添加到暂存区中;

git remote add (你的github项目地址链接):这个命令则是关联远程仓库到本地上，远程仓库就是github项目地址;

git push -u origin master:把本地的所有内容推送到远程库上，由于第一次推送，所以远程库是空的，所以要加上 -u 参数，origin 就是远程库的名字，master 就是你要推送的分支;

git remote:查看远程库的信息;

git remote -v:查看更加详细远程库的信息;

git pull:把最新的提交从远程库的分支上抓取到本地上;



