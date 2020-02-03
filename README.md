# django知识点小结

## 快速入门
#### 从零开始
#### 入门教程
1.创建项目
```
django-admin startproject mysite
```
2.建数据库 (后面再补充直接改文件的方法)
```
python manage.py migrate 
python manage.py makemigrations
```
3.用于开发的简易服务器
```
python manage.py runserver 0.0.0.0:8000
```
4.用于生产环境中的部署启动
```
Nginx+uWSGI+Django
1.启动Nginx服务器 nginx -s reload
2.启动uWSGI服务器 uwsgi -x django_socket.xml
```
4.[django runserver部署和uwsgi部署的区别](https://www.cnblogs.com/linwenbin/p/11820970.html)
#### 进阶教程

## 获取帮助 ----暂略

## 这份文档是如何组织的 ----暂略

## 模型层
#### 模型
#### QuerySet
#### Model实例
#### 迁移
#### Advanced
#### 其他
这里只补充说明几点:<br>
1.要根据项目的实际情况来设置表结构;<br>
2.数据库查询一定要注意浪费,如models.UserInfo.objects.all();<br>
3.数据库增删改查的优化。<br>

在模块文件和静态文件这2块,实际开发的过程中往往采用前后端分离的模式,比如
[react + django 实现前后端分离 ](https://www.jianshu.com/p/e9bc8b819075)


## 视图层  --明天继续
#### 基础
#### 参考
#### 文件上传
#### 基于类的试图
#### 高级
#### 中间件

## 模板层
#### 基础
#### 对于设计者
#### 针对程序员

## 表单
#### 基础
#### 进阶

## 开发进程
#### 设置
#### 应用程序
#### 异常
#### django-admin.py和manage.py
#### 测试
#### Deployment

## 管理
#### 管理站点
#### 管理动作
#### 管理文档生成器

## 安全
#### 安全概览
#### 在django中披露的安全问题
#### 点击劫持保护
#### 跨站请求伪造CSRF保护
#### 登录加密
#### 安装中间件

## 国际化和本地化
## 性能和优化
## 地理框架
## 常用的Web应用程序工具
## 其它核心功能
## Django开源项目




