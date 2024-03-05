# git （分布式版本控制软件）

```git
git init 初始化当前目录 即开始接管管理该目录的所有东西
```

```
git status   查看当前目录下文件的状态
```

## 1.三种状态：  工作区  暂存区 版本区

- ​     红色：	新增文件/被修改的老文件 

- ​     绿色：  git已经管理起来的文件-    

```g
  git add 文件名 / .（指所有文件）
```

- ​     在生成版本需要 你设置用户名和邮箱[一次即可]

```
git  config  --global user.email "邮箱1

git config --global  user.name "用户名"
```



- 透明色(看不到): 即生成版本

```
git commit -m '描述信息'
```

- 查看版本记录

```
git log
```

## 2 第二阶段 “拓展新功能”

```
git add .

git commit -m '描述'
```

### 2.2第三阶段 “约饭事件”

- #### *回滚至之前的版本*

```
git log

 git reset --hard 版本号
```

- #### 回滚之后的版本

```
git reflog   #查看之前版本

git reset --hard 【版本号】
```

- #### 处理bug 或开发新功能运用分支功能

```
git branch 查看分支

git branch [分支名] 创建分支

git branch -d [分支名] 删除该分支

git checkout [分支名] 切换分支

git  merge [分支名]  将输入的分支名合并到当前分支
```

## 3.Github+git使用

```
1.给远程仓库其别名

git remote add [别名] [仓库地址]

2.想远程仓库发送代码

git push -u [别名] [分支名]
```
### 3.1在公司第一次开发拉取代码

```
1.克隆远程仓库代码

git clone  [远程仓库地址] (内部已经完成git remote add [别名] [仓库地址])

2.切换分支

git checkout [分支名]
```

### 3.2**在公司进行开发**

```
1.切换到开发分支
git  checkout development
2.将主分支合并到开发分支上《仅一次即可》
git  merge master
3.修改代码
4.提交代码
git add .
git commit -m “”
git push origin development
```

### 3.3回到家中继续开发

```
1.切换到开发分支
git checkout development
2.拉代码
git pull origin development
3.继续开发
4.提交代码
git add .
git commit -m “xxx”
git push origin development
```

### 3.4开发完毕后投入到线上

```
git checkout master
git merge development
git  push  origin master
同时也把开发分支推到远程(必要习惯)
git checkout development
git merge master
git push origin development
```

### 3.5衍生两条命令

```
git pull origin development #将github拉到工作区
相当于
git fetch origin development #将github拉到版本区
git merge origin/development #将版本区合并到工作区
```

### 3.6 rebase三种应用场景

#### 3.6.1第一种  将多个提交整合成一个提交

```
git rebase -i 【版本号】     #当前版本合并到输入版本
git rebase -i HEAD～3       #合并当前版本前三个版本
```

**执行完后 将顶部pick保留其余pick改为s保存**
**之后又会让你重新修改一次提交记录**

#### 3.6.2第二种 将development分支合并到master分支（图形意义上）

```
此命令详细显示提交记录简洁版
git log --graph --pretty=format:"%h %s"
```

操作流程：

```
git checkout development           #切换到开发分支
git rebase master                  #将master分支新内容拉到development分支一条线上
git checkout master                #切换到master分支
git merge development              #在将两条分支合并到master分支上
```

#### 3.6.3第三种：在家一个版本和在公司一个版本都未及时提交仓库时，pull代码时会产生一次分叉记录，rebase解决分叉而使用

操作流程：

```
git fetch origin development
git rebase origin/development
```

```
流程过程中难免会遇到同一文件不通版本修改过，从而引起冲突，手动解决冲突后执行
git rebase --continue 即可
```

### **3.7beyond compare 解决冲突软件**

