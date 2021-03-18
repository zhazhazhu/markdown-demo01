# git操作

## 配置你的本地仓库
```javascript
git config --global user.name 你的英文名
git config --global user.email 你的邮箱
git config --global push.default simple
git config --global core.quotepath false
git config --global core.editor "code --wait"
git config --global core.autocrlf input


git commit --amend 
git config --global --list（查看配置）

git init(初始化)

git add 路径（表示哪些文件是要提交的）

.gitignore（表示哪些文件是不需要提交的）
常见的有    node_modules    .Ds_store   .idea   .vscode

*git commit -m 字符串（提交）
    注意：字符串里如果有空格，就要用引号包起来

*git commit -v（能显示我们刚刚改了哪些内容）建议用这个

git log（查看提交的版本）

git reflog（查看所有历史版本

git reset --hard XXXXXX(后面是版本号前六位)作用是切换版本

git branch x（新建一个版本，同时做两个版本，分支）

git branch（查看当前处于哪个分支）

git branch -d x（删除x分支）

git checkout x（切换到新版本分支）

git checkout master（回到旧版本分支）

git merge（合并分支）

git status -sb（查看在你上次提交之后是否有对文件进行再次修改）

git commit

```

