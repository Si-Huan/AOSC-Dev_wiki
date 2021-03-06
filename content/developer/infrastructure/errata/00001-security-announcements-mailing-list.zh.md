+++
title = "INFRA-ERR-00001：安全公告邮件列表迁移"
description = "关于最近安全公告邮件列表迁移的情况简要说明"
date = 2020-05-04T03:36:15.932Z
[taxonomies]
tags = ["infra-errata"]
+++

# 概述 

AOSC 安全公告邮件列表（security@lists.aosc.io）因不明问题无法正常工作。一方面，我们尽全力排查问题但仍无法找到合适的解决措施；另一方面，我们还注意到这个邮箱地址在 RFC 2142 中被定义为只供系统管理员使用的保留邮箱，显然将其用作邮件列表是不恰当的。因此，我们决定遵循 RFC 的规则创建一个新邮件列表 security-announcements@lists.aosc.io，并将旧邮件列表存档迁移到新邮件列表。迁移已于 2020 年 4 月 5 日完成。

# 背景

从 2020 年三月下旬开始，我们就已经无法在旧邮件列表（security@lists.aosc.io）发布安全公告。尽管我们做了各种尝试（例如排查配置文件和暂时取消入站垃圾邮件过滤），但我们还是无法解决这个问题。由于自 2018 年邮件列表开始运行后，我们几乎没对配置做任何更改，因此我们认为很有可能是底层软件（Sympa）的更改破坏了我们的邮件列表。在这个过程中，我们还发现根据 RFC 2142，"security" 是为站点管理员而设的保留邮箱，因此我们决定用另一个名称重新创建邮件列表。在 Telegram 群组中进行了一系列讨论后，我们决定使用 "security-announcements" 这个名字作为新的邮件列表的名称。

# 成因

尚未查明。目前我们猜测问题是在某次常规服务器维护时意外引入的。

# 决议

我们在 2020 年 4 月 5 日创建了新的邮件列表 security-announcements@lists.aosc.io 并将旧邮件列表存档迁移到新邮件列表上。在确认新的邮件列表可以正常运行之后，使用 Sympa 的停用功能停用旧邮件列表。在迁移之后，入站垃圾邮件过滤被重新激活并确认可以运行，订阅者和旧的存档也被成功导入。

即日起，所有安全公告都应该通过 security-announcements@lists.aosc.io 发送。