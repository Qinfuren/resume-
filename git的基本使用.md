## git 使用手册

### 基于本地仓库的使用
	git本地仓库的三种分区,也叫三棵树
		工作区：正常的工作分区，所有的可见开发都在工作区进行
		暂存区：工作区和版本区的暂时保留地，通过暂存区来提交到本地仓库也就是版本区
		版本区：工作成果的最终保留地，所有完成的工作都要提交到版本区
1. 创建仓库目录并初始化
	* git init
2. 添加新文件到暂存区
	 - git add test.txt 或者 git add *
3. 设置git仓库的配置信息
	 - git config --global user.name "Irick"
	 - git config --global user.email "lucasbollute@sina.com"
	 - git config --global core.editor "notepad"
4. 提交文件到将完成的工作提交到版本区
	- git commit -m "hello world"
	`git 当中，每次提交都必须设置提交的具体信息`
	```
	注意：由于git是分布式版本控制系统，每个用户本地都维护一个版本库，所以不存在更新工程的情况，
	我们可以使用版本库或者暂存区的文件来替换或者覆盖工作区的工程
	```
5. 常用命令
	- git status  `查看三个工作区的文件状态`
	- git branch `查看有多少个分支`
	- git checkout -b feature_x  `创建工作区的一个分支`
	- git merge feature_x	`将分支中的修改合并到主工作分支,合并过程中产生冲							突需要手动解决`
	- git checkout master `工作分支进行切换`
	- git branch -D feature_x `删除已经存在的工作分支`
	- git log `查看提交日志`
	- git tag v1.0+提交id
	- git checkout -- hello.txt`使用版本区的文件覆盖工作区的内容`
	- git fetch origin --> git reset --hard origin/master `丢弃本地所有的改动与提交， 使用版本库中的最新内容`
6. git高级命令：
 	- git rebase master `使用rebase而非merge来拉取上游修改，与merge不同，它不会产生合并提交日志,变基合并会产生一个更加整洁的项目历史`
	- git stash`临时保存暂时不想提交的修改，以便切换分支`
	- git stash list`列出修改栈中未完成的工作状态`
	- git stash pop`取回之前的工作状态，继续完成未完成的工作`
	- $ git stash save "describe it"   # give the stash a name
	- git stash clear          # delete a stashed commit
### 基于远程仓库的使用
    
1. 常用命令：
	- git clone url `克隆远程仓库到本地，并且建立连接`
	- git remote add origin url `和远程仓库创建连接`
	- git remote rm origin `删除和远程仓库的连接`
	- git push origin master `将本地版本区的内容推送到远程仓库`
	- git pull origin master`更新远程仓库中的内容到本地`
2. 使用公钥和私钥和远程仓库创建连接


---
* 查找关注大的项目: stars:>1000