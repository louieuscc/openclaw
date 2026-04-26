# All about Openclaw with Workbuddy



**一、目录**

Openclaw目录位置：~/.openclaw/



Skill安装位置：~/.openclaw/workspace/skills



Skill的安装：

最佳方法：直接在workbuddy对话框安装，用命令行方式：`install skill named xxx`

不稳定方法：直接拷贝张贴此SKILL文件包至SKILLS目录下，然后重启GATEWAY：

`Openclaw gateway restart`



Weather skill命令:

`curl -s "wttr.in/Beijing?format=3” `  (Check weather status in Beijing)

`curl -s "wttr.in/Chongqing?format=4”`  (Check weather for Chongqing) (format value: 1~4)



**二、Openclaw常用命令**

`openclaw --version  -v`

查看当前安装版本



`openclaw --help  -h`

显示所有可用命令列表



`openclaw tui`

启动终端交互界面



`openclaw dashboard`

打开网页管理控制台，习惯浏览器操作的用户首选



`openclaw restart`

重启 OpenClaw 服务，修改配置后必须执行



`openclaw stop`

停止运行中的服务



`openclaw update`

一键更新到最新版



**三、查看本地Openclaw安全**

我的IP是：

183.69.156.xxx



在CLI输入`openclaw gateway status`可查看当前网关状态。如发现以下内容：

Gateway: bind=loopback (127.0.0.1), port=18789 (service args)

Probe target: ws://127.0.0.1:18789

Dashboard: http://127.0.0.1:18789/

Probe note: Loopback-only gateway; only local clients can connect.



则表明当前为loopback（本地局域），只能本地访问，监听地址为http://127.0.0.1:18789

没有安全问题。如果设置为LAN（所有接口可访问），则较危险。

需输入以下命令更改：

`npm openclaw config set gateway.bind loopback`



**四、Workbuddy常用工作命令**



1. 根据桌面的教学档案存档要求.pdf，把桌面文件夹XXXX中的内容做成教学档案，创建教学大纲、教案、考勤及成绩表、学生作业、教学分析表、结课检查表、教案等子文件夹，把对应的内容放进对应的子文件夹中，并存入桌面的XXXX教学档案U盘文件夹中。



2. 安装某SKILL

在Openclaw对话框，输入:

​		`clawhub install <Skill name>` (此法不稳定，可能会报错)

更新所有已安装的 Skills：

`clawhub update --all`



**五、飞书**

开发者后台地址：https://open.feishu.cn/app



> 飞书App ID: cli_a927f958c278dbb4

> 飞书App secret: zALD0pZ98bANuf1rXuyuEhnuqkl7BUXF
