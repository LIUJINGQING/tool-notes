## Git使用教程

## 一、Git简介

​	Git是由C语言开发目前世界上最先进的分布式版本控制系统。



## 二、安装Git

###1、在Linux上安装Git

​	你可以试着输入`git`，看看系统有没有安装Git。

- Apt-get 安装

```sh
$ git
The program 'git' is currently not installed. You can install it by typing:
sudo apt-get install git
```
​	像上面的命令，有很多Linux会友好地告诉你Git没有安装，还会告诉你如何安装Git。如果你碰巧用Debian或Ubuntu Linux，通过一条`sudo apt-get install git`就可以直接完成Git安装。



>  ==注意==:老一点的Debian或Ubuntu Linux，要把命令改为`sudo apt-get install git-core`，因为以前有个软件也叫GIT（GNU Interactive Tools），结果Git就只能叫`git-core`了。由于Git名气实在太大，后来就把GNU Interactive Tools改成`gnuit`，`git-core`正式改为`git`。



- Yum 安装

```sh 
$ git
-bash: git: command not found
```


​	像上面的命令，提示系统没有找到该命令。需要自行安装Git。如果你碰巧使用CentOS或Redhead，通过一条`sudo yum -y install git`就可以之间完成Git安装。

- 源码安装

  如果是其它Linux版本，可以直接通过源码安装。先从Git官网下载源码，然后解压，依次：`./config`，`make`，`sudo make install`这几个命令安装就好了。

### 2、在Mac OS X上安装Git

​	你可以试着输入`git`，看看系统有没有安装Git：

- Homebrew 

  安装homebrew，然后通过homebrew安装Git，具体方法请参考homebrew的文档：[brew.sh](http://brew.sh)

- Xcode 

  从App Store安装Xcode ，Xcode 集成Git，不过默认没有安装，你需要运行Xcode ，选择菜单"Xcod"->"Preferences"，在弹出窗口中找到"Downloads"，选择"Command Line Tools",点"Install"就可以安装了。

### 3、在Windows上安装Git

   在Windows上使用Git，可以从Git官网直接[下载安装程序](https://git-scm.com/downloads)，然后按默认选项安装即可。

   安装完成后，在开始菜单里找到“Git”->“Git Bash”，蹦出一个类似命令行窗口的东西，就说明Git安装成功！

   ![install-git-on-windows](https://www.liaoxuefeng.com/files/attachments/919018718363424/0)

   安装完成后，还需要最后一步设置，在命令行输入：

```
   $ git config --global user.name "Your Name"
   $ git config --global user.email "email@example.com"
```

   因为Git是分布式版本控制系统，所以，每个机器都必须自报家门：你的名字和Email地址。你也许会担心，如果有人故意冒充别人怎么办？这个不必担心，首先我们相信大家都是善良无知的群众，其次，真的有冒充的也是有办法可查的。

   > ==注意==:`git config`命令的`--global`参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。



## 四、使用Git

### 1、创建版本库

​	创建一个版本库非常简单，寿险选择一个合适的地方，创建一个空目录。再通过`git init`命令把这个目录变成Git可以管理的仓库即可。

```sh
$ mkdir git-test
$ cd git-test/
$ pwd
/Users/mr_liu/mr_liu-data/git-repositories/git-test
$ git init
Initialized empty Git repository in /Users/mr_liu/mr_liu-data/git-repositories/git-test/.git/
   ```

​	瞬间Git仓库就建好了，而且返回告诉你空的仓库(empty Git repository)，并且当前仓库下多了.git的隐藏目录，该目录为该仓库的配置目录，没事不要手动修改该目录。

### 2、 文件操作

​	文件操作均在仓库目录下进行。

 - 添加文件进仓库

   我们在仓库主目录下创建readme.md文件，文件内容如下：

   ```shell
   Git is a version control system
   Git is free software
   ```

   1. 用`git add`命令告诉Git，把文件添加到仓库

      ```sh
      $ git add readme.md
      ```

   2. 用`git commit`告诉Git，把文件提交到仓库

      ```sh
      $ git commit -m "wrote a readme file"
      [master (root-commit) 87b48ab] wrote a readme file
       1 file changed, 2 insertions(+)
       create mode 100644 readme.md
      ```

   > 简单解释一下`git commit`命令，`-m`后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。
   >
   > `commit`可以一次提交很多文件，所以你可以多次`add`不同的文件

- 版本回滚

  1. 查看当前Git仓库状态

     我们修改一下readme.md文件，改成如下内容：

     ```shell
  Git is a distributed version control system.
  Git is free software.
     ```
     
     现在，运行`git status`命令查看结果：
     
     ```sh
     $ git status
     On branch master
     Changes not staged for commit:
       (use "git add <file>..." to update what will be committed)
       (use "git restore <file>..." to discard changes in working directory)
     	modified:   readme.md
     
     no changes added to commit (use "git add" and/or "git commit -a")
     ```
     
     `git status`命令可以让我们时刻掌握Git仓库当前状态，上面的命令输出告诉我们，`readme.md`被修改过了，但还没有准备提交修改。
     
     

- 





### 3、 远程仓库

### 4、分支管理

### 5、标签管理

### 6、自定义Git

## 四、使用GitHub

## 五、使用Gitee

## 六、搭建Git服务器

## 七、使用SourceTree



