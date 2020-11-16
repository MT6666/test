# First Chapter

## 一、概述

在使用 FR 数据决策系统时，一般流程是先在测试环境系统上进行开发部署，确认无误后再迁移到正式系统中；而之前只支持平台配置从测试系统到正式系统上的全量迁移，不能满足两者系统存在差异的情况。因此，10.0 中新增支持报表文件及平台配置从测试系统到正式系统的增量迁移。

## 二、步骤

### 1、进入资源迁移界面

1\) 通过设计器\[服务器\]&gt;\[平台管理\]进入本地决策平台

![](https://uploader.shimo.im/f/mmi6FmsQuT6Q6VPc.png!thumbnail)

2\) 通过\[管理\]&gt;\[智能运维\]&gt;\[资源迁移\]进入内存管理界面

![](https://uploader.shimo.im/f/HLCsHMb6d8IHeRTj.png!thumbnail)

### 2、资源导出

1\)资源类型默认为目录，可选的内容包括挂载在系统目录中的各个节点及其权限配置。

![](https://uploader.shimo.im/f/ajtMjDUqTRh0ynSm.png!thumbnail)

2\)勾选想要导出的目录资源，并选择是否“同时导出权限配置”，导出文件（包括节点、节点设置、权限信息）到本地。文件名默认为：resource.zip。

![](https://uploader.shimo.im/f/ZwTqQIXkSjk05zty.gif)

### 3、资源导入

![](https://uploader.shimo.im/f/RMX2iMtp7dxoXfrt.png!thumbnail)

注：资源导入前建议进行系统备份，其中备份迁移到的 MySQL 数据库需要选择 utf8\_bin 的排序规则。

* 单次只允许上传单个压缩文件。
* 系统会获取导入文件所包含的资源，包含文件类型、平台路径、物理资源、权限信息及导入方式。

尝试将步骤2中导出的资源导入：

![](https://uploader.shimo.im/f/L7KPwKQnN33aIAxm.gif)

* 冲突检测：

在导入时，系统会对资源进行检测，检测是否与系统现有资源有冲突，冲突检验以资源的原始名与其在平台中的路径名为准。若导入的数据在系统中有冲突，导入方式会显示为覆盖导入且置为未勾选状态；若与系统中已有资源没有冲突，则会显示直接导入且置为选中状态。点击![](https://uploader.shimo.im/f/Ozc96ql8Oacuruon.png!thumbnail)按钮可以查看到详细说明。

![](https://uploader.shimo.im/f/q4IIcQNSiiGem8zj.gif)

* 路径缺失情况：自动创建完整路径。
* 权限信息：点击“详情”可查看权限信息，其中会提示是否有部门/角色/用户在被导入系统中的缺失情况。
* 若导入失败，显示失败的原因（如：导出工程和导入工程中存在同名同路径但是类型不同）；若导入成功，则资源即时生效。

![](https://uploader.shimo.im/f/Ioc70uS6Q50lOqNq.gif)

3\)模板具体信息默认按照\[开始时间\]升序排列。支持选中后手动杀死会话。比如，结束会话\[Detail Report A\]。存活会话数变更为2，近10分钟内新增会话数变更为2，近10分钟内结束会话数变更为1。

![](https://uploader.shimo.im/f/b2Mou7gYMgsu4URO.gif)

### 5、智能释放

1\) 智能释放默认开启

2\)释放机制

* * * 负载判断：使用基于 JVM 底层原理开发的负载判断算法，
      能及时、准确地判断
      系统负载。
    * 动态释放：不需要用户设置各项阈值，系统根据负载状态智能地选择最合适的释放策略，保障系统稳定运行的同时，尽可能降低对用户的影响。

![](https://uploader.shimo.im/f/oUcajKwOAlCnGki7.png!thumbnail)

### 6、模板限制-通用限制![](https://uploader.shimo.im/f/eknxfx5BLQkvrshS.gif)

![](/assets/gif短.gif)

