# tomcat-analysis
tomcat 源码分析。后续会在代码中补充中文注释，以及我的一些思考。
该项目是直接从 tomcat 官网上下载下来的 tomcat 源码，只不过我把它配置成了一个 maven 项目，从而方便在学习的过程 debug。

## 1. 说明
该项目的环境版本为：
- tomcat9
- jdk8
> 建议使用 idea 从 github 上导入该项目。

## 2. 环境配置

1、先把项目下载到本地，在终端执行下面这条 git 命令：
```
git clone https://github.com/ypfssm/tomcat-analysis.git
```
2、在 IDE（idea 或 eclipse） 中设置 org.apache.catalina.startup.Bootstrap 这个启动类的 JVM 参数如下：
```
-Dcatalina.home=<tomcat-analysis 这个项目所在的文件路径>/tomcat-analysis/home
-Dfile.encoding=UTF-8
```
比如说我把 tomcat-analysis 这个项目放到了 /shuaifei/IdeaProjects/ 这个文件夹下，那 -Dcatalina.home=/shuaifei/IdeaProjects/tomcat-analysis/home

这样环境就配好了，是不是很简单。嘿嘿嘿！！！

> idea 中如何设置 JVM 参数教程：https://blog.csdn.net/wangnayu/article/details/76794112
eclipse 中如何设置 JVM 参数教程：https://blog.csdn.net/FS1360472174/article/details/51147051

## 3. 项目启动
1、先把终端（Terminal）切换到 Maven 项目的根目录，比如：/shuaifei/IdeaProjects/tomcat-analysis/，然后执行 maven 命令：
````
mvn clean package
````   
2、等待 maven 打包编译完成后，点击 `Bootstrap` 类运行它的 main 方法
