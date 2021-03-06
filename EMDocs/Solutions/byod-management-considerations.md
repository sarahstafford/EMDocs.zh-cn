---
# required metadata

title: 管理注意事项
description:
keywords:
author: YuriDio
manager: swadhwa
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service:
ms.technology:
ms.assetid: ba8cc256-2075-457f-a827-7ec9213c5235

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: 
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# 管理注意事项

支持 BYOD 模型的基础结构中必须具有管理域。 为了完全支持 BYOD 需求，管理域必须允许 IT 监视资源、提供报告功能、管理计算和存储资源、支持设备配置和自动化，并且可以管理应用部署和设置。

## 监视

管理域的角色之一是监视符合性设置，不仅对于公司资产，对于用户拥有的移动设备也是如此。 应根据公司业务线评估符合性方面的注意事项。 一些公司可能仅允许公司数据在已加密时驻留在用户的设备上。 IT 必须控制安全设置以强制执行这些策略。

根据公司策略和公司将采用的 BYOD 基础结构，用户设备中的管理级别将有所不同。 如果公司规定必须提供完全擦除功能才能访问公司资源，IT 必须在所有受监控的设备上强制实施此设置。 IT 还需要能够将设备重置为制造商的默认设置，这会擦除所有个人设置和数据（如有必要）。 使用以下部分来确定你的 BYOD 基础结构将需要的监视选项。

### 监视选项 - 优点和缺点

使用以下列表了解每个监视选项的优点和缺点：

- 用户的设备上装有管理代理
    - 优点
        - 更好地控制用户的设备
        - 远程擦除功能
        - 选择性擦除功能
        - 更快的应用部署和生命周期管理
    - 缺点
        - 需要在用户设备中安装管理代理
        - 从用户的角度来看更具有侵入性
        - 需要后台管理基础结构以支持代理
- 没有安装管理代理
    - 优点
        - 用户的设备上未安装任何管理代理
        - 只能从应用角度强制实施策略（例如，ActiveSync）
    - 缺点
        - IT 可用来管理设备的选项有限

正如上表所示，在设计 BYOD 基础结构解决方案时，如果你要强制实施公司策略，就需要在用户的设备上安装代理。

如果公司选择支持不同类型的设备，你需要了解设备的功能，例如存储加密、VPN 连接选项以及受支持的编程语言。 评估可通过实现哪些功能来遵守公司策略。 可以通过强制执行策略来监视设备以满足符合性。 当数据存放在用户的设备中时，请考虑启用设备加密；这可以在你的数据泄露策略中提供帮助。 强制实施策略（例如密码解锁、密码历史记录和强密码）可以跨本地设备和移动设备实现类似的安全性。

Configuration Manager 中的符合性设置使 IT 能够管理企业中服务器、便携式计算机、台式计算机和移动设备的配置和符合性。 请考虑使用 Configuration Manager 中针对移动设备内置的默认符合性设置作为基准，并在此基础上根据贵公司的需求进行自定义。 有关 Configuration Manager 中的符合性设置的详细信息，请参阅 [Configuration Manager 中的符合性设置简介](https://technet.microsoft.com/en-us/library/gg682139.aspx)。

通过使用 Windows 选择性擦除，IT 可以确保企业分散在公司或个人设备上的公司数据的安全。 开发人员可以创建应用以对数据使用 Windows 选择性擦除策略，并在企业拥有的 Internet 域上对其进行保护。 有关 Windows 选择性擦除的详细信息，请参阅“用于设备数据管理的 Windows 选择性擦除”。

## 报表

若要保持对已知设备的控制，报告设备功能或者简单地了解这些设备的行为是 IT 的基本任务。 可以使用报告更好地了解当前的环境。 当你不仅尝试了解环境，还要了解某些移动设备的功能时，将出现以下一些问题：

- 你的组织中使用多少 iOS 设备？
- 这些设备运行哪些 iOS 版本？
- 这些设备上安装了哪些公司应用？
- 你的组织中是否存在任何已越狱的设备？

请考虑使用可提供设备清单和可自定义报告的管理解决方案。 通过选择此选项，你将在 IT 需要发现关于用户设备的详细信息时为他们提供更灵活的方法。 IT 必须能得到关于已在本地和云中注册的所有设备的报告。 管理系统的报告功能可以位于本地或云中 - 也可以是两者混合（称为混合解决方案）。 使用下表来确定哪个报告选项适用于你的公司。

### 报告选项 - 优点和缺点

使用以下列表了解每个报告选项的优点和缺点：

- 内部
    - 优点
        - 集中式报告
        - 完全由 IT 控制
        - 可自定义
        - 在本地管理安全控制
    - 缺点
        - 不能以本机方式枚举非本地设备
        - 与基于云的解决方案相比，管理开销较高
- 基于云
    - 优点
        - 能够报告已加入云服务的设备
        - 经济高效
        - 报告可用性（可从任何位置创建和查看报告）
        - 与本地解决方案相比，管理成本更低
    - 缺点
        - 不能以本机方式枚举本地设备
        - 通常需要每月订阅服务
- 混合
    - 优点
        - 能够报告已加入云服务的设备
        - 经济高效
        - 报告可用性（可从任何位置创建和查看报告）
        - 与本地管理解决方案集成
    - 缺点
        - 通常需要每月订阅服务。

通过将 Microsoft Intune 与 System Center 2012 R2 相结合，你可以从本地和基于云的设备获取报告。 Configuration Manager 包括很多随时可用的内置 UDM 报告，包括针对应用、硬件清单和设置管理的报告。 你不需要为电脑和移动设备管理创建自定义报告或单独的报告；这些功能可以集成在一起。

有关 Configuration Manager 报告功能的详细信息，请参阅 [Configuration Manager 中的报告简介](https://technet.microsoft.com/library/gg682105.aspx)。

## 计算和存储

在开发新应用且用户使用自己的设备对其进行远程访问之后，如果没有合理规划解决方案，应用性能可能会降低。 尽管此设计注意事项指南不会向你深入介绍性能注意事项，但必须回答有关管理基础结构的问题：

- 贵公司当前使用的管理解决方案是否能够针对支持从用户设备访问应用的平台管理存储和计算资源？ 
- 贵公司当前使用的管理解决方案是否能根据一组预先设定的规则针对支持从用户设备访问应用的平台增加计算和存储资源？
如果目前采用的管理解决方案不能满足上述两个要求，可考虑使用一种通过解决下表所示的两个核心要求来管理计算和存储的管理解决方案。

### 计算和存储管理功能 - 优点和缺点

使用以下列表了解每个存储管理功能的优缺点：

- 资源池
    - 优点
        - 可分配来自不同位置的计算和存储池资源
        - 高级别可用性。
        - 比不能利用资源池的解决方案更加可靠
    - 缺点
        - 可利用资源池的管理解决方案非常少
        - 如果公司尚未在其数据中心使用云计算原则，用于实现的初始开销可能更高
- 弹性
    - 优点
        - 能够按需动态分配计算和存储池资源
        - 高级别可用性
        - 在实现后更易于管理
    - 缺点
        - 可利用弹性功能的管理解决方案非常少
        - 如果公司尚未在其数据中心使用云计算原则，用于实现的初始开销可能更高

System Center 2012 R2 可以使用资源池和弹性来管理存储和计算。 System Center 2012 R2 还将存储与差异磁盘这一优化集成，它通过允许在多个虚拟磁盘之间共享大部分磁盘数据来降低存储要求，这可以优化存储成本。 使用 System Center 2012 R2 虚拟化并且将由远程用户所使用的应用利用的服务器可以采取这种技术。

有关 System Center 2012 R2 存储功能的详细信息，请参阅 [System Center 2012 R2 的 VMM 中的新增功能](https://technet.microsoft.com/library/dn246490.aspx)。 

## 自动化

自动化可用于修正不合规的设备，并且 IT 还可以指定不同级别的不合规严重性。 你应该考虑自动化在 BYOD 不同方面的用法；例如，如何自动部署将由移动设备使用的新服务？ 如何自动化移动设备的授权过程？

尽管你将看到显示的所有 BYOD 子域都可以利用自动化，但自动化资源的责任属于管理子域。 自动化可内置于操作系统；但是，公司将采用的管理解决方案将负责扩展这些功能并提供减轻 IT 日常任务的方法，同时还要监视和报告自动化所产生的结果。
System Center 2012 R2 中功能最强大的自动化选项是 Windows PowerShell。 有关 System Center 2012 R2 自动化的详细信息，请参阅使用 [Windows PowerShell 的 System Center 自动化](https://technet.microsoft.com/library/dn507037(v=sc.20).aspx)。 但是，还可使用另一个选项，它提供一种更为简单但不十分可靠的自动化任务形式：任务序列。 使用下表来评估每个选项的优缺点。

### 自动化选项 - 优点和缺点

使用以下列表了解每个自动化选项的优点和缺点：

- Windows PowerShell
    - 优点
        - 与 Windows 操作系统集成
        - 比任务序列更可靠
        - 可以编写脚本
        - 可以使用编程原则，如过程、循环和数组
        - 提供管理平台以外的功能。
    - 缺点
        - 需要更多技术技能才能使用它
        - 开发初始自动化脚本可能需要更长的时间，具体取决于手头的任务
- 任务序列
    - 优点
        - 易用
        - 可使用 System Center 内的本机功能
    - 缺点
        - 功能有限
        - 不可脚本化
        - 功能仅适用于 System Center 本身的一些任务

## 部署和设置

下一步是了解将应用部署和设置到远程设备的相关注意事项。 应回答两个关键问题：

- 用户如何从他们自己的设备访问应用？
- IT 如何以友好而有效的方式向用户提供这些应用？

公司采用的管理解决方案还负责处理软件分发和设置（不考虑用户使用的平台）。 用户应该能够从自己的设备安全访问一个集中的位置并安装他们有权使用的应用，以执行他们的工作。

该方面的挑战之一是：要能够管理不同的平台并保留一个集中的管理界面，该界面使 IT 能够快速识别本地和云中连接的设备。 你必须考虑采用可整合这两者（本地和云）的管理平台，还要考虑采用能够管理 Windows 和非 Windows 系统的管理平台。

若要在本地进行集中式管理，你可以使用 Configuration Manager 。 通过使用此选项，IT 可利用企业注册功能在公司的 Configuration Manager 服务器上注册设备。 有关如何使用 Configuration Manager 管理设备的详细信息，请参阅[使用 Configuration Manager 和 Microsoft Intune 管理移动设备](https://technet.microsoft.com/en-us/library/jj884158.aspx)。

若要管理不是基于 Windows 设备的其他平台，你可以利用 Microsoft Intune 云服务。 Microsoft Intune 公司门户可以用于注册、管理和安装已授权的应用。 用户可以轻松访问应用，并将它们安装在自己的设备上。 

>[!TIP] 
>有关 Microsoft Intune 的详细信息，请参阅 [Microsoft Intune 页](/intune/understand-explore/introduction-to-microsoft-intune)。 

尽管它们是两个不同的选项，但你可以将两者集成，以便从单个位置提供应用部署和设置。 使用下表来确定哪个选项适合你的 BYOD 设计。

| **设计要求**                                             | **部署和设置选项**                |
|---------------------------------------------------------------------|--------------------------------------------------------|
| 将应用部署和设置到仅位于本地的设备。      | Microsoft System Center 2012                           |
| 将应用部署和设置到位于公司外部的设备。   | Microsoft Intune                                       |
| 将应用部署和设置到非 Windows 设备。                   | Microsoft Intune                                       |
| 仅部署和设置应用程序到本地设备，部署和设置应用到公司外部设备或部署和设置应用到非 Windows 设备。       | 与 Configuration Manager 集成的 Microsoft Intune
                                                                    


<!--HONumber=Apr16_HO4-->


