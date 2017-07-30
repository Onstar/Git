## 问题及解决方案

1. 当本地仓库和```Git```远程仓库建立连接（使用的是````git remote add origin https://....```的方式）后，对一个文件操作完了```git add```和```git commit```后，  
最后使用```git push```命令上传时，没有上传成功。
  * 出现原因：没有指定上传到哪个分支上。
  * 解决方式：```git push origin master```
