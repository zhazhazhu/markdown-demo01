# GitHub操作

ssh-keygen -t rsa -b 4096 -C 你的邮箱\
cat ~/.ssh/id_rsa.pub （得到公钥内容）\
ssh -T git@github.com

## 上传到GitHub：
    git remote add origin git@xxxxxxx
    git push -u origin master(x)

## 下载到本地：
    git clone 地址
    git clone 地址+（目录名称）（克隆 以你目录名称新建一个文件下载）
    git clone 地址 . (注意后面是空格+ . 用处是有一个新的空目录，把代码下载到空目录下)


<font color='red'> 
注意：自己的代码用SSH下载，反之别人的代码用HTTP下载
</font>

<font color='green'>git pull（git push之后如果提示你git pull，你就git pull，原因是把远程分支合并到本地对应的分支）
</font>

## 把一个文件推送到两个远程仓库
    cd ~/desktop --进入到桌面
    mkdir one    --创建文件
    cd one    --进入到one文件夹
    git init    --创建本地仓库
    touch 1.txt    --创建文件
    git add 1.txt    --提交到本地仓库
    git commit -v    --上传到本地仓库

## GitHub创建两个仓库
    git remote add origin 地址    --添加第一个远程仓库
    git remote add origin2 地址    --添加第二个远程仓库
    git push -u origin master    --上传到远程仓库
    git push -u origin2 master    --上传到远程仓库

## 配置快捷键
    
    touch ~/.bashrc
    echo 'alias ga="git add"'>> ~/.bashrc
    echo 'alias gc="git commit -v"'>> ~/.bashrc
    echo 'alias gl="git pull"'>> ~/.bashrc
    echo 'alias gp="git push"'>> ~/.bashrc
    echo 'alias gco="git checkout"'>> ~/.bashrc
    echo 'alias gst="git status -sb"'>> ~/.bashrc

    source ~/.bashrc   (最后一定要执行这个快捷方式才生效)

## git log用glog代替
    alias glog="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit -- | less"
最后执行source ~/.bashrc

## 美化历史命令
    git rebase -i xxxx  （xxxx为编号）
    