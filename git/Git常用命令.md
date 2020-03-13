# Git常用命令

`git config`	*用来配置git配置文件,其中参数`--local`仓库级别，必须要进入到具体的目录下`--global`用户级别`--system`系统级别*

> 通常：
>
> git 仓库级别对应的配置文件是当前仓库下的.git/config 
>
> git 用户级别对应的配置文件是用户宿主目录下的~/.gitconfig
>
> git系统级别对应的配置文件是git安装目录下的 /etc/gitconfig

`git config --local -l` 	*查看仓库配置，必须要进入到具体的目录下*

`git config --global -l` 	*查看用户配置*

`git config --system -l` 	*查看系统配置*

`git config -l` 	*查看所有的配置信息*

`git config -e` 	编辑配置文件 

>`git config --local -e` 编辑仓库级别配置文件
>
>`git config --global -e` 编辑用户级别配置文件
>
>`git config --system -e` 编辑系统级别配置文件 

`git config --global user.email “you@example.com”`	*添加用户邮件地址*

`git config --global user.name “Your Name”`		*添加用户名*

`git init`	初始化一个Git仓库。

`git add <file>`	添加文件，可以多次使用添加多个文件。

`git commit -m <message>`	提交至Git仓库，并给予提交说明