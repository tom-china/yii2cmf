## 安装:

进入项目根目录

1. `composer install` 

2. `php yii app`(windows 命令行乱码问题是因为windows命令行默认编码为gbk，项目编码为utf8，执行`chcp 65001`修改命令行编码为utf8即可)

3. `php yii serve`

4. 收工

    前台访问地址: `http://localhost:8080/`

    后台访问地址: `http://localhost:8080/admin/` 管理员 帐号 `hehe` 密码 `111111`

## 目录结构

```
api             api
backend         后台
common          核心
console         命令
database        数据库（迁移 填充）
frontend        前台
plugins         插件
runtime         运行时（日志 缓存等）
tests           测试
vendor          扩展
web             web统一入口（web服务器可只开放该目录,保证安全）
wechat          微信
.env            基本配置文件
helpers         基本工具函数（自动加载）
```

## 现有功能:

* rbac权限管理

* 系统配置,管理员操作日志等

* 文章,单页,评论,弹幕等

* 数据库备份还原

* 国际化 主题 皮肤

* 可拆卸插件

* todo

## demo

前台地址 `www.51siyuan.cn`

后台地址: `www.51siyuan.cn/admin`  帐号 `demo` 密码 `111111`

## 定时采集：

`crontab -e` 添加

`* * * * * php /path/to/yii schedule/run  1>> /dev/null 2>&1`

`console/schedule.php` 里添加

`$schedule->exec('craw jianshu')->daily();`

相关前端项目,基于本项目api
-----------------------

[vue-yii2cmf](https://github.com/yidashi/vue-yii2cmf)


