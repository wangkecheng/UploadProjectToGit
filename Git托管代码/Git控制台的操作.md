#Git控制台的操作
 - 1.查看本机是否有git： git --help
 - 2.在桌面上创建一个git仓库和工作空间：mkdir  learngit
 - 3.进入learngit：cd learngit
 - 4.初始化仓库： git  init
 - 5.显示空间下的信息：ls -al
 - 6.若直接将文件拷贝到工作空间：打开空间：open.  之后 会弹出类似这样的
```
On branch master
Initial commit
Untracked files:
  (use "git add <file>..." to include in what will be committed)

	.DS_Store
	"\351\231\220\345\205\215\351\241\271\347\233\256\357\274\210\346\233\264\346\226\260).docx"
```
 - 7 **添加**. 让git管理仓库中的SVN\&Git.md ：git add SVN\&Git.md  之后有绿色字显示则添加成功 如：new file:   SVN&Git.md
   - 提交并写上注释 git commit  -m "添加"
 - 8 **修改**在仓库中修改已经管理的文件， 再运行git status 时 ， 会显示红字 modified: SVN&Git.md，  
   - 运行git add . 可完成修改 之后会显示蓝字 modified:   SVN&Git.md
     - 添加注释，git  commit  -m "修改"  
  -  **删除** 
     -  在管理空间中删除SVN\&Git.md  文件 
     -  方式 1、执行(系统删除方法) rm SVN\&Git.md
     -  会显示红字  	deleted: SVN&Git.md
        -  此时可以回滚操作 git checkout -- SVN&Git.md
        -   也可以执行 git add .从git中移除管理
    -   方式 2、 执行git rm SVN\&Git.md  ，表示执行了两步操作，一是删除 二是移除