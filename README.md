# Git六行配置
* `git config --global user.name 你的英文名`
* `git config --global user.email 你的邮箱`
* `git config --global push.default simple`
* `git config --global core.quotepath false`
* `git config --global core.editor "code --wait"`
* `git config --global core.autocrlf input`
# Git命令
* `git init`
初始化git本地仓库,创建一个.git目录
* `git add`
将文件添加到暂存区
* `git commit`
将暂存区里的内容添加到本地仓库中
-m 后接较短的描述
-v (verbose) 会用编辑器打开，可以写较长的描述，同时能帮你回顾修改了哪些内容
* `git log`
查看每一次提交的时间，同时查看提交的版本号
* `git reflog`
更简洁，能查看所有改动包括reset的HEAD编号和提交描述
* `git reset --hard xxxxx`
接之前提交的HEAD编号，可以回滚到之前提交的代码状态
* `git branch xxxx`  
创建分支，空格后接分支名
*`git checkout xxxx`
切换分支
# Git远程仓库
### 创建SSH KEY
[docs.github.com](docs.github.com)中搜索最新ssh key添加代码
到 .ssh目录中查看.pub文件，复制粘贴到GitHub网页中的New SSH Key
### 上传本地仓库到GitHub
* `git remote add origin git@xxxxxxxx`
在本地添加远程仓库地址，使用SSH地址，不用每次密码验证
* `git push -u origin master`
推送到远程仓库origin的master分支
### 下载远程仓库到本地
* `git clone git@?/xxx.git`
克隆远程仓库的代码到本地，Clone or Download中，复制SSH地址到命令行，然后yes
别人的代码只能https下载
记得cd目标路径
下载是所有分支，可以git checkout查看分支
