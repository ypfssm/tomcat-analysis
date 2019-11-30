# tomcat-analysis
tomcat 源码分析
##1. 说明
该项目的环境版本为：
- tomcat9
- jdk8
> 建议使用 idea 从 github 上导入该项目。
##2. 环境配置
只需设置 org.apache.catalina.startup.Bootstrap 这个启动类的 JVM 参数如下：

```
-Dcatalina.home=<tomcat-analysis 这个项目所在的文件路径>/tomcat-analysis/home
-Dfile.encoding=UTF-8
```
> 比如说我把 tomcat-analysis 这个项目放到了 /shuaifei/IdeaProjects/ 这个文件夹下，那 -Dcatalina.home=/shuaifei/IdeaProjects/tomcat-analysis/home
##3. 项目启动
1、先把终端（Terminal）切换到 Maven 项目的根目录，比如：/shuaifei/IdeaProjects/tomcat-analysis/，然后执行 maven 命令：
````
mvn clean package
````   
2、等待 maven 打包编译完成后，点击 `Bootstrap` 类运行它的 main 方法