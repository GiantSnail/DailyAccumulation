# Git常用命令

## common CMD
    git pull
    git add -A
    git commit -m "changes"
    git push

## `git clone`克隆仓库
    git clone <远程仓库的地址>

## `git init` 在本地初始化
    git init//在本地初始化git目录，生成.git文件夹

## `git add`添加修改到暂存区
    git add 将文件添加到暂存区，在commit时，将提交到本地仓库
    git add <文件目录>//将指定文件添加到暂存区
    git add -u|--update [<文件路径>] 添加所有修改，删除的文件
    git add -A|--all [<文件路径>] 添加修改，删除，增加的文件到缓存区

## `git commit` 提交修改到本地仓库
    git commit -m "提交的内容描述"//将暂存区的内容提交到本地仓库中

## `git push` 将本地仓库同步到远程仓库
    将本地仓库修改推送到远程仓库中

## `git pull` 拉去远程仓库版本到本地仓库
    git pull//将远程仓库的最新版本合并到本地

## `git log` Log记录
    git log//打印提交记录信息


## 将本地的工程添加到远程仓库

    在本地创建了一个项目,进行了一段时间的开发，想要把项目添加到GitHub，具体操作：
    1. 将本地文件夹初始化为git仓库 `git init`
    2. 将本地修改添加到本地仓库： git add -A
    3. 在GitHub上创建同名仓库
    4. 本地仓库添加远程仓库：git remote add <name> <url>
    5. eg: git remote add master https://github.com/XXX/XXX.git
    6. 将分支合并到主分支：

```
git branch  查看一下分支
git merge master 选择合并的分支
git pull origin main --main-unrelated-histories
git push origin main
```
