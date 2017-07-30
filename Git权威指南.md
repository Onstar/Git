# git初始化

1. 创建仓库及提交    
    1. 初始化仓库
    ```
	  git inint 或者 git init 文件名:前者会把当前所在目录初始化为一个仓库，  
	  	后者会在当前目录下新建一个文件，并把这个文件初始化为一个仓库。
	```
	2.创建一个文件，并写入内容
	```
	  echo "hello" > welcome.txt
	  //创建一个内容为"hello"的welcom.txt文件
	  
	```
	3. 将文件添加到暂存区
	```
	  git add welcome.txt
	  // git add . ：表示将工作区的所有文件添加到暂存区里
	  
	```
	4. 将文件提交
	```
	git commit -m "有关提交相关说明"
	
	```
	
2. 提交（commit）前的设置

要为 ```Git```设置全局配置变量 ```user.name```、```user.email```。否则，提交(commit)会失败
```
git config --global user.name "用户名"  
git config --global user.email "Email地址"

// 删除Git全局配置文件中user.name和user.email的设置：  
git config --unset --global user.name
git config --unset --global user.email

```

3. ```git config```命令的一些参数的设置及区别
	* ```Git```别名的设置
		1. 如果拥有系统管理员权限（例如通过执行```sudo```命令获取管理员权限），希望注册的命令别名能够被所有的用户使用，可以执行如下命令：
		```
		  sudo git config --system alias.st status
		  sudo git config --system alias.ci commit
		  sudo git config --system alias.co checkout
		  sudo git config --system alias.br branch
		  
		```
		2. 也可以运行下面的命令，只在本用户的全局配置中添加```Git```命令别名：
		```
		  git config --global alias.st status
		  git config --global alias.ci commit
		  git config --global alias.co checkout
		  git config --global alias.br branch
		  
		```
	* ```Git config```命令参数的区别
	
	```
	  1. 执行下命令，是对 /demo/.git/config文件进行编辑（demo是本地仓库文件夹）
	    cd demo/.git/config
	    git config -e  
	  2. 执行下命令，是对 /home/xxx/.gitconfig（用户主目录下的.gitconfig 文件）全局配置文件进行编辑
	    cd /home/xxx/.gitconfig
	    git config -e --global
	   3. 执行下命令，是对/etc/gitconfig 系统级配置文件进行编辑。如果Git安装在非标准位置，则这个系统的配置文件可能是在另外的位置。
	     cd /etc/gitconfig
	     git config -e --system
	```
	```Git```的三个配置文件分别是版本库级别的配置文件、全局配置文件（用户主目录下）和系统级配置文件（/etc目录下）。配置文件的优先级高到低是：版本库，全局配置文件，系统配置文件。
	
		
	
