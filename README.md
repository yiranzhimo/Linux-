# Linux-Learning
Linux 命令

# 基本命令

## cat

cat 从第一行读取文件内容

## cd

**cd** 进入目录

**cd ..** 返回上级目录


## chgrp

chgrp [group] [file]

* -R或--recursive 　递归处理，将指定目录下的所有文件及子目录一并处理。 
* --reference=<参考文件或目录> 　把指定文件或目录的所属群组全部设成和参考文件或目录的所属群组相同。

## chmod

chmod 可以改变文件权限

> Linux 文件的基本权限有九个，分别是 owner/group/others 三种身份各有自己的 read/write/execute 权限，其中权限分数如下：
> r:4；w:2；x:1

chmod [R] xyz [file]，比如说，**chmod 777 test.txt**，就可以将 test.txt 的文件权限全部更改为 -rwx，同时使用 ls -l 命令查看文件详细情况。

**chmod a+/-[rwx] [file]** 给所有文件添加或减少权限。

## chown

设置文件所有者和文件关联组的命令

chown user[:group] [file]

**chown root /var/run/httpd:pid**，把 /var/run/httpd:pid 的所有者设置为 root

**chown runoob:runoobgroup test.txt**，把 test.txt 的拥有者设为 runoob，群体使用者 runoobgroup

**chown -R runoob:runoobgroup**，把当前目录的所有文件与子目录的拥有者设置为 runoob
  
## cp

cp 复制文件

**cp [file] [new_file]**，同时复制执行者的属性和权限

## echo

echo，打印出，显示出

## file

file [filename] 可以知道文件类型

## grep

**grep [pattern] [filename]**，查找文件中包含的字符串


## gzip

**gzip** [file]

通过 gzip 压缩文件，原始文件会不存在，比如说如果原始文件存在 link，就会导致无法压缩，而一旦压缩，原始文件会变成 .gz 文件。

gzip -d xxx.gz 解压缩命令

## head

head [n] [file]


## less

less [filename] 可以查看文件，按 q 退出。

command 模式下，g 回到文件首，G 跳转到文件末尾。

## ln

ln命令可用来创建硬链接或是符号链接

ln [参数] [源文件或目录] [目标文件或目录]

## ls

ls 可以列出当前目录的文件

**ls -a** 列出当前目录的可显示和隐藏文件

**ls -l [file]** 可以列出文件的详细信息

## mkdir

mkdir 创建目录

## mv

mv 命令可以执行文件移动和文件重命名操作，这具体取决于如何使用它。

**mv item1 item2**

将文件（或目录）item1 移动（或重命名）为 item2。

mv item… directory

将一个或多个条目从一个目录移动到另一个目录下。

## nano

简单的文书编辑器

**nano test.txt** 命令即可以编辑 txt 文件

* ctrl-X，离开 nano 编辑器
* ctrl-R，读取其他文件内容，读取内容会置于光标前
* ctrl-W，搜寻字符串
  
## pwd

**pwd** 显示当前路径

## qsub
提交任务

## qstat
查询任务状态，，常用状态：R 代表运行，Q 代表
排队，E 代表正在退出，H 代表挂起，C 代表运行完毕

## rm

**rm -r**，递归地删除目录

**rm -f**，强制删除，无需确认

## tac

tac 从最后一行读取文件内容


## tail

tail [n] [file]

打印结尾部分

## touch

**touch** 命令用于修改文件或者目录的时间属性，包括存取时间和更改时间。若文件不存在，系统会建立一个新的文件。

## tar

**tar** 是一个打包指令

* 压缩：tar -z< u>c</ u>v -f filename.tar.gz filename
* 解压缩：tar -z< u>x</ u>v -f filename.tar.gz

## vi

vi 有三种模式，一般指令模式，编辑模式和命令行命令模式。

输入 i/o/a 可以直接进入编辑模式，开始编辑文字;

按下 ESC 按钮回到一般指令模式；

输入 :wq 存储文件后离开。

## which

**which** 命令可以显示可执行程序的位置

## wc

**wc [file]** 显示文件中包含的行数、字数和 字节数。

# 其他

tap 键具有自动补齐功能

* Tap 接在一串指令的第一个字后面意为命令补齐
* Tap 接在一串指令的第二个字后面意为文件补齐

ctrl + c 中止正在进行的命令 

ctrl + d 键盘输入结束，离开命令行

打开带空格目录，可以使用 \ 转义，比如：

**cd /Users/xxx/Documents/VS\ Code/Perl/test.pl**





 


