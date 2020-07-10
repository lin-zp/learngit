# git使用

## 安装完git之后需要两条命令：

​		安装完成后再开始菜单选择GIT->GIT Bash,弹出命令行工具证明安装成功。

​		Git是分布式版本控制系统，所以在你的电脑上需要有用户名和用户邮箱，指令为：

```
$git config --global user.name "Your name"

$git config --global user.email "Your email"
```

$git config 中的 --global 指令表示此机器整个参考都使用此配置的用户，也可为单独的仓库设置单独的用户。

## 创建版本库

​		版本库（repository），也就是仓库，可以理解为一个目录，且此目录中所有的文件都可以被git管理。Git可追踪文件的修改、删除，以便还原文件。

​		创建版本库流程（git bash）：

```
1.使用指令 “$mkdir 创建目录名” 在合适的根目录下创建所需要的目录；

2.使用指令 “$cd 创建好的目录名” 跳转到目标目录文件下；

3.使用指令 “$pwd” 可显示目前文件夹的路径；

4.在目前文件夹下使用指令 "$git init"在此目录下创建git版本库，会在此目录下生成一个".git"目录。
```

​		把一个文件放入git仓库：

```
1.创建一个新的readme.md文件；

2.使用指令 "$git add readme.md" 将readme.me添加入仓库中，添加成功不会有任何提示；

3.使用指令 "$git commit -m "提交填写的信息""对已添加的文件提交到仓库。-m "信息" 为每次提交进行的说明。commit 将对已添加的文件一次性提交，因此可以add多个文件一次commit。提交成功提示 1 file changed（一个文件被改动） 2 insertions(+)（插入了两行内容）。
```

​		查看工作区状态和修改后的文件区别：

```
1.使用指令 "$git status" 可以查询工作区状态：
On branch master
nothing to commit, working tree clean（工作目录是干净的，无需要提交的修改）
------------------------------------------------On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
        modified:   readme.md
no changes added to commit (use "git add" and/or "git commit -a")（readme.me文件被修改，使用add或commit进行添加或提交）

2.使用指令 "$git diff" 查询修改后的文件与原文件的区别（diff—>difference）：
diff --git a/readme.md b/readme.md
index d8036c1..a5fc558 100644
--- a/readme.md
+++ b/readme.md
@@ -1,2 +1,3 @@
-Git is a version control system.
-Git is free software.
\ No newline at end of file
+Git is a distributed version control system.
+Git is free software.
```

```
$git log
$git reset --hard HEAD^
$cat readme.md
$git reflog
```

