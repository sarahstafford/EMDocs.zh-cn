---
# required metadata

title: 用户和设备注意事项
description:
keywords:
author: YuriDio
manager: swadhwa
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service:
ms.technology:
ms.assetid: d1653116-3922-40d3-bc4f-3d845b6aaecb

# optional metadataco

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: 
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# 用户和设备注意事项

你需要解决的首要用户和设备问题是：现有技术将如何影响安全访问公司资源时的用户体验。 跨不同的设备解决用户体验问题十分困难，这不仅适用于安全的角度，从应用开发的角度来看也是如此。 为避免数据在传输时泄露，必须针对所需的适当级别的网络安全性考虑设备和公司资源之间的通信信道。

以下各节基于本指南的 [BYOD 问题定义](byod-design-considerations-guide.md#problem-definition)部分中用户和设备子域的各个组件，即 BYOD 问题域的概念图。

## Profiles

在设计你的 BYOD 基础结构解决方案时，了解用户的需求和要求以从他们选择的设备执行其工作非常重要。 并非所有用户都具有相同的要求；一些用户始终访问本地数据，面向他们的策略强制措施可能有所不同。 远程工作人员将从各种不同的位置以及不同情况下访问公司数据。 你必须考虑可用于满足这些需求的选项。 根据其需求确定每位用户的配置文件：

- 他们只需访问应用吗？
- 他们是否需要访问文件服务器上的文件夹？

虽然下表为每个用户的配置文件推荐了一组要求，但你可以根据贵公司的需求添加或删除要求以自定义此表。 相比于它应该包含的内容，每个配置文件类别的分类根据都基于它所消耗的资源。 例如，轻型配置文件表示设备上的资源利用率较低以及网络要求较低。 请确保你了解每个用户的配置文件空间占用量；这使你可以在余下的整个设计过程中作出更适当的选择。

本指南中建议的用户配置文件是：

- **轻**
    - 可以在本地或云中访问基于 Web 的应用
    - 访问企业移动应用
- **中等**
    - 可以在本地或云中访问基于 Web 的应用
    - 可以访问企业移动应用
    - 可以访问虚拟化的业务应用
    - 可以访问本地文件服务器上的文件
    - 可以访问云中的文件
- **重型**
    - 可以在本地或云中访问基于 Web 的应用
    - 可以访问企业移动应用
    - 可以访问本地文件服务器上的文件
    - 可以访问云中的文件
    - 可以访问使用远程桌面的计算机
    - 可以访问其他本地计算机

你需要确定哪些用户配置文件更适合你的 BYOD 基础结构解决方案。 你可以考虑根据其工作需求建立多位用户的配置文件。 在理想情况下，使用来实现 BYOD 基础结构解决方案的技术应该可以适应所有用户配置文件，因为要求可能会因人而异。 

## 设备

IT 必须确定它是否需要设备方面的知识。 例如，一个 BYOD 方案如下：当员工不在办公室时，他们每小时检查其工时单，或者查看公司通知或社交网站。 在许多组织中，这些要求通常只是涉及到 LAN 的服务，但现在它们可能面向个人设备开放。 检查其计划的人是否需要设备管理？ 了解设备的空间占用量将帮助 IT 进行以下工作：

- 跟踪哪些用户正在注册设备：用户每周注册多个设备可能表明存在可疑活动。
- 了解设备的空间占用量：了解网络上正在使用哪些类型的设备都可以帮助 IT 支持这些设备。

请考虑让设备和用户之间的链接存储在一个中心位置，IT 以后在执行审核或报告时可以使用它。 IT 需要从未知的设备状态转为已知的设备状态以启用 BYOD。 这使 IT 部门能够对作为公司资产的设备拥有更多控制权。 通常，公司将通过三种不同的方式达到这一要求：

- 方法 1 ：在每个用户的设备中安装一个管理代理。
- 方法 2 ：在一个中心存储库中注册每个设备，无需安装管理代理。
- 方法 3（1 + 2）：在每个用户的设备中注册并安装一个管理代理。


### 未知到已知设备选项 - 优点和缺点

使用以下列表来了解未知到已知设备选项的优点和缺点：

- 在每个用户的设备中安装一个管理代理
    - 优点
        - 更好地控制用户的设备
        - 远程擦除功能
        - 应用部署功能
        - IT 可使用多种安全控制来控制设备
    - 缺点
        - 要求用户安装一个管理代理
        - 必须在不同设备的平台上安装管理代理
        - 更多管理开销
- 在一个中心存储库中注册每个设备，无需安装管理代理
    - 优点
        - 不需要管理代理
        - 较少的管理开销
        - 设备的第二重身份验证
        - 验证用户和设备之间的链接
    - 缺点
        - 对用户设备的控制较弱
        - 提供较少的安全控制
        - 缺少执行远程擦除和应用部署的功能
- 在每个用户的设备中注册并安装一个管理代理
    - 优点
        - 更好地控制用户的设备
        - 远程擦除功能
        - 应用部署功能
        - 更多安全控制
        - 设备的第二重身份验证
        - 验证用户和设备之间的链接
    - 缺点
        - 要求用户安装一个管理代理
        - 必须在不同设备的平台上安装管理代理
        - 更多管理开销

在 Windows Server 2012 R2 中，[工作区加入](https://technet.microsoft.com/library/dn280945.aspx)的新概念允许 IT 部门将设备从未知状态变为已知状态。 该设备也可用作到工作区资源和应用的第二重身份验证和单一登录。 工作区加入在 Windows 10 中以本机方式提供，但它也在诸如 iOS 和 Android 等其他平台中受到支持。 工作区加入利用设备注册服务 (DRS)。 有关 DRS 的详细信息，请阅读[使用设备注册服务配置联合务器](https://technet.microsoft.com/library/dn486831.aspx)。 工作区加入是一项新技术，并且适用于特定用例。 有关结合使用工作区加入和单一登录的解决方案的详细信息，请参阅[在任何设备上从任何位置安全地访问公司资源](https://technet.microsoft.com/library/dn550982.aspx)。

如果你考虑使用 DRS，请了解此功能不提供任何管理功能。 如果你的公司需要更多安全控制，以便具有更多用于控制用户设备的选项，请考虑结合使用 DRS 和[移动设备注册](https://technet.microsoft.com/library/jj733620.aspx)以作为管理代理解决方案。 但是，如果你选择此选项，你必须具有 Windows Intune 订阅。 有关 Microsoft Intune 的详细信息，请参阅 [Microsoft Intune 页](/intune/understand-explore/introduction-to-microsoft-intune).

## 网络

必须从用户和设备的角度处理企业网络访问权限。 用户如何在使用自己的设备时访问公司数据？ 大多数 BYOD 基础架构解决方案仅在最低程度上关注从用户的设备进行远程访问；但是，如果采取以人为中心的做法，就必须考虑用户所在的物理位置。 你不仅应该关注远程访问，还应关注用户在本地访问数据的方式。 此外，你需要考虑特定于贵组织的地缘政治联合的法规问题。 例如，在物理上位于不同国家或地区的用户如何具有个性化的网络访问权限？

如果贵公司在公共云中的资源将通过 Internet 从用户设备进行访问，你必须考虑如何处理通信。 请考虑在数据从用户设备传输到云提供商的过程中使用加密。 当用户访问内部资源时，你也应该使用数据加密。

### 网络连接选项 - 优点和缺点

使用以下列表来了解连接选项的优点和缺点：

- 传统 VPN
    - 优点
        - 技术成熟
        - 易于配置
        - 在多个平台上广泛使用
    - 缺点
        - VPN 和加密协议带来的协议开销
        - 必须在启动应用之前启动
        - 要求用户交互以建立连接
- Microsoft 直接访问
    - 优点
        - 为用户提供无缝体验（始终启用）
        - 支持对 Internet 网络服务器执行选定服务器访问权限和 IPsec 身份验证
        - 支持端到端身份验证和加密
    - 缺点
        - 需要本地基础结构以支持此功能
        - 故障排除可能比较困难
        - 更多管理开销
        - 并非在所有平台上可用
- 自动触发器 VPN
    - 优点
        - 易于配置
        - 当某个应用需要对公司资源的访问权限时，将启动到本地服务器的连接
    - 缺点
        - VPN 和加密协议带来的协议开销
        - 并非在所有平台上可用
- 使用 VDI 的远程桌面
    - 优点
        - 无缝用户体验
        - 更好地控制桌面（加强）
        - 在多个平台上广泛使用
    - 缺点
        - 需要本地基础结构以支持此功能
        - 必须对网络、存储和计算谨慎执行容量规划以避免性能瓶颈
        - 每个设备需要一个远程访问客户应用
- Web 访问
    - 优点
        - 在多个平台上广泛使用
        - 可使用 HTTPS 加密
        - 技术成熟
        - 易于配置
    - 缺点
        - 需要证书
        - 如果证书基础结构在内部，则需要 PKI 基础结构
        - 需要边缘基础结构才能安全地发布应用

在定义用于访问远程网络的设计之后，请考虑用户拥有的设备在以物理方式连接到你的网络时将如何进行连接。 携带自己设备上班的用户很可能会使用 Wi-Fi 功能连接到公司资源。 你应该考虑为用户设备使用网络分段（以物理或逻辑方式）以将其隔离。

还可以根据它们运行的平台将连接到 Wi-Fi 网络的设备分段。 当它们在本地访问公司资源时，还应考虑如何保护其通信和授权。

可以在你的无线接入点和网络组件上（交换机和路由器）选择物理分段，以隔离使用自己的设备进行连接的用户。 你还可以通过使用 [Configuration Manager 中的 Wi-Fi 配置文件](https://technet.microsoft.com/library/dn261221.aspx)实现这种分段。 提供范围广泛的安全设置，例如，用于服务器验证和客户端身份验证的证书，这些证书已使用 [Configuration Manager 证书配置文件](https://technet.microsoft.com/library/dn270540.aspx)进行预配.


### Wi-Fi 网络分段选项 - 优点和缺点

使用以下列表来了解 Wi-Fi 分段选项的优点和缺点：

- 物理分段
    - 优点
        - 较低级别的安全分段
        - 相对易于配置
        - 将其自身从平台（操作系统）抽离
    - 缺点
        - 可管理性可能因供应商而有所不同
        - 不同硬件供应商之间的集成可能颇具挑战性
        - 更高的实施和维护成本
- 逻辑分段（Wi-Fi 配置文件）
    - 优点
        - 为用户提供无缝体验。
        - 更易于管理（与物理分段相比）
        - 实施成本更低（与物理分段相比）
        - 将其自身从用于连接设备的硬件中抽离
        - 支持多个平台（操作系统）
    - 缺点
        - 不提供硬件解决方案执行的较低级别的安全分段
- 动态分段
    - 优点
        - 无线访问点使用通用基础架构和 SSID
        - 最终用户和设备属性将动态设置网络访问
    - 缺点
        - 需要 IPsec 才能使用 [Microsoft 网络访问保护 (NAP)](https://technet.microsoft.com/library/cc731276(v=ws.10).aspx) 实现此类分段，对于需要支持“任何设备”的 BYOD 方案，这可能会造成问题。

> [!NOTE] 有关 Configuration Manager 中 Wi-Fi 配置文件的详细信息，请参阅 [Configuration Manager 中的 Wi-Fi 配置文件简介](https://technet.microsoft.com/library/dn261224.aspx).

网络位置是考虑用户和设备时的一个重要注意事项。 你可以利用 AD FS 中的多重访问控制以启用按应用程序的授权策略，借此你可以根据用户、设备和网络位置来允许或拒绝访问。 有关如何设置环境以验证此功能的详细信息，请参阅[使用多重访问控制管理风险](https://technet.microsoft.com/library/dn280936.aspx)。



<!--HONumber=Apr16_HO4-->


