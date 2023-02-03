# git-learning
git-learning course at 极客时间 三剑客课程

1、初探 .git 目录

用到的命令：
git cat-file -t 查看对象类型：git cat-file -t e23ed33 输出 commit，说明该哈希值的对象是个 commit

在根目录下（...../jikeshijian/）
```
cd .git
ls -al
# 打印出：
# total 40
# drwxr-xr-x  12 Ethan  staff  384  2  2 23:36 .
# drwxr-xr-x@  4 Ethan  staff  128  2  2 23:35 ..
# -rw-r--r--   1 Ethan  staff   19  2  2 23:36 COMMIT_EDITMSG
# -rw-r--r--   1 Ethan  staff   23  2  2 23:31 HEAD
# -rw-r--r--   1 Ethan  staff  137  2  2 23:31 config
# -rw-r--r--   1 Ethan  staff   73  2  2 23:31 description
# drwxr-xr-x  14 Ethan  staff  448  2  2 23:31 hooks
# -rw-r--r--   1 Ethan  staff  137  2  2 23:36 index
# drwxr-xr-x   3 Ethan  staff   96  2  2 23:31 info
# drwxr-xr-x   4 Ethan  staff  128  2  2 23:36 logs
# drwxr-xr-x   7 Ethan  staff  224  2  2 23:36 objects
# drwxr-xr-x   4 Ethan  staff  128  2  2 23:31 refs
```

对其中解释如下：
1. HEAD 文件
   保存着当前分支的信息
   ```
   cat .git/HEAD
   # ref: refs/heads/master
   ```
2. config 文件
   保存着配置信息，如姓名邮箱等
3. refs 文件夹
   1. heads——分支信息
   2. tags——标签信息，也叫里程碑
