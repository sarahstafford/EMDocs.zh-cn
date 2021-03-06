---
# required metadata

title: 保护公司电子邮件附件
description:
keywords:
author: karthikaraman
manager: swadhwa
ms.date: 04/28/2016
ms.topic: article
ms.prod:
ms.service:
ms.technology:
ms.assetid: a1e630c1-7190-4ba9-b71d-ed9c2e93a6cc

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer:
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# 保护电子邮件和附件，防止数据泄露
[保护企业电子邮件和文档](protect-corporate-email-documents.md)讨论了如何能确保只有合规的设备才可以访问企业电子邮件。 但是，仅仅是保护访问权限并无法保护电子邮件和邮件附件中的内容。 内容可以复制、移动、保存到其他位置，或与其他用户共享。 EMS 使用移动应用程序管理 (MAM) 策略解决了这一问题。

托管应用是由 IT 管理员部署的符合公司安全要求的应用。 利用这些应用，IT 部门可以直接控制部署、行进中管理（如储存或更新），以及选择性擦除应用及其关联数据。 此外，通过一组移动应用程序管理 (MAM) 策略，Intune 允许你修改应用的功能并限制数据的共享，例如：

-   阻止复制和粘贴，或阻止从托管应用传输数据到不含 MAM 策略的应用。

-   防止备份到个人云存储空间，阻止另存为等功能。

-   在受 MAM 保护的应用上要求 PIN/密码或企业凭据，保障应用访问安全。

-   配置应用程序在 Intune 托管浏览器内打开所有 Web 链接。

-   选择性地仅擦除与托管应用相关的数据。 当设备丢失、被盗或不再由 IT 管理时，选择性擦除可以删除应用中的所有公司数据，仅保留个人应用数据。 这称为多身份。

利用 [Azure Rights Management Services](https://technet.microsoft.com/en-us/library/jj585026.aspx)，你可以通过以下方式扩展电子邮件保护：

-   可以对电子邮件加密，这样无论在公司内部或外部，仅有符合规定的用户才可以读取或查看邮件内容。

-   用户可以保护电子邮件消息，收件人可以读取和使用发送给他们的受保护电子邮件。

-   管理员可设定规则以：

    -   自动将规则应用于一组指定的收件人或为特定部门创建模板。

    -   自动检测规则并将其应用于包含敏感内容的电子邮件。 规则可以基于发件人、收件人、邮件主题或内容。

    -   检测敏感内容并发出警报提醒发件人在发送电子邮件之前应用保护规则。

## 托管应用组件

-   你可以在 **Microsoft Intune** 中配置策略、将策略与应用关联，或使用应用包装工具启用内部应用以使用移动应用程序管理策略。

-   **公司门户** 是在每个设备上本机运行或是基于浏览器的应用。 IT 部门会将托管应用部署到用户或设备，而最终用户可以从门户安装应用。 与应用关联的策略将转移至安装了应用的设备。

![显示如何通过公司门户和 Microsoft Intune 处理用于托管应用的策略的图形](./media/ProtectEmail/CADataSheet-Diagram-Apps.png)

## IT 管理员体验：
IT 管理员创建移动应用程序管理策略、将策略关联至应用，并将其部署到用户或设备。 在设备上安装托管应用后，应用限制即会生效。 创建和部署托管应用只需花费极少或无需花费任何额外精力：

-   存在已有应用 SDK 的应用让你可以将限制应用到应用。 无需进行其他处理，只需添加指向应用商店（如 iTunes 或 Google Play）的链接即可。 阅读 [这篇](https://technet.microsoft.com/en-us/library/dn708489.aspx) 文章以查看托管应用的列表。

-   如果想要管理在内部创建的应用，则可以使用 Microsoft Intune 应用包装工具重新打包应用。 该工具会重新打包应用，从而让你可将限制应用到应用。

## 最终用户体验
最终用户可以安装托管应用并使用它们来完成工作。 他们只能移动或共享托管应用之间的数据。 任何将数据移出托管应用生态系统的尝试都会被阻止。

## 后续步骤
你已了解了[保护企业电子邮件和文档](protect-corporate-email-documents.md)以及电子邮件附件的相关内容，现在可以详细了解如何[实现保护你的企业电子邮件的解决方案](implement-solution.md)。


<!--HONumber=Apr16_HO4-->


