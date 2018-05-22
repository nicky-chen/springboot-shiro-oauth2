# springboot-shiro-oauth2

#### 项目介绍
Springboot + shiro权限管理

#### 开发环境

| 工具    | 版本或描述                |    
| ----- | -------------------- |    
| OS    | Windows 10           |    
| JDK   | 1.8+                 |    
| IDE   | IntelliJ IDEA        |    
| Maven | 3.3.1                |    
| MySQL | 5.6.4                |    

#### 模块划分

| 模块         | 释义                      |    
| ---------- | ----------------------- |    
| shiro-core  | 核心业务类模块，提供基本的数据操作、工具处理等 |    
| shiro-admin | 后台管理模块                  |    

#### SQL Model

![首页](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/sql-model.png?raw=true)

#### 使用说明

1. 使用IDE导入本项目
2. 新建数据库`CREATE DATABASE shiro;`
3. 导入数据库`docs/db/shiro.sql`
4. 修改(`resources/application.yml`)配置文件
   1. 数据库链接属性 
   2. redis配置
   
5. 运行项目(三种方式)
   1. 项目根目录下执行`mvn -X clean package -Dmaven.test.skip=true`编译打包，然后执行`java -jar shiro-admin/target/shiro-admin.jar`
   2. 项目根目录下执行`mvn springboot:run`
   3. 直接运行`ShiroAdminApplication.java`
6. 浏览器访问`http://127.0.0.1:8080`

**用户密码**

_超级管理员_： 账号：root  密码：123456 

_普通管理员_： 账号：admin  密码：123456

**Druid监控**

_链接_： `http://127.0.0.1:8080/druid/index.html`

用户名：admin  密码：123456


#### 图片预览

![首页](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/index.png?raw=true)
![资源管理](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/root-resource.png?raw=true)
![角色管理](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/root-role.png?raw=true)
![角色分配资源](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/root-role[root].png?raw=true)
![用户管理](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/root-user.png?raw=true)
![用户分配角色](https://github.com/nicky-chen/springboot-shiro-oauth2/blob/master/docs/img/root-user[role].png?raw=true)

_注：以上图片是以`root`用户登录，`admin`用户的界面请参考`docs/img`下的图片_

