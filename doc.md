#分支
git branch <分支名>		创建分支
git checkout <分支名>		切换分支
git checkout -b <分支名>	创建分支并切换到该分支
git merge <分支名>		合并分支
git rebase <分支名>		合并分支，实际上在当前分支取出一系列的提交记录，然后在<分支名>放下去。

##HEAD分离
git checkout <提交号>	将HEAD从原本指向分支分离，到指向一个提交记录

##相对引用
git checkout <分支名/HEAD>^		将HEAD指向当前分支的父节点
git checkout <分支名/HEAD>~<数字>	将head相对<分支名>向上移动<数字>位置
git branch -f <分支名> HEAD~<数字>	将<分支名>强制指向HEAD第<数字>级父提交

##撤销变更
git reset HEAD~<数字>			将当前分支移动到HEAD<数字>级父提交
git revert HEAD~<数字>			撤销修改并分享给远程分支，相当增加了一个新提交

##整理提交
git cherry-pick <提交号>		git cherry-pick C2 C4指在HEAD下新增C2 C4提价记录

##交互式的rebase
git rebase -i HEAD～<数字>				会打开一个UI界面，调整提交记录的顺序，删除不想要的提交，合并提交
