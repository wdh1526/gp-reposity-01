# Git

配置信息

> git config --global user.name 'bobo'

> git config --global user.email 'bobo@163.com'

在个客户端的情况下用来身份识别

## 基本操作

### 1 创建版本库

指定一个文件夹位置即可

### 2 初始化操作

要将某个文件夹作为版本库，需要通过`git init`进行初始化

### 3 添加文件

> 把某个文件管理起来，首先创建一个文件；

> 通过`git add xx`命令添加到版本库中；

> 执行`git commit -m '备注'`，来提交；

### 4. status和diff命令

| 命令   | 介绍                                 |
| ------ | ------------------------------------ |
| status | 查看当前库的状态                     |
| diff   | 用来查看文件的变化（工作区和版本库） |

### 5. 版本回退

#### 5.1. log命令

查看文件的历史版本

简化日志文件的显示方式 `git log  --pretty=oneline`

#### 5.2 版本回退

回退到上一个版本

> git reset --hard HEAD^

回退到指定的版本

> git reset --hard 版本编号

回退到最新版本

> git reset --hard 最新版本号

> 还可以借助 `git reflog`查到过往所有变化，包括版本切换回退

## 工作区和暂存区

创建文件------工作区

> `git add`-------工作区到暂存区

> `git commit`----------master版本库里，从暂存库到版本库

## 撤销管理

### 还未提交到暂存区

> `git checkout --file `

### 提交到暂存区

> `git reset HEAD fileName` 撤销到工作区
>
> `git checkout --fileName`撤销操作

 ### 已经提交到版本库

> 直接回退到上个版本 `git reset --hard HEAD^`

## 删除管理

操作和添加文件类似

> 工作区：是直接编辑的地方，比如Eclipse打开的项目或记事本打开的文件，直接操作
>
> 暂存区：数据暂时存放的区域，是工作区和版本库之间进行数据交流的纽带
>
> 版本库：存放已经提交的数据，push的时候，就是将这个区域的数据push到远程仓库

## Github远程仓库

### 1 创建SSH key

`ssh-keygen -t rsa -C "wangdonghe2018@163.com"`

![image-20210421112410313](C:\Users\wdh\AppData\Roaming\Typora\typora-user-images\image-20210421112410313.png)

### 2 登录Github

配置SSH

右上角->settings

![image-20210421112634486](C:\Users\wdh\AppData\Roaming\Typora\typora-user-images\image-20210421112634486.png)

![image-20210421112845804](C:\Users\wdh\AppData\Roaming\Typora\typora-user-images\image-20210421112845804.png)

### 3 创建远程仓库

![image-20210421113023853](C:\Users\wdh\AppData\Roaming\Typora\typora-user-images\image-20210421113023853.png)

![image-20210421113135343](C:\Users\wdh\AppData\Roaming\Typora\typora-user-images\image-20210421113135343.png)



### 4 关联远程仓库

![image-20210421113748703](C:\Users\wdh\AppData\Roaming\Typora\typora-user-images\image-20210421113748703.png)

`git remote add origin git@github.com:wdh1526/gp-reposity-01.git`