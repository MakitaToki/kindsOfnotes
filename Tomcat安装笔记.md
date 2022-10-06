### 步骤

1. 解压tomcat

   ![1662299315949](image/Tomcat安装笔记/1662299315949.png)
2. 添加环境变量

   ![1662299708341](image/Tomcat安装笔记/1662299708341.png)

   PATH里

   ![1662299810157](image/Tomcat安装笔记/1662299810157.png)
3. tomcat-users.xml里添加一下几句

   ```
   <role rolename="manager-gui"/>
   <role rolename="admin-gui"/>
   <user username="admin" password="admin" roles="admin-gui"/>
   <user username="tomcat" password="admin" roles="manager-gui"/>
   ```
4. 双击

   ![1662300163934](image/Tomcat安装笔记/1662300163934.png)

在8080端口可以访问tomcat了
