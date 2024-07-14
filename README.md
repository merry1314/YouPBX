# YouPBX
A great GUI manager for FreeSwitch

# 概述

YouPBX 是一个强大 FreeSwift (电话软交换系统) 的管理GUI系统，基于Django开发，功能全面，体验友好，可以基于此项目做一个完善的IPPBX系统、呼叫中心应用等

# 使用

1. git clone https://github.com/JoneXiong/YouPBX.git
2. cd YouPBX安装依赖包
   #配置pip
   cat ~/.pip/pip.conf 
   [global]
   index-url = http://mirrors.aliyun.com/pypi/simple/
   [install]
   trusted-host = mirrors.aliyun.com
 
   #安装依赖的包
 
   pip install pip==20.3.4
 
   pip  install requests
 
   pip install -r requirements.txt

3. 项目界面框架用的 [DjangoX](https://github.com/JoneXiong/DjangoX), 请拷贝xadmin包到运行根目录
   
   git clone https://github.com/JoneXiong/DjangoX.git
   cp -rp Django/xadmin YouPBX/
   
4. cp config_sample.py config.py 编辑配置freeswitch的连接信息
5. 执行Django migrations命令 初始化数据库，执行Django createsuperuser创建管理员账号

   python manage.py migrate
   python manage.py createsuperuser
   
6. python manage.py runserver 0.0.0.0:8080 运行服务
7. 浏览 http://localhost:8080/


# 预览
![info](https://github.com/JoneXiong/YouPBX/raw/master/apps/base/static/base/images/youpbx0.jpg)

![info](https://github.com/JoneXiong/YouPBX/raw/master/apps/base/static/base/images/youpbx1.jpg)

![info](https://github.com/JoneXiong/YouPBX/raw/master/apps/base/static/base/images/youpbx2.jpg)
