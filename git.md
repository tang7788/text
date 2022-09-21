# git是做代码管理的工具，帮助我们记录代码的修改

git的使用
1. 初始化git仓库     git init
2. 添加修改到暂存区   git add path./文件名
3. 提交修改到版本库   git commit -m "描述"

4. 查看工作区的修改   git status
5. 查看提交记录       git log

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>或者git switch <name>

创建+切换分支：git checkout -b <name>或者git switch -c <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>