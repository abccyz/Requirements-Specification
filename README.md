# 需求规格说明书：2017秋季 软件工程 团队作业 需求规格说明书

# 1.引言

## 1.1.编写目的

## 1.2.项目背景

## 1.3.预期的读者和阅读建议

## 1.4.项目范围

## 1.5.参考资料

# 2.总体描述

## 2.1.目标

### 2.1.1.开发背景

当前社团的各方面管理工作主要都由手工完成，对社团管理人员而言，工作量庞大，机械重复性强，冗余而繁琐。同时，大量重复工作也容易出现纰漏，可能造成资源的浪费，耗时耗力却可能达不到好的效果。对社团成员而言，信息碎片化缺少管理，可能导致信息的延迟、遗漏。

一个合理有效的社团管理系统能够从一定程度上简化当前重复性的工作方式，减轻管理人员的工作量，并提高效率，减少纰漏，帮助管理人员更好更快地管理社团。同时，社团系统的综合使得信息更为集中化，能为社团成员提供方便快捷的途径参与社团活动。因此，社团系统的开发与维护成为需求的一部分。

### 2.1.2.开发意图

减轻社团管理人员的工作量，为他们提供更高效的管理方式；整合集结社团相关信息，让社团成员更方便地参与社团活动。同时，通过团队合作的方式，学习体验与他人沟通、磨合，培养团队意识。在做中学，在实践中提高姿势水平。

### 2.1.3.应用目标和作用范围

该系统面向高校社团的高层管理人员以及全体部员，当前阶段主要是面向福州大学内的社团。该系统为独立的系统，用于社团管理，与其他系统没有关联。

### 2.1.4.产品前景

TODO

## 2.2.用户特点

### 2.2.1.最终用户及特点

本项目用户主要有以下三类：社团管理人员、社团积极成员、社团消极成员。这三种成员分别具有如下特点：

(1)社团管理人员使用本项目的主要目的在于：
- 根据部员的空闲时间信息，得到潜在可行的活动安排日期；
- 得到部员生日信息，辅助活动日程安排；
- 日常通知部员部门内部活动信息；
- 对本部门进行人员管理；
- 进行活动签到；
- 对本部门进行人员出勤管理。

(2)社团积极成员使用本项目的主要目的在于：
- 查看部门活动通知；
- 回复部门活动通知。

(3)社团消极成员使用本项目的主要目的在于：
- 查看部门活动通知；
- 请假。

### 2.2.2.软件使用频率

对于部门管理人员，需要一天多次访问APP，以进行部门日常活动管理；
对于部员，一天内同样也需要多次访问APP，以查看部门所推送的消息，举行活动时进行活动签到。

### 2.2.3.用户场景

**1、背景：**

**1) 典型用户**

(1)社团管理者小鹿：

| 姓名 | 鹿含 |
| ----- | ----- |
| 年龄 | 21岁 |
| 代表的用户在市场上的比例 | ~30% |
| 重要性 | 很重要，对于是否使用APP进行社团管理有决定权 | 
| 生活/工作情况 | 在校学生，目前是某大型社团领导人 |
| 知识层次和能力 | 本科生，离不开手机，日常频繁通过手机与他人进行通信；平时还需要通过PC端Excel做表格 |
| 用户偏好 | 社交管理 | 
| 典型场景 | 通过手机群发部门活动短信，组织部门活动，确认大家都收到信息了 | 
| 典型描述 | 部门存我存，部门亡我亡 |

(2)社团积极成员晓彤：

| 姓名 | 管晓彤 |
| ----- | ----- |
| 年龄 | 18岁 | 
| 代表的用户在市场上的比例 | ~60% |
| 重要性 | 社团管理APP的主要用户 |
| 生活/工作情况 | 在校学生，国民闺女 |
| 知识层次和能力 | 本科生，平时通过手机上网，QQ、微信聊天，还喜欢刷刷微博热门 |
| 用户偏好 | 跳舞，聊天 |
| 典型场景 | 听从小鹿学长指挥，积极参与社团活动 |
| 典型描述 | 听帅气部长的话 |

(3)社团消极成员程祥：

| 姓名 | 程祥 | 
| ----- | ----- |
| 年龄 | 20岁 |
| 代表的用户在市场上的比例 | ~10% | 
| 重要性 | 社团管理APP的主要用户 |
| 生活/工作情况 | 在校学生 |
| 知识层次和能力 | 计算机专业学生，使用电脑的频率高于使用手机的频率 |
| 用户偏好 | 平时热爱运动，喜欢踢足球，喜欢各个方面都插足 | 
| 典型场景 | 消息很晚才回，经常请假 | 
| 典型描述 | 我的时间非常宝贵，那这次部门活动/今天的课还是不去了吧 |

**2) 用户的需求 / 迫切需要解决的问题**

社团管理者小鹿：
- 每次组织活动都需要收集每个部员的空闲时间，从而再推导得到活动的具体时间和安排；
- 活动开始前，要通过群发短信逐个部员通知，并确认谁到场谁缺席；评选部门之星时需要根据部员出勤率找出优秀部员，因此需要在PC端记录出勤信息，非常麻烦；
- 需要记录部员的请假信息，有时候是QQ的信息，有时候是微信的信息，忙着忙着就忘记了谁请假，询问时才回想起来；
- 在考虑活动的时候，需要根据部员的一些信息来进行组织，比如当月有好多个同学过生日，就可以组织一个大趴体来庆祝一下，但是这些信息一条条记录到excel里面要花费不少的精力和时间；
- 举办活动当天有时候还需要签到，来确定奖品、综测发放的名额。

社团积极成员晓彤：
- 每周都要把自己当周的课表、空闲时间发给小鹿学长，好烦。

社团消极成员程祥：
- 有的时候会忘记回复小鹿学长发过来的信息，他打电话过来确认的时候再请假好不好意思啊。

**3) 假设**

APP的基本功能均已实现。基本功能包括：
- 活动安排；
- 生日提醒；
- 活动发布；
- 考勤审核；
- 部员管理；
- 消息；
- 请假；
- 活动签到。

**2、场景：**

小鹿发现最近成员们的参与社团热情度有所减弱，决定组织一波吃喝玩乐的活动来收拢人心。说干就干，他打开了部门管理APP，输入了他的账号及密码，一旦他的账号密码输入错误，会被错误提醒。接着，小鹿选择进入他管理的A部门，在生日提醒模块逐月查看了大伙的生日，发现十一月份过生日的人有点多，于是决定挑选十一月份的某一天来举行大趴体。

他进入到活动安排模块，选择十一月，该模块便根据十一月份每个部门成员的课表，生成并列举了一些可行的活动日期。在和部门的其他核心骨干商量之后，决定在11.23号这天来举办大趴体。于是乎，他来到了活动发布模块，为了给过生日的同学一个惊喜，小鹿选择只告诉他们是举办一次部门例会，于是编辑了两种不同的信息安排。在依次输入活动安排时间、地点、描述以及选择发送对象之后，他可以选择退出编辑、保存不发送以及保存并发布。小鹿选择了发布活动信息，APP会判断通知的完整性，必要时进行提示。

管晓彤同学在上课时收到了部门APP的推送，兴致勃勃的她进入A部门，打开消息模块点开小鹿的消息，发现马上有一次关于吃吃吃的活动要举办了，而且举办的时间没有冲突，有两个按钮供晓彤选择，确认回复和请假，她点击确认回复按钮表示自己收到了这条信息。管晓彤确认之后，小鹿在消息模块中立即收到了来自她的确认。在所有人确认回复之后，小鹿能够在活动安排模块查看到这次活动的详细信息，如确认到场人数、缺勤人数，以及活动地点和时间。

活动前夕，小鹿根据人数定制了一个大蛋糕，并进入消息模块，查看本次活动并点击再次提醒按钮，编辑信息并确认发送，以提醒部员们。晓彤收到信息推送之后，进入活动提醒模块设置了这次活动的闹钟，并带着满满的期待点击了确认。而A部门的另一个成员程祥觉得那天自己没有时间，又不知道是给自己举办的趴体(推送通知说是"一次组会")，于是乎在请假模块选择了该活动，随便填写了信息点击申请。小鹿在消息模块看到程祥的申请提醒之后，叹了口气，来到考勤审核模块确认并批准了他的事情，系统提醒程祥的缺勤次数以及超过上限，小鹿发现程祥的缺勤次数早已超过了6次，于是下定决心，点击了旁边的移除该部员按钮，系统显示"程祥同学已被列入潜在移除名单，详细操作请进入部员管理模块"字样，并提供了"确认"、"取消"按钮，小鹿选择了确认，并进入部员管理模块，点击进入潜在移除名单，找到程祥同学的信息，点击红色的移除该部员按钮，并编辑移除信息，点击确认，系统提示"本次操作将从您的部门中移除程祥同学，操作后不可恢复，请问确认要执行该操作吗？"，小鹿点击确认。

活动时间当天，小鹿早早的来到了会场，精心布置了一番，并进入A部门的活动签到模块，开启本次活动的签到模式。晓彤来到会场之后，打开APP的活动签到模块，并点击签到。活动快开始了，小鹿进入活动签到模块，发现还有两三个人还没有签到，于是点击提醒按钮，编辑信息并发送对还没有到场的同学进行了催促。

趴体举办地很成功，小鹿进入部门A的活动安排模块，选择该活动点击结束，系统弹出本次到场总人数、缺勤总人数，并列举了缺勤的同学信息，提供"确认到场"按钮以防止同学忘记签到的情况，对于缺勤的同学，系统在考勤审核模块记录了本次缺勤的情况。

### 2.2.4.用例图

## 2.3.假定与约束

### 2.3.1.假定

### 2.3.2.约束

## 2.4.运行环境

# 3.界面原型

# 4.系统功能描述及验收验证标准

## 4.1.对功能的约定

## 4.2.对性能的约定

### 4.2.1.精度

### 4.2.2.时间特性需求

### 4.2.3.灵活性

## 4.3.输入输出要求

## 4.4.数据管理能力要求

## 4.5.其他要求

### 4.5.1 安全性

- 1.利用可靠的加密技术对重要信息进行加密。防止用户信息、密码的泄露。
- 2.采用日志记录。记录系统运行时发生的错误，便于查找系统故障原因。记录用户关键性操作信息。

### 4.5.2 可用性

- 1.使用方便。界面体验良好，操作简单方便。
- 2.系统稳定。系统不存在太多不稳定因素，即时修复bug,更新增加功能。
- 3.交互良好。操作时有提示信息，如进行添加删除等更改性操作时提示确认操作信息。
- 4.系统具有一定的容错能力。在非硬件故障、非网络故障时系统应保证正常运行。
- 5.系统能保证一定量用户同时在线使用而不崩溃。

### 4.5.3 可维护性

- 1.合理架构，保留各版本代码。
- 2.代码需要有一定的注释，但不要轻易注释，在关键处简洁提示思路。
- 3.遵守同一套命名规范、代码规范，注意接口的设置，方便后期的系统维护和迭代更新。
