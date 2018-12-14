一键脚本安装shadowsocks
支持系统
CentOS 6+

Debian 7+

Ubuntu 12+

一键搭建shadowsocks
在购买VPS并用Xshell连接上你刚购买的VPS后，你将看到如下图所示的界面：

如红框中所示，root@vult（root@ubuntu）说明已经连接成功了，之后你只需要在绿色光标处直接复制以下代码就可以了（直接复制即可，如每段代码下方截图中所示）。

1.下载一键搭建ss脚本文件（直接在绿色光标处复制该行命令回车即可，只需要执行一次，卸载ss后也不需要重新下载）


git clone https://github.com/caralr/ss-wink

如果提示bash: git: command not found，则先安装git：


Centos执行这个： yum -y install git
Ubuntu/Debian执行这个： apt-get update && apt-get -y install git
1
2
Centos执行这个： yum -y install git
Ubuntu/Debian执行这个： apt-get update && apt-get -y install git
2.运行搭建ss脚本代码


ss-fly/ss-fly.sh -i caralr.club 2333

其中caralr.club换成你要设置的shadowsocks的密码即可 
这个caralr.club就是你ss的密码了，是需要填在客户端的密码那一栏的），密码随便设置，
最好只包含字母+数字，一些特殊字符可能会导致冲突。而第二个参数2333是端口号，也可以不加，不加默认是2333
