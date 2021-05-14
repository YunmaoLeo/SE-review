## Menu
- [Menu](#menu)
- [Lecture 02 Git projects](#lecture-02-git-projects)
  - [git](#git)
- [Lecture 03 Requirements](#lecture-03-requirements)
  - [SE Processes:](#se-processes)
  - [Requirements Elicitation 需求启发](#requirements-elicitation-需求启发)
  - [Stakeholder Analysis](#stakeholder-analysis)
  - [Personas:](#personas)
  - [``Use Case Diagrams``](#use-case-diagrams)
  - [User Stories](#user-stories)
- [Lecture 04 Requirements Gathering](#lecture-04-requirements-gathering)
  - [Documenting  Requirements](#documenting--requirements)
  - [Non-Fcuntional Requirements](#non-fcuntional-requirements)
- [Lecture 05 RequirementsModeling](#lecture-05-requirementsmodeling)
  - [UML - Key Diagram Types](#uml---key-diagram-types)
  - [Context Diagram:](#context-diagram)
  - [Activity Diagrams](#activity-diagrams)
  - [Use Case Modeling & Sequence Diagrams](#use-case-modeling--sequence-diagrams)
  - [Scenarios](#scenarios)
- [Lecture 06 Requirements Validation](#lecture-06-requirements-validation)
  - [Requirements/Specification Documents](#requirementsspecification-documents)
  - [Requirements Validation](#requirements-validation)
- [Lecture 07 Specifications](#lecture-07-specifications)
  - [Specification](#specification)
  - [Specification review](#specification-review)
- [Lecture 08 Prototypes](#lecture-08-prototypes)
  - [Prototyping Risks](#prototyping-risks)
- [Lecture 09 OODesignAndTestPlan](#lecture-09-oodesignandtestplan)
  - [Class Description Documents](#class-description-documents)
  - [Test Plans](#test-plans)
  - [Test Plans的用处](#test-plans的用处)
  - [Overall Document of Test Plans](#overall-document-of-test-plans)
  - [Types of test plans:](#types-of-test-plans)
- [Lecture 10 Implemetation & Debug](#lecture-10-implemetation--debug)
  - [Key Concerns for SE Dev:](#key-concerns-for-se-dev)
  - [Comment-Driven Development](#comment-driven-development)
  - [Bug trackers](#bug-trackers)
  - [Debugging](#debugging)
  - [Paired Coding](#paired-coding)
## Lecture 02 Git projects

### git
+ ``.gitignore``
  + a list of types of files that git will ignore
  + 这允许我们只让git管理源代码文件，忽略掉那些``.exe``什么的
  + 同样可以忽略掉个人文件，比如一个``.txt``文本
+ ``git tag -a v1.2 -m "Version 1.4"``
+ ``Milestones, issues, lables``
  + 可以使用``milestones``里程碑来跟踪进程``track progress``
  + 可以把里程碑和``issues`` ``pull request``结合在一起

## Lecture 03 Requirements

### SE Processes:
+ Specification: design the system for the customer 为客户设计系统
+ Development: production of the software system  制作软件系统
+ Validation: checking that the software is what the customer wanted 验证软件是客户需要的
+ Evolution: 根据客户的新需求修改代码


### Requirements Elicitation 需求启发
+ 1. Requirements discovery 需求探索
+ 2. Requirements classsification and organization 需求分类和汇集
+ 3. Requirements prioritization and negotiation 需求优先次序和negotiation
+ 4. Requirements Definition 需求定义

+ Initial methods
  + Personas & user profiles
  + Requirements gathering
  + Task analysis
  + Contextual enquiry / ethnography

### Stakeholder Analysis
+ Identify:
  + Primary stakeholders
  + Secondary stakeholders
  + Tertiary stakeholders

### Personas:
+ 代表一个真正类别的用户``from your stakeholders``
+ 主要意图：``Personas``应该能够把stakeholders区分开来
+ Identify：
  + motivations
  + expectiations
  + goals
  + knowledge
+ 并不是真正的某一个人
+ 为核心的使用类别是做两到三个personas
+ Stop desginers designing for themselves

### ``Use Case Diagrams``
+ 阐述stakeholders会怎么做
+ use case diagrams 代表了系统的使用者会怎么执行tasks
+ 其中我们通常把使用者称作``actors``
+ A use case can be an ``extension`` of a task（应该首先完成）
  + Consultant ---- Record Consultancy Visit <-----(extend) Record Consultancy Expence
+ ``include``
  + Senior Consultant ---- Conclude Consultancy Project结束咨询项目 ------> Invoice Customer 开发票

### User Stories
+ 现在有了使用者和Use case，现在整合他们，并添加行为的原因
+ ``As a <role>, I want <goal/desire> so that <outcome>``
+ `As an employee, I want to know how to write good stories so that I can submit cards to the planning game that are clear and will be accepted in the next iteration`
+ 优点：
  + 简洁清晰
  + ``little maintenace``
  + ``creates a clear requirements checklist``
  + 将项目拆分成了不同的模块chunks
+ 缺点：
  + 很难在大型的项目中使用
  + 忽略了细节和formality
  + 没有描述流程或者是任务

## Lecture 04 Requirements Gathering

### Documenting  Requirements
+ User requirements: What a stakeholder needs to be able to do
  + `一个课程负责人需要能够查看一个学生是否有先修课的知识`
+ System specification: What the software must do to meet the requirement above
  + `课程负责人应该能够查看想要报这门课的学生的名单列表`
  + `课程负责人要能够看到报名这门课的学生的成绩`
+ user requirement是系统使用者``希望能够实现的功能``
+ specification是系统针对使用者的需求 设计的``系统应该实现的功能``

+ Functional:
  + 允许登陆，提供密码更改，展示个人信息等
+ Non-Functional:
  + ``constrains on how well the system performs``
  + 安全性保证，同时在线的用户数，用户验证

### Non-Fcuntional Requirements
+ Organisational Requirements:
  + ``我们希望能够使用学校账号进行验证登陆``
+ External Requirements
  + ``软件需要能够符合标准 web的访问要求，因为我们想要那些残疾学生也能够正常使用``

## Lecture 05 RequirementsModeling

### UML - Key Diagram Types
+ Initial Requirements: Req. Spec. or Doc.
  + Context models
  + Activity diagrams
+ Refined Requirements
  + Use case diagrams
  + Sequence diagrams
+ Architecture Designe of code
  + Class diagrams
  + Sequence diagrams
  + State diagrams

### Context Diagram:
+ Show related systems
+ 通常是Non-Functional requirements的一部分
+ ``define the boundaries of the system``
+ represent key systems that need to be developed
+ relationshio to the other systems/components

### Activity Diagrams
+ 用于制作工作流程图``workflows for key activities``
+ Explain the process, decision points, wait points & parallel work
+ 通常用于深入阐述一个``Use Case``的细节
+ 可能会把几个Use case联合在一起形成更大的流程
+ ``圆角矩形 Rounded Rectangles``表示``actions``
+ ``Diamonds``represent ``decisions``
+ ``Bars`` represent the ``start or end of concurrent activities``
+ ``black circle`` represents the start
+ ``encircld black circle`` represent the end

### Use Case Modeling & Sequence Diagrams
+ 适用于人和系统之间分享信息

### Scenarios
+ Adding context/detail to models/diagrams
+ 不只是一个story，是一个结构化描述的流程
+ 必须确定一个设定或语境
+ 必须定义一个或多个``actors or users``
+ 必须定义``goals or objectives``

## Lecture 06 Requirements Validation

### Requirements/Specification Documents
+ SRS = Software Requirements Specification
+ 通常是一大串有着ID的列表
+ 项目末尾一般都有``acceptance testing``的定义

### Requirements Validation
+ 为什么要做需求验证
  + 检查我们做的是对的
  + 避免重复工作
  + ``contractually agreeing``
+ Internal validation
  + 把它展示给老板或者同事
+ External Validation
  + 把它展示给客户

## Lecture 07 Specifications
### Specification
+ 关注点在于需要创建什么，暂时还不需要具体方法
+ Specifying：一个系统该怎么做才能迎合用户的需求
+ specification应该和需求相关
+ ``State Diagram``
+ 好的specification需要是``Traceability``可追溯性的
  + 其中的所有specifications都应该是根据相应的用户需求得来的
  + 在报告中，应该举出每一条specification支持的用户需求
  + 同样也应该根据重要性和难度对他们进行分类
+ ``Testability``
  + 提出的需求应该要是可测试的
    + ``It must load fast``, 不可证明的
    + ``It must load within 10s``可测试，可证明的

### Specification review
+ 这是一个需要进行的正式回顾流程
+ 每一个人都扮演一个角色，同时回顾specifications
  + ``Validity checks`` 是否确定了必要的功能领域
  + ``Consistency checks`` 一致性检测，查看specification之间是否有冲突
  + ``Completeness checks`` 完整性检查，查看他们是不是制定了一个连贯的系统或其中的一部分
  + ``Realism check`` 现实检测，这些specifications都能够被实现吗
  + ``Verifability checks`` 验证性检查，这些specifications都可以被测试吗？

## Lecture 08 Prototypes

### Prototyping Risks
+ 为了高逼真度的原型花费了太多的时间或经历
+ 特定的原型代码可以重复利用，但是他们并没有一个专业的水平
+ 原型可能不足以用作软件维护阶段
+ 原型可能会被错误的利益相关者通过，（经理通过了，但经理不是终端使用者）


## Lecture 09 OODesignAndTestPlan

### Class Description Documents
+ Adding detial to Classes
+ Both guide developers and act as v1 of documentation
  + for each variable:
    + data format
    + what will it be used for
  + for each method/function
    + 方法会接收到什么信息，（原因）
    + 它做什么
    + 输出什么
    + 谁会使用这个方法
  + 最后：该怎么知道它会按照希望的方法进行工作

### Test Plans
+ 当一个程序员结束制造某个事情后决定的
+ 用于``Test Driven Develpment``

<br>

+ Development Test Plans(Unit Testing)
  + 证明一个类的功能是正确的
  + 谁来做，使用什么数据，在什么平台
+ Ststem/Integration Test Plans(System/Integration Testing)
  + 证明这个软件是符合specifications的要求的
  + 测试类和类之间的关联的测试
  + 检查组件接口是否正确
+ Acceptance Test Plans
  + 证明软件符合requirements的需求
  + 通常有客户来做，所以是他们``accept``接受了软件
  
### Test Plans的用处
+ 开发者用TP来测试代码
+ 管理者用TP来估计测试的工作量，然后来安排他们，把这些涵盖在预算内
+ ``Testing documentations serves as evidence``开发文档是面向客户的证据，证明有适宜的软件工程

### Overall Document of Test Plans
+ Testing Process 测试流程：描述实用的方法
+ Requirements Traceability: 将requirements 和test结合在一起，回溯性
+ Test Items: list of things to be tested
+ Testing Schedule
+ Testing Recording Procedure 记录测试的结果
+ Hardware/Software Requiremtns - for testing machines 
+ Constraints -  number of people, machines, and etc. needed
+ System Tests - a list of all the exact test cases that will be tested

### Types of test plans:
+ Validation Testing:
  + 展示软件流程可以得到正确的结果的测试
+ Defect Testing
  + 测试软件不会中断的测试（一些不正确的数据输入）
  + 制作validation test是一个普遍的错误

## Lecture 10 Implemetation & Debug

### Key Concerns for SE Dev:
+ Conventions for ``Good Code``
+ 8 guidelines for dependable systems:
  + 控制程序内信息的可见性
  + 检查所有的输入有效性
  + 为所有的异常都准备处理handler
  + 尽可能减少使用容易出错的构造
  + 提供重启的能力
  + 检查数据的边界
  + 调用外部构造的时候，涵盖时间控制``include timeouts``
  + 给所有表达真实世界的值的常数取名

### Comment-Driven Development
+ Strategy: 先写注释，然后根据注释写代码

### Bug trackers
+ ``bugzilla.org`` 就是一个开源的web bug tracker from Mozilla
+ 这些bug追踪器帮助我们判断defect

### Debugging
+ 使用``breakpoints``断点
+ Variable Inspection 在代码停止运行后，获取当前的变量
+ Trace Tables
  + 让系统追踪某个特定的变量，来查看他们在运行过程中的改变
+ Exception-based Breakpoints
  + 在得到错误之后暂停，这样就可以判断所有事情了

### Paired Coding
+ 有一个人来负责思考，检查其他人的代码
+ 好处：解决问题和写代码这两件事情被分开了
  + 没有某个单独的人知道代码是怎么运行的
  + 他有一个内置的非正式审查流程``informal review process``
  + 良好的做法非正式地散布在团队中
