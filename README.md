## 环境要求
```
python3.6+
virtualenv
```

## 安装项目

```
git clone git@github.com:Nick233333/flask-microblog.git # 克隆项目
cd flask-microblog  # 进入目录
virtualenv --no-site-packages env_name # 创建运行环境
virtualenv -p /usr/local/bin/python3 env_name --no-site-packages # 创建指定运行环境
source env_name/bin/activate # 进入运行环境
pip install -r requirements.txt # 安装依赖
```

## virtualenv 环境变量设置

如果你使用的是 `Windows` ，则需要在下面的每个 `export` 语句中将 `export` 替换为 `set`

本地邮件服务器配置

```
export MAIL_SERVER=localhost
export MAIL_PORT=8025
python -m smtpd -n -c DebuggingServer localhost:8025
```

qq 邮箱服务器

```
export MAIL_SERVER=smtp.qq.com
export MAIL_PORT=25
export MAIL_USE_TLS=1
export MAIL_USERNAME=512817655@qq.com
export MAIL_PASSWORD=xxx
```

框架运行配置

```
export FLASK_APP=microblog.py
export FLASK_DEBUG=1
```

执行数据库迁移，生成数据表

```
flask db upgrade 
```

运行项目

```
flask run 
```

项目配置到此结束。

--- 

## 项目初始化

```
pip3 install virtualenv
mkdir myproject
cd myproject
virtualenv --no-site-packages env_name
source env_name/bin/activate
deactivate
```

数据库迁移

```
flask db init                      //初始化
flask db migrate -m "users table"  //生成迁移文件并添加注释
flask db upgrade                   //执行迁移文件
flask db downgrade                 //回滚上一次迁移
```
`flask db migrate` 命令不会对数据库进行任何更改，只会生成迁移脚本。 要将更改应用到数据库，必须使用 `flask db upgrade` 命令


## 导出依赖

```
pip freeze > requirements.txt
```

## 安装依赖

```
pip install -r requirements.txt
```


