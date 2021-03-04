# -This project is developed using Tuya SDK, which enables you to quickly develop branded apps connecting and controlling smart scenarios of many devices.For more information, please check Tuya Developer Website.
# 项目概述
======
>>本方案旨在研究基于涂鸦三明治 Wi-Fi MCU 通信板和移动应用APP的智能物联宠物喂食器。
>>采用基于涂鸦三明治 Wi-Fi MCU 通信板作为主控的智能终端。智能终端通过wifi模块与服务器进行socket通讯，移动应用在WIFI连通的情况下，通过Http请求至服务器完成对于信息的查询和任务的设定，并通过云服务器的桥接实现了智能喂食的控制。
# 项目系统框图
====
## 硬件部分
===
![image](https://user-images.githubusercontent.com/80017125/109914281-917cd180-7cea-11eb-9d8b-01b4e114e296.png)

模块需要具有自身计时的功能，从而能够实现基于时间的控制；
模块需要有一定的检测功能，需要能够接驳一些传感器，便于后期功能的拓展，实现闭环控制；
	模块需要能够接入互联网，实现同服务器的通信，从而实现远程的设置、控制与监控
## 软件部分
整个APP的功能可以分为用户管理、设备管理和场景管理三部分。通过用户管理，可以实现用户的登录、注册、密码找回、信息管理等操作。设备管理功能包括设备的查看、添加、删除、控制等功能，并可以查看设备控制的历史记录。通过场景管理，可以添加和使用场景，并在场景中自定义任务的执行。
>>APP主要分为设备、场景、个人三个模块。主界面采用底部标签栏的结构，可以通过底部标签栏或者页面之间的滑动进行三个模块的切换。 
>>APP通过http协议与服务器进行通信，通信的方式以post为主。
>>移动应用具有查看设备的历史信息以及当前状态，同时能够根据该用户已有的设备设定定时或者实时的控制任务组。
