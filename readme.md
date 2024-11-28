socks5 一键搭建代码 bash <(curl -sL https://raw.githubusercontent.com/moneyfly1/socks5/main/socks5.sh)

如果上面的失效请用别的大佬写的代码：
 稳定版V3.0
介绍
基于nps的Shell脚本，集成socks5搭建，管理，启动，添加账号等基本操作。方便用户操作，并且支持快速构建socks5服务环境。

默认管理页面ip:18080
默认管理员账号密码:admin admin
默认socks5账号信息:账号socks5 密码socks5 端口5555
支持多端口、多账号管理
加密传输、数据压缩
服务端、客户端分离安装、可实现国内中专代理，降低被和谐概率
脚本只提供学习交流，请在法律允许范围内使用！！！！
image image
系统支持
contest、ubuntu、debian
windows(需要自行编译)
功能
全自动无人值守安装，服务端部署只需一条命令
全新的web端管理，支持多端口、多账号、多服务器、以及中转代理
添加账户、删除用户、开启账户验证、关闭账户验证、一键修改端口
方法一：一键安装或更新到最新
wget -q -N --no-check-certificate https://raw.githubusercontent.com/wyx176/nps-socks5/master/install.sh && chmod 777 install.sh && bash install.sh
方法二:linux、windows均支持，需要安装go语言环境进行编译
参考NPS文档
1、安装源码

go get -u github.com/wyx176/nps-socks5
2、编译服务端：进入到nps-socks5文件夹中执行命令

go build cmd/nps/nps.go
3、编译客户端：进入到nps-socks5文件夹中执行命令

go build cmd/npc/npc.go
相关文件路径、命令
1、后台管理的配置文件
/etc/nps/conf
登录账号web_username=admin
登录密码web_password=admin
web管理端口web_port = 18080
修改后需要重启服务端
2、基本命令
启动服务端： nps start
停止服务端： nps stop
更新日志
-2022.10.06 v3.0
1、端口增加创建时间、到期时间
2、开启用户注册
安装后修改/etc/nps/conf/nps.conf中
allow_user_login=true
allow_user_register=true

-2022.10.03 v2.0
1、增加多端口、多账号设置
-2022.09.03 v1.0
