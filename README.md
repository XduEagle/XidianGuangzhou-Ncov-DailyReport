# 前言
本自动晨午晚检自动填写脚本为西电广研院最新适配版，依靠挂载在Github上使用Github Action自动运行。或者使用Linux等系统的自动运行程序

原西电本部版本README如下，脚本参数修改可参考下文。

# 如需使用请自行更改地址，本Repository不再更新

# AutoDailyCheck 个人使用方法

## 简单上手

1. 首先你需要一台电脑或虚拟机，安装python3和pip
2. 使用pip下载requests库
3. 只需下载该仓库内的personal.py文件，修改uname和upswd为自己的学号和密码
4. 定时运行这个py代码即可（例如使用cron或Windows计划任务）






# AutoDailyCheck 多人项目构建
每日自动晨午晚检，解放双手~  
Powered by Python + Flask

## 立即上手
❤ [DEMO](https://soowin.me)

## Debug方法
1. Checkout codes
2. Requirements： Python3 and Linux OS (Not supported on Windows when using gunicorn)
0. Create a new file "users.json" in sever folder.  
Format like this:  
 {"ID1":"password2", "ID2":"Password2"}
3. execute ```python3 -m pip install -r requirements.txt```
4. execute ```python3 -m flask run -h Host -p Port```

You can also uncomment the main function in app.py and run
```python3 app.py```


## 性能突破
由于本身性能的问题，Flask 并不适合直接用作web 服务器，常见的方案是使用Flask+gunicorn+nginx
gunicorn 配合gevent 可以高效代理WSGI应用程序
```shell script
gunicorn -c config.py app:app
```
也可以使用PythonAnyWhere、Heroku、Azure等部署，详情参考：[Deployment Options](https://flask.palletsprojects.com/en/1.1.x/deploying/)

## TODO
1. 首次接触Flask所以app.py写的非常乱，希望有好心人PR
2. 输入过滤在做了，也希望有好心人PR

（我是大懒蛋）
