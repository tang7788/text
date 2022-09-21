# git是做代码管理的工具，帮助我们记录代码的修改

git的使用
1. 初始化git仓库     git init
2. 添加修改到暂存区   git add path./文件名
3. 提交修改到版本库   git commit -m "描述"

4. 查看工作区的修改   git status
5. 查看提交记录       git log [--graph --pretty=oneline --abbrev-commit]

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>或者git switch <name>

创建+切换分支：git checkout -b <name>或者git switch -c <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>
gggg
hhhh
ppp
合并分支 git merge --no-ff -m "merge with no-ff" <name>
合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并。

# 远程库
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；
关联后，使用命令git push -u origin master第一次推送master分支的所有内容；
此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改；
git remote -v 查看远程库信息
git remote rm origin 删除远程库(解除了本地和远程的绑定关系)
如果推送失败，先用git pull把最新的提交从origin/dev抓下来，然后，在本地合并，解决冲突，再推送

* 本地新建的分支如果不推送到远程，对其他人就是不可见的；
* 从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；
* 在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；
* 建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；
* 从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。
# 从远程库克隆一个本地库
git clone git@github.com:michaelliao/gitskills.git