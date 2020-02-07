# 客户端自动更新API接口设置

总的设计是:2张表.<br>
1张记录oss上的包的信息(oss_msg表);<br>
1张记录当前环境安装的客户端版本信息(version表)。<br>

#### 表的字段设置如下:
```
表名        字段
oss_msg表	包的版本     package_version
            包的下载url  package_download
```
```
表名        字段
version表	当前版本     current_version
```

#### API设置如下:
```
  接口功能                               API                接口实现的内容(包括接口的返回信息,接口中所要做的事情)
1.查询当前环境上已安装的客户端版本信息   /search_version/    {current_version:*};若有版本更高的包,则+{package_version:*;package_download:***}
2.查询出oss上所有版本信息                /version_list/      返回oss_msg表的全部数据
3.升级到指定版本                         /update_version/    升级成功后需要更新 version表的 current_version 字段
4.回滚到指定版本                         /rollback_version/  回滚成功后需要更新 version表的 current_version 字段

5.上传新版本的包到oss服务器             /update_package/    上传成功后oss_msg表增加数据
6.删除oss上指定的版本包                 /delete_package/    删除包成功oss_msg表删除对应数据
```


