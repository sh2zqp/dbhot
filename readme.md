## Git学习笔记

### 第一章 快速入门

#### 1.1 什么是Git
	
	分布式 版本控制 软件

#### 1.2 为什么要做版本控制

    要保留之前所有的版本，以便回滚和修改。

#### 1.3 安装Git

    详见 链接

### 第二章 “东北热”创业史

#### 2.1 第一阶段：单枪匹马开始干

>想要让Git对一个目录进行版本控制需要一下步骤： 

	1. 进入要管理的项目目录
	2. 执行初始化命令，让git帮助我们管理当前文件夹
		git init
	3. 管理目录下的文件状态
		git status  
		红色：新增的文件/修改了原来的老文件
		绿色：git已经管理起来
	4. 管理指定的文件（红变绿）
		git add 文件名
		git add .
	5. 个人信息配置，不配置会报错【只需要配置一次】
		git config --global user.name '用户名'
		git config --global user.email '邮箱'
	6. 生产版本
		git commit -m '描述信息'
	7. 查看版本记录
		git log

#### 2.2 第二阶段：拓展新功能

	git add .
	git commit -m '直播专区'
	
	git add .
	git commit -m '短视频专区'

#### 2.3 第三阶段：“短视频事件”

- 回滚到之前的版本
	
		git log
		git reset --hard 版本号

- 回滚之后版本

		git reflog
		git reset --hard 版本号

- git三个区域切换命令

	>见图：C:\Users\sh2zqp\Desktop\dbhot\image\readme\git工作区转换.png

		git reset --soft 版本号
		git reset HEAD -- 文件名
		git checkout -- 文件名  对修改的文件有效
		git reset --mix 版本号
		git reset --hard 版本号

#### 2.4 第四阶段：商城功能&紧急bug修复

- 分支

	> 分支可以给开发者提供多个环境使用，意味着你可以把你的工作从开发主线（master）上分离出来，以免影响开发主线。

- 紧急修复bug方案

	>见图：C:\Users\sh2zqp\Desktop\dbhot\image\readme\Bug紧急修复示意图及工作流.png

- 命令小结

	- 查看分支
				
			git branch

	- 创建分支

			git branch 分支名

	- 切换分支

			git checkout 分支名

	- 分支合并（可能产生冲突）

			git merge 要合并的分支
			注意：切换分支再合并

	- 删除分支

			git branch -d 分支名

#### 2.5 第五阶段：进军三里屯

- 家里和公司两地开发，需要借助远程仓库Github


- 常用命令

		本地创建远程仓库别名
		git remote add origin 远程仓库地址（origin为别名，可以任意，与下面对应）

		往远程仓库推代码
		git push -u origin master(分支名)

		远程仓库克隆代码 
		git clone https://github.com/sh2zqp/dbhot.git（内部已默认本地创建远程仓库别名，分支也复制下来）
		

