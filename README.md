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
9. [IDEA图文教程](https://mp.weixin.qq.com/s?__biz=MzIxNjA5MTM2MA==&mid=2652435550&idx=1&sn=6ccd0924ea91378023abee5e13137c53&chksm=8c620bd1bb1582c7526c58e94fc570f31f1dd009decf393550b5f797a550bf0956cd06a2e0cc&mpshare=1&scene=23&srcid=0503NFGEvFTLsl5obv0Em5Cv#rd)

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
`$ git init //初始化`   
`$ git add //添加文件`   
`$ git commit //提交`   
`$ git push //向远程仓库推送`   
`$ git clone //从远程仓库克隆`   
`$ git pull //从远程仓库拉取`   
10. 参考资料
  - [Git简明指南](http://www.runoob.com/manual/git-guide/)
  - [Git官方教程](https://git-scm.com/book/zh/v2/)

## Maven：依赖管理
在Java的世界中, 依赖管理是不得不面对的问题. 所谓依赖就是在项目中引用的开源类库(别人的)或者项目里的其他模块(自己的).
+ [IDEA自带 Maven 官方教程](https://www.jetbrains.com/help/idea/maven-support.html)
+ [Maven基本教程](http://www.runoob.com/maven/maven-tutorial.html)
+ [Maven视频教程](https://www.imooc.com/learn/443)
+ [认识`pom.xml`文件](https://www.cnblogs.com/wkrbky/p/6353285.html)

## Linux与云服务器：搭建个人网站
在网站后台的开发过程中, 通常测试环境和生产环境的软件都是运行在Linux服务器上. 而为了在公网上提供网络服务, 你需要一个公网固定IP 以及一个域名, 如果你想每次访问你的个人网站的时候都输入IP 来访问, 那么域名便不是必需的.    
购买一个当下云服务提供商的云主机能有效解决Linux操作系统和公网IP 的功能, 此外这些云服务提供商还一站式的提供了域名购买和备案服务(最新的规定购买的域名要备案才能使用了, 挺麻烦的, 周期一到两个月吧).
+ 云服务商
  + [AWS](http://aws.amazon.com)
  + [Google Cloud](http://cloud.google.com)
  + [Microsoft Azure Cloud](http://azure.microsoft.com)
  + [阿里云](http://www.aliyun.com)
  + [腾讯云](http://cloud.tencent.com)
  + [百度云](http://cloud.baidu.com)
  + [华为云](http://www.huaweicloud.com)
+ 体验腾讯云(试用[开发者实验室](https://cloud.tencent.com/developer/labs/gallery))
  + [搭建 Nginx 静态网站](https://cloud.tencent.com/developer/labs/lab/10003)
  + [基于 CentOS 搭建 WordPress 个人博客](https://cloud.tencent.com/developer/labs/lab/10001)
  + [基于 CentOS 搭建微信小程序服务](https://cloud.tencent.com/developer/labs/lab/10004)
  + [搭建 Java Web 开发环境](https://cloud.tencent.com/developer/labs/lab/10035)
+ [Linux命令行基础](http://www.runoob.com/linux/linux-command-manual.html)
  + 文件管理   
  `$ cd //切换工作目录`   
  `$ ls //查看文件信息`   
  `$ mkdir //创建目录`   
  `$ mv //移动`   
  `$ copy //复制`   
  `$ rm //删除文件`   
  `$ rmdir //删除目录`  
  + 权限管理   
  `$ chmod`
  + 启动服务   
  `$ nohup`   
  例如`$ nohup java -jar xxx.jar >xxx.log 2>&1 & //java -jar xxx.jar：启动打包好的jar宝, xxx.log：指定标准输出为xxx.log, 2>&1：将标准错误流重定向到标准输出, &：让该命令在后台运行`

## 万事俱备只欠东风：开始你的Java 开发
### Java基础
+ 基本类型与运算   
  + [Java中基本数据类型和包装类](https://www.cnblogs.com/linjiaxin/p/6393380.html)    
  Java是一种面向对象语言, Java中的所有对象都是由Object类派生而来, 但Java的八大基本类型是特例, Java中万物皆对象, 除了这八位大哥
  + [Java中boolean类型到底占用多少个字节？](https://blog.csdn.net/YuanMxy/article/details/74170745)
  + [运算符](http://www.runoob.com/java/java-operators.html)
+ 流程控制
  + if-else
  + switch
  + while
  + for
  + break
  + continue
  + return
+ 面向对象
+ 权限控制
+ 继承
+ 接口
+ 多态
+ 反射
+ 注解
+ 异常
+ 容器
+ I/O
+ 并发
+ JUnit

### 服务框架
+ Spring
+ Spring MVC
+ Spring Boot
+ Spring Cloud

### 核心组件
+ MySQL
+ MongoDB
+ Redis
+ Zookeeper
+ Kafka
+ FastDFS
+ Elasticsearch

### 部署服务
+ Docker

### 设计模式
+ [23种设计模式全解析](https://www.cnblogs.com/geek6/p/3951677.html)
+ [JDK中的设计模式](https://mp.weixin.qq.com/s?__biz=MzIxNjA5MTM2MA==&mid=2652435557&idx=1&sn=87e79f13b2bf0a151aea16f2c21a16b0&chksm=8c620beabb1582fc99a9ae079ba0de7004b7517e983dd83b8c7d7e415cbe8712d269e3c5ed45&mpshare=1&scene=23&srcid=0503F7nxSDKOWCMVgAJTiEyy#rd)

### 网站 & 博客

+ [并发编程网](http://ifeve.com/)
+ [Stackoverflow](https://stackoverflow.com/)
+ [Javaworld](https://www.javaworld.com/)
+ [Java API Examples](https://www.programcreek.com/java-api-examples/)
+ [Java 技术驿站](http://cmsblogs.com/)
+ [剑指offer](http://zhedahht.blog.163.com/)
+ [张开涛的博客](https://jinnianshilongnian.iteye.com/)
+ [Javadoop](https://javadoop.com/)
+ [花钱的年华](http://calvin1978.blogcn.com/)
+ [梁桂钊的博客](http://blog.720ui.com/)
+ [Best的博客(哈哈哈哈，忍不住放了上来)](https://blog.csdn.net/whut2010hj)

### 代码规范
+ [阿里巴巴 Java 开发手册（详尽版）]()
+ [Effective Java第三版中文版](https://legacy.gitbook.com/book/jiapengcai/effective-java/details)
+ [Google Java 编程规范（中文版）](http://www.gitbook.com/book/jervyshi/google-java-styleguide-zh/details)
