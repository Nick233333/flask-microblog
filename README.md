环境要求
```
python3.6+
virtualenv
```

项目初始化

```
pip3 install virtualenv
mkdir myproject
cd myproject
virtualenv --no-site-packages env_name
source env_name/bin/activate
deactivate
```

导出依赖

```
pip freeze > requirements.txt
```

安装依赖

```
pip install -r requirements.txt
```
