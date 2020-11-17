## I. Overview {#1}

1\) SQL injection generally means to trigger background execution of SQL query through malicious parameter input, to obtain data or damage the database.

2\) Anti-SQL Injection is aimed to prevent SQL injection by following methods:

* Disable special keywords.

* Escape some characters.

Note: this feature only works for the FineReport templates.

## II. Instructions {#3}



### 1. User Interface

ClickManage -&gt; Security -&gt; Anti-SQL Injectionand enter this page, as shown below:

![](https://help.fanruan.com/finereport-en/uploads/20201012/1602494439559200.png "1602494439559200.png")

  




### 2. Special Keywords

**1\) Enable special keywords**  


Forbid Keywordsoption is enabled by default:

![](https://help.fanruan.com/finereport-en/uploads/20201012/1602493700818766.png "1602493700818766.png")

Note: an error message will be thrown into the log when a disabled character is present in SQL parameters.

**2\) Add special keywords**

* Click onEdit belowForbid Keywordsswitch to add new keywords or delete custom ones. Click on selected keywords to change it as unselected keywords, and vice versa.

![](https://help.fanruan.com/finereport-en/uploads/20201012/1602493702310415.gif "1602493702310415.gif")

* ClickAdd Special Keywords to add custom keywords.

  Note: custom keywords can be removed.

![](https://help.fanruan.com/finereport-en/uploads/20201012/1602493702225754.gif "1602493702225754.gif")一、概述

1）有关定时调度功能基本的介绍和操作方法可以参见文档：定时调度介绍

2）定时调度任务设置时有四个操作步骤，如下图所示。本文将详细介绍这四个操作步骤中的设置项。

![](https://uploader.shimo.im/f/nm477s6lzUlBGkWX.png!thumbnail)

## 二、添加任务

管理员进入数据决策系统，点击\[管理系统\]&gt;\[定时调度\]&gt;\[添加任务\]，可以新建定时任务。如下图所示：

注：普通用户若需要设置定时调度任务，需要管理员开启\[分级授权\]后，为其分配\[定时调度\]管理页面的\[查看\]权限，具体步骤请参见分级权限设定

