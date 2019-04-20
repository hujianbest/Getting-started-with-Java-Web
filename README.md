# Java后端入门知识图谱
## 如何用[学校邮箱](http://mail.whut.edu.cn/)申请[IntelliJ IDEA](https://www.jetbrains.com/idea/)开发软件的正版授权
1. [注册](https://account.jetbrains.com/login)JetBrains Account
2. 根据验证邮件中的指引完成注册
3. 登录并查看[Licenses](https://account.jetbrains.com/licenses)
4. 申请[学生版](https://www.jetbrains.com/student)
5. 填写EDU邮箱并[申请](https://www.jetbrains.com/shop/eform/students)
6. 验证邮件
7. [下载](https://www.jetbrains.com/idea/download)Ultimate版本
8. 安装IDEA并使用已获得LICENSE的账号登录即可

## Git 与 Github: 开始你的代码管理
1. [下载](https://git-scm.com/)并安装Git
2. 配置本地Git的用户名和邮箱   
`$ git config --global user.name "username" //用户名`  
`$ git config --global user.email "your@email.com" //邮箱`
3. [注册](https://github.com/)Github Account
4. 在本地Git中创建SSH Key   
`$ ssh-keygen -t rsa -C "your@email.com"`   
Windows下会在用户文件夹下的`.ssh`文件夹下生成两个秘钥文件   
其中`id_rsa`为私钥，`id_rsa_pub`为公钥
5. 将`id_rsa_pub`中的内容复制到[Github SSH Key](https://github.com/settings/keys)中， 添加， 可使用下述命令验证   
`$ ssh -T git@github.com`
6. 在Github中创建一个repository, 即Github远程仓库
7. 在本地Git中添加远程仓库   
`$ git remote add origin git@github.com:xxx.git //github repository 的地址`
8. 然后即可使用`git push`命令将本地代码推动到远程仓库了   
`$ git push -u origin master //第一次推送需指明远程仓库的别名和分支`   
`$ git push //后续只需push即可`
9. Git常用命令   
`git init //初始化`   
`git add //添加文件`   
`git commit //提交`   
`git push //向远程仓库推送`   
`git clone //从远程仓库克隆`   
`git pull //从远程仓库拉取`   
10. 参考资料
  - [Git简明指南](http://www.runoob.com/manual/git-guide/)
  - [Git官方教程](https://git-scm.com/book/zh/v2/)

## Maven：依赖管理
+ [IDEA自带 Maven 官方教程](https://www.jetbrains.com/help/idea/maven-support.html)
+ [Maven基本教程](http://www.runoob.com/maven/maven-tutorial.html)
+ [Maven视频教程](https://www.imooc.com/learn/443)
+ [认识`pom.xml`文件](https://www.cnblogs.com/wkrbky/p/6353285.html)

## Linux与云服务器：搭建个人网站
