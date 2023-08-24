# Ansible-入门


## 核心概念  intro：
Ansible是一种自动化的运维工具，基于Python开发，能够实现批量操作linux主机。 

　　1、部署简单，只需在主控端部署ansible环境，被控端无需做任何操作;

　　2、默认使用SSH协议对设备进行管理;

　　3、有大量常规运维操作模块，可实现日常绝大部分操作;

　　4、配置简单、功能强大、扩展性强;

　　5、支持API及自定义模块，可通过Python轻松扩展;

　　6、通过Playbooks来定制强大的配置、状态管理;

　　7、轻量级，无需在客户端安装agent，更新时，只需在操作机上进行一次更新即可;

　　8、提供一个功能强大、操作性强的Web管理界面和REST API接口-AWX平台



## 安装  Installation：
在管理端机器 安装ansible的软件 （windows不合适）

1 CentOS (Yum)

  * 添加 epel-release 第三方套件來源
```
$ sudo yum install -y epel-release
```
  * 安裝 Ansible
```
$ sudo yum install -y ansible
```

2 Ubuntu (Apt)

```
$ sudo apt update
$ sudo apt install software-properties-common
$ sudo apt-add-repository --yes --update ppa:ansible/ansible
$ sudo apt install ansible
```

3 vagrant （virtualbox）
基于虚拟机方式，创建一个管理机和二个node节点，可实现各类ansible的应用操作和练习   

安装只需要以下二个文件及安装了vagrant软件

 * Vagrantfile 

 * setup.sh

```
vagrant up   #创建虚拟机 调用vagrantfile和setup.sh
vagrant ssh name-box # 登录虚拟机
```


安装后默认为基于密钥登录 实现免密登录