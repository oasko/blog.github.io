---
title: Windows Fundamentals 1~3教程
date: 2025-01-18 08:47:40
tags: windows 基础
top_img: transparent
cover: https://s2.loli.net/2025/01/19/MHICLXqONb38YnW.png
---
现在搞一个比较简单的windows Fundamentals 其实Windows我也是学习中 基本的功能也算半桶水

## windows基本功能1
现在是windows基本功能1 只能说基础 得打牢

就是了解了解windows的功能 各种系统自带的程序的作用

![1](/images/Windows%20Fundamentals%201教程/1.png)


### task2
task2就跳过了 无法启用bitlocker

### task3
讲的是桌面的组成 桌面又称为图形用户界面或简称GUI

分为一下几个部分
- 桌面
- 开始菜单
- 搜索框（Cortana）
- 任务视图
- 任务栏
- 工具栏
- 通知区域

我们看看问题
![问题](/images/Windows%20Fundamentals%201教程/task3.png)

其实这些问题很容易 就是吃了不太懂这些东西的英文叫啥

#### 问题一 如何隐藏/禁用搜索框

右键点击下方的空白处 调出任务栏 点search搜索 就会有个隐藏

![任务栏](/images/Windows%20Fundamentals%201教程/hidden.png)

#### 问题二 隐藏任务视图 
 
还是那个地方 任务视图叫task view 点击show task view button

![task](/images/Windows%20Fundamentals%201教程/show%20task.png)

#### 问题三 还有哪些图标

在时间和网络的旁边 有个小框框 那个就答案 名字叫做action center

![tu](/images/Windows%20Fundamentals%201教程/action.png)

### task4
ntfs叫做**New Technology File System**

### task5
windows文件夹系统变量%windir%

### task6

![task6](/images/Windows%20Fundamentals%201教程/task6.png)

看到有用户 账户 我们直接cmd 输入**lusrmgr.msc** 

![user](/images/Windows%20Fundamentals%201教程/other.png)

一下子找到另一个用户和他的描述 第一题第四题解决
另一个账户叫**tryhackmebilly** 描述是**window$Fun1!**

点击tryhackmebilly账户 我们选到有member的选项

![group](/images/Windows%20Fundamentals%201教程/mumer.png)

发现是属于remote desktop user和user的用户

内置账户可以用于访问访客计算机 当然是guest用户

## task7
uac是user account control 用户账户控制

## task8

cmd 输入**control** 进入控制列表 选择类别 小图标 最后一个是Windows defender firewall

![control](/images/Windows%20Fundamentals%201教程/small.png)

## task9

打开任务管理器的键盘快捷键是什么

ctrl+shift+esc


 ## windows基本功能2

接下来是windows基本功能2

![2](/mages/Windows%20Fundamentals%202教程/2.png)


## task2

我们看看题目

![task2](/images/Windows%20Fundamentals%202教程/task2.png)

我们cmd输入**msconfig** 系统配置

### 第一题
题目是说服务 我们点开services 点一下manufacturer筛选一下 从底部开始显示 一下子就能找到 Systems Internals的服务是**psshutdown**

![msc](/images/Windows%20Fundamentals%202教程/man.png)

### 第二题
题目说是Windows 我们在tool里面看 关于Windows **about Windows**点击之后点一下下面的launch

![windows](/images/Windows%20Fundamentals%202教程/windowsuser.png)

### 第三题

Windows排除故障 我们还是在在系统配置中的tools中找到troubleshooting 点击一下 下方就有显示具体的程序

![](/images/Windows%20Fundamentals%202教程/trub.png)

### 第四题
控制面板就不用多说 不用想都是control 我们真要去系统配置找的话 我们就依然在tools中找到control

![contorl](/images/Windows%20Fundamentals%202教程/control.png)



## task3
我们也是在系统配置的tools进行查找
可以发现是**UserAccountControlSettings.exe**

![task3](/images/Windows%20Fundamentals%202教程/uac2.png)

## task4

我们看一下题目吧

![task4](/images/Windows%20Fundamentals%202教程/task4.png)

### 第一题

第一题和之前的一样在系统配置中的tools找计算机管理 **computer management**

![man](/images/Windows%20Fundamentals%202教程/compmgmt.png)

### 第二题

这题我们要打开计算机管理的任务计划程序 在里面找到题目要求的程序 发现是6:15am

![ua](/images/Windows%20Fundamentals%202教程/ua.png)

### 第三题
我们在这个界面找到共享文件夹 点进去就可以发现答案

![share](/images/Windows%20Fundamentals%202教程/share.png)

## task5
![task5](/images/Windows%20Fundamentals%202教程/task5.png)

### 第一题和第二题

我们又又又又在在系统配置中查找system infomation 找到之后单击launch 就可以找到第二题答案

![diyiti](/images/Windows%20Fundamentals%202教程/msinfo32.png)

### 第三题

环境变量就在系统信息中 在cmd中输入**msinfo32** 进入系统信息 找到software enviroment的enviroment variables 就能看到ComSpec的值

![disanti](images/Windows%20Fundamentals%202教程/envir.png)

## task6

在系统配置中的tools能找到 Resource Monitor

![task6](/images/Windows%20Fundamentals%202教程/remon1.png)

## task7

这个题目比较ez

![task7](/images/Windows%20Fundamentals%202教程/task7.png)

ipconfig 要展示所有细节的话 在后面加/ all

```
ipconfig /all
```

## task8

这一题方法与task7 第一题题方法一致


## windows基本功能3

总算来到了最后一个了 速战速决

### task2

![task1](/images/Windows%20Fundamentals%203教程/task1.png)

第一个他问定期更新的时间是多少？我们打开设置点击更新
![1](/images/Windows%20Fundamentals%203教程/1.png)

点开更新历史 就能发现日期
![2](/images/Windows%20Fundamentals%203教程/2.png)

### task3

很幸运 任务二也只有一道题
![task2](/images/Windows%20Fundamentals%203教程/task2.png)

打开设置找到Windows security这个选项 你就可以发现答案

![task22](/images/Windows%20Fundamentals%203教程/proten.png)

### task4

![task4](/images/Windows%20Fundamentals%203教程/task4.png)

一开始看这道题看得一头雾水的 不知道说啥 先不管他 我们上面已经打开了virus&threat protection

![4](/images/Windows%20Fundamentals%203教程/dakai.png)

接着点开manage setting 就会发现就是实时保护(real-time protection) 
本人因为我的世界就被这个老六sha掉了 害我的存档之间没了

![4](/images/Windows%20Fundamentals%203教程/dakai2.png)

### task5
![task5](/images/Windows%20Fundamentals%203教程/task5.png)

机场wifi毫无疑问就是公共网络 public network

### task6

就是给你读的 

讲了Microsoft Defender SmartScreen的作用

### task7
tpm就是Trusted Platform Module

### task8

BitLocker 与受信任平台模块 (TPM) 一起使用时可提供最大程度的保护

BitLocker 驱动器加密是一种与操作系统集成的数据保护功能，可解决因计算机丢失、被盗或不当退役而导致的数据盗窃或泄露威胁

![task8](/images/Windows%20Fundamentals%203教程/task8.png)

我们查看微软官方文档可以知道 没有tpm的需要准备a startup key

![8](/images/Windows%20Fundamentals%203教程/8.png)

### task 9

卷影复制服务 (VSS) 协调所需的操作来创建要备份的数据的一致卷影副本（也称为快照或时间点副本）。 

卷影副本存储在每个启用了保护的驱动器上的系统卷信息文件夹中。

如果启用了 VSS(打开了系统保护)，您可以在高级系统设置中执行以下任务。 

- 创建还原点
- 执行系统还原
- 配置恢复设置
- 删除还原点

![9](/images/Windows%20Fundamentals%203教程/9.png)


终于我们把所有的Windows function搞完了 基础篇 不难 主要是给我们熟悉一下操作和常用的程序 Windows安全工具 可以用来检查安全事件