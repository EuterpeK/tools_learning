1.  创建一个空目录（版本库）
    mkdir name
2.  git init
3.  git add file
    git commit -m "本次提交的说明"
4.  git status
5.  git diff file
    查看具体修改了什么内容与上次相比
6.  git log (--pretty=oneline)
    查看最近到最远的提交日志
7.  git reset --hard HEAD^
    版本回退：  在git中用HEAD表示当前版本，上一个版本用HEAD^来表示
                上上个版本就是HEAD^^或者HEAD~2
8.  git reflog  
    用来记录每一次的命令
9.  工作区：电脑里能看到的目录
    版本库：工作区有一个隐藏的目录".git"，这个是Git的版本库
    add的文件先放到版本库里的暂存区，然后再用commit将暂存区的文件
    全部提交到当前分支中
10. git checkout -- file
    可以丢弃工作区的修改，就是让这个文件回到最近一次git commit或git add的状态
    一种是file自修改后还没有被放到暂存区，那么撤销修改就和回到版本库一模一样的状态
    一种是file已经添加到暂存区后，又做了修改，那么撤销修改就回到添加到暂存区后的状态
    (实际上就是用版本库里的版本替换工作区的版本，不论工作区是修改还是删除)
11. git reset HEAD file
    可以把暂存区的修改撤销掉，重新放回工作区
12. git rm
    git commit
    从版本库里面删除该文件
13. 