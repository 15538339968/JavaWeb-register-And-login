# JavaWeb-register-And-login
一个运用了MVC模式及JavaWeb三大框架的注册和登录系统

> 在网上找的一个项目，对比着敲了一遍。
>[项目来源](https://github.com/codingXiaxw/JavaWeb-Regist-and-Login)



## MVC模式
实现模型(domain)、视图(jsp)、控制器(servlet)三者的分离

## JavaWeb三大框架
实现Web层、Business(业务逻辑层)、Dao(数据层)三者内容的分离。将xml文件当作数据库，用Dao对其进行读取。

## 功能
### 注册界面:  
读取注册表单数据中的用户名，在xml文件中查找。若查找到，说明该用户名已被注册，要求客户重新注册；若没查找到，说明用户名没有被注册，将表单数据的用户名和密码保存到xml文件中，注册成功，点击跳转链接可以回到登录页面。  
其中设置了输入验证码的功能，防止恶意注册；对服务器表单进行校验，防止无效的用户名注册。
### 登录界面:  
读取登录表单数据中的用户名，在xml文件中查找。若查找到，则比较表单数据中的密码和xml文件中的密码，若二者相同，则登录成功跳转到welcome界面，若二者不相同，则返回密码错误的信息；若没有查找到，则返回用户名错误的信息。
### 欢迎界面
不允许用户直接登录该界面，若用户直接输入网址登录该欢迎界面，则要求客户登录后才能访问该界面。若用户通过登录成功，则可正常访问该界面。
