## 介绍
这是一个研究生及导师经费管理系统，功能包括：

* 管理员增删改查
* 研究生信息增删改查
* 导师信息增删改查
* 研究生以及导师关系的管理
* 经费（批量）分配和分配日志
* 留言板，后台可回复
* 公告栏
* 网站信息管理
* 分页
* 数据导出
* 验证码
* 用户审核

## 导入数据库
数据库文件保存在Data文件夹下，导入即可.

## 修改数据库连接配置

修改`includes/common.inc.php`：

```php
define('DB_HOST', 'localhost');  //地址
define('DB_USER', 'root');       //用户名
define('DB_PWD', '');            //密码
define('DB_NAME', 'gmanage');    //数据库名
```

## 登录
初始登录时有以下用户：

`超级管理员：1000   密码：1`

`管理员：1001   密码：1`

## 其它

学生也可以用学号登录哦，不过必须被审核过后才行

用户角色有：`超级管理员、管理员、学生`
各角色功能有明显区别，分别登录就能发现了哦

超级管理员的后台管理包括`导出数据为excel、更改初始密码、是否允许注册、是否开启验证码、分页类型、每页条目数、网站标题、执行耗时`等等

安全方面考虑了应对`SQl注入、跨页面攻击、页面盗用`等等

:exclamation: PS：我的第一个完整项目，经验不足/不懂对象/高手勿喷～:grimacing:
