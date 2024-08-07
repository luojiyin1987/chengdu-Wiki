---
title: 家庭实验室新手指南（硬件）
date: 2020-02-25 00:00:00
updated: 2024-03-15 09:58:00
authors:
  - Hayden James
  - luojiyin1987
authorURL: 'https://linuxblog.io/about-me/'
original: 'https://linuxblog.io/home-lab-beginners-guide-hardware/'
categories:
  - Article
  - Translation
toc: true
---

**3 月 8 号, 2024** by **[Hayden James][1]**, in [Blog][2] [Linux][3]

直到最近，并且超过过去十年的大部分时间，我和我的妻子都是数字游民。我们从加勒比海搬到了迈阿密、纽约、拉斯维加斯、温哥华，现在又回到了家乡。这意味着在过去的许多年里，我的家庭办公室基本上由几台笔记本电脑和屏幕组成。

如今，我们的生活更加安定；我的妻子完成了学业，从事全职工作，而我的全职工作仍然是远程办公，通过[支持 Linux 服务器][4] 的家庭办公室和[托管它们][5]。

短暂的安提瓜之行后，我与我的一位技术朋友 [Yves Ephraim][6] 进行了简短的会面。他曾在 [Cable & Wireless 公司][7] 担任工程师长达 20 年（直到 2003 年）。伊夫在我 2004 年入职前不久离开了 C&W。他支持了安提瓜和巴布达互联网和技术发展。

我们坐在他家的办公室里，他向我介绍了一些他目前的项目，以及他在 [IPv6][8]、虚拟主机、邮件、[BGP4][9]等方面的涉猎。他的大部分工作都是通过他的家庭实验室完成的。

<!-- more -->

## 什么是家庭实验室?

![我的家庭实验室 - 2020](https://static.linuxblog.io/wp-content/uploads/2020/03/my_homelab-868x868.jpg "My Home Lab - 2020")  
_截至 2020 年 5 月，我家庭实验室位于一个 12u 机架中_

把家庭实验室看成是一个可以让你在家中个人环境中尝试失败的地方。正如托马斯-爱迪生所说 我没有失败。我认为自己是失败专家。不过说真的，我还想失败得更多一些，而家庭实验室将为我创造无穷无尽的失败机会。当然，在追求成功的同时，你已经得到了成功。

一般来说，实验室是一个可以安全进行实验的地方。阅读本文的大多数人都是技术人员和系统管理员。正如你们所知，在生产设备上尝试新东西从来都不会有好结果。嘘……没关系，我知道，我知道，你不会想到一个命令就能让所有东西都离线。正因为存在这种风险，我们才要为自己构建一个沙盒环境，让自己在舒适的环境中进行尝试、测试和失败。

迄今为止，我的测试实验室设在北美和欧洲的服务器上。我正在创建一个定制的网络和服务器家庭实验室，让我更加熟悉的相关领域。我还将使用家庭实验室进行远程备份、[远程服务器的网络监控和警报][10]以及有线 UAP 接入点等。

## 愿我们相互激励，共同创建伟大的家庭实验室

正如我告诉 Yves 的那样，我们的聊天让我重新审视了这个想法。事实上，我想我的原话是："Yves，我看到了你的家庭实验室，我会把我的也提出来。和往常一样，我确信通过讨论还能学到很多东西。有鉴于此，我想从我的家庭实验室的硬件选择过程开始，与大家分享我的心路历程。

当然，这些年来，我一直在四处闲置设备，但今天这一切都停止了。算是吧。所以，如果你曾经有兴趣建立一个家庭实验室，或者你已经有了一个，那么[让我们一起交流、分享和探索][11]。

我们该从哪里开始呢？为了避免听起来陈词滥调，让我们从头做起，或者说是向前推进。我想说的是，我们需要存储空间，物理上的存储空间，为我们的新家庭实验室服务。

## 家庭实验室的位置，一切都与位置有关

位置、位置、位置。一切都与位置有关！请原谅我缺乏新意。我是系统管理员，不是作家。我会尽力让你读完这篇文章。

位置至关重要，原因有几个。在家庭办公室、起居室、壁橱、阁楼、地下室或车库之间做出选择，取决于一系列重要的变量。这些变量包括室温和通风、设备周围的工作空间、网线铺设的方便程度和距离、人流量、24 小时进出的方便程度、电源、家庭实验室的噪音水平等等。

这里是一个优点与缺点速选对比表，我整理出来以帮助我们思考所有可能的家居实验室位置。请明智地选择：

**家庭办公室**

- 优点：靠近工作区域、办公桌或设备，减少电缆铺设，整天观看指示灯闪烁。
- 缺点：占用空间或者你会在家里的办公花费了太多时间。

**客厅**

- 优点：通常很酷，空间大且布局灵活，适合晚上一起看科幻电影，融入家庭生活。
- 缺点：可能造成离婚、人多可能损坏，或者在离婚过程中受损。

**衣柜**

- 优点：容易接近，隐蔽，你可以说： "看看我衣柜里藏了什么"
- 缺点：通风不良（热量过高），空间不足，少了一个衣柜=妻子不开心。

**地下室**

- 优点：通常温度较低，并且自愿洗衣服（可能也是缺点？）。
- 缺点：你真的有地下室？洪水泛滥、蜘蛛出没或受伤时无法进入。

**阁楼**

- 优点： 噪音小，电缆铺设方便。
- 缺点：不同地区，可能会面临阳光太强烈温度高、屋顶漏水、潮湿结露，造成电路损坏、设备噪音，夜间令人毛骨悚然。

**车库**

- 优点： 室内噪音小，完全隐蔽，妻子甚至不会注意到。
- 缺点：有虫子，过热（如果没有空调），灰尘，可能需要更长的电缆，或者在停车时被弄坏。

对于我的实验室，我打算把它建在家里的办公室里。我的办公室里有笔记本电脑、台式机、服务器和其他设备，因此这个位置需要的电缆线较短。在选择位置时，应考虑房间/空间中最凉爽的区域，避免阳光直射，并考虑为将来的扩展预留空间。

最好能画出家庭网络图或 [使用网络设计软件][12]。请牢记你的楼层平面图以及如何完成电缆铺设。例如，岛上大多数住宅都有 8 英寸的混凝土内墙。这些都要事先考虑，而不是事后。换句话说，把所有事情都规划好，做好笔记并列出清单。

## 网络与服务器机架与机柜？

![home lab rack vs cabinet](https://static.linuxblog.io/wp-content/uploads/2020/02/home_lab_rack_vs_cabinet-868x399.jpg "home lab rack vs cabinet")

接下来，我们需要决定如何存放设备（调制解调器、路由器、交换机、服务器、配线架、UPS 系统、电源插座、冷却风扇等）。

网络机柜和机架经常与服务器机柜和机架混淆。路由器、交换机、配线架等通常比服务器浅得多。因此，网络机柜和机架通常没有服务器机柜和机架那么深。此外，网络设备产生的热量通常比服务器要少。你会发现有些网络机柜有玻璃门，可能无法为服务器留出足够的通风空间。

在决定了家庭实验室的深度和通风要求后，还需要考虑其他一些事项。机柜是一个带门和/或可移动侧面的封闭空间，而机架则是一个半开放或完全开放（四面开放）的框架。为了帮助你决定使用柜还是架，请考虑以下几点：

- 如果要**安装大型、重型服务器**，则应考虑机柜或四面机架的额外稳定性。
- 如果你**需要经常接触**设备的侧面或后部，那么开放式机架或侧面可拆卸的机柜会很合适。
- 如果你的**设备需要额外的冷却**，那么封闭式机柜需要更加注意冷却和通风。
- 如果**房间容易积尘**，机柜的额外保护将大大有助于防止灰尘进入设备。
- 如果**安装在有客人经常光顾的一般生活区域**，可以考虑使用封闭式机柜，这种机柜在上锁后通常会显得更加整洁。不过，维护良好的开放式机架以及整齐的电源和网线走线看起来也同样整洁！
- 如果需要**限制访问/安全**，许多封闭式机柜通常提供锁和钥匙访问控制，以提高安全性。

## 推荐的家庭实验室硬件

**更新：** 我已经更新了这篇文章。其中提到的一些设备已经停产或不再容易买到。我已经更新了我所做的升级以及其他推荐的硬件和配件。从我最初建立家庭实验室到现在，已经将近四年了。

现在，你已经测量了设备的最大深度，并考虑了上述所有建议，是时候购买你的第一件硬件了。或者不买。如果你喜欢用更有创意的方法来搭建家庭实验室，或许可以跳过本节。不过，即使你打算把家庭实验室设在客厅现有的柜子里、书架上、书桌下或纸箱里，上述大部分建议也适用。不，说真的...

![cardboard box home lab](https://static.linuxblog.io/wp-content/uploads/2020/02/cardboard-box-home-lab-868x564.jpg)  
_[Image][13]: 精美的纸板箱橱柜._

**注：** 在某些国家，你可以通过 Craigslist、Universities 和其他本地二手商家获得以下列出的大部分设备。本页面上的价格反映的是亚马逊当前的定价，可能会有变动。作为亚马逊准会员，我提供了付费商品链接，并因此获得报酬。对于亚马逊未列出的所有其他商品，如果链接随着时间的推移而不可访问，请告诉我，因为这种情况似乎总是经常发生，这也是使用亚马逊链接的另一个好处。下面我们来看看推荐的家庭实验室硬件。

### 换还是不换 网络运营商的调制解调器

![replace cable modem](https://static.linuxblog.io/wp-content/uploads/2020/02/replace_cable_modem-868x196.jpg "replace cable modem")

在我们深入探讨我的家庭实验室建议之前，如果你是交换机和路由的初学者，那么下面的许多硬件可能看起来有点矫枉过正。你只需更换网络运营商的调制解调器就能轻松上手，你知道的，就是那个闪烁着各种指示灯的东西，你经常需要拔下插头重新设置才能重新访问互联网。对，就是那个，你客厅里的迷你加热器。

大多数美国网络运营商都会收取月租。购买一台自己的网络设备在经济上更有意义。而且还能提供更好的性能、可靠性和安全性。我敢打赌，你已经被财务方面的优势所吸引了，对吧？但还有更好的办法；网络运营商提供的这些调制解调器通常质量很差，都是二手货，缺乏功能。最后，网络运营商的调制解调器/路由器组合通常无法根据新出现的漏洞独立更新固件版本。这意味着你只能听从网络运营商推送新的修补固件。

如果你有一个很好的网络运营商，而且这种情况对你不适用，请继续使用你的调制解调器。在这种情况下，更换调制解调器的唯一原因是为了获得更多的网络功能，并创建一个家庭实验室进行测试！我从 ISP 更换了调制解调器/路由器组合。我选择了 [Motorola MB7420 16×4 Cable Modem][14]。更新：3 年后，有了更快的型号，例如 [Motorola MB7621 32×8][15]。

如果你希望一切从简，那就选择 [Modem + Wi-Fi 路由器组合][16]。否则，如果你想建立一个家庭实验室来管理防火墙、NAS 存储、VPN、VLAN、PoE（以太网供电）、虚拟化、远程网络基础设施监控/警报、有线 AP、网络服务器、备份服务器等，请继续。

**\*更新：** 这款调制解调器与我使用过的大多数调制解调器类似，都会发出大量热量。在决定放置位置时，我建议放在顶部，或者在下面和上面留出空间。尽管如此，我还是很喜欢这款调制解调器！与网络运营商的调制解调器不同，它可以显示你的连接质量，包括频率（MHz）、功率（dBmV）、信噪比（dB）、校正和未校正，如果网络运营商需要，甚至可以手动设置下行频率。

### 选择你的家用实验室机架

机架单位（缩写为 _U_ 或 _RU_）是一种测量单位，定义为 1 3⁄4 英寸（或 44.45 毫米）。它是 19 英寸和 23 英寸机架框架高度和设备高度的测量单位。机架/设备的高度以机架单位的倍数表示。典型的全尺寸机架高度为 42U。机架和机柜则以 1U、2U、3U、4U 等单位表示。

下面是一个 6U 机架的示例（已标注）：

![6u rack example](https://static.linuxblog.io/wp-content/uploads/2020/02/6u-rack-2-868x583.jpg "6u rack example")

- [StarTech 12U 壁挂式机架 - 13.5 英寸深/19 英寸宽/125 磅承重][17] - $158 （[规格][18]）- 在寻找壁挂式机架的过程中，我几乎买了这款机架的 6U 版本，但在最后一刻，我改买了 12U 版本，以便将来可能进行扩展。
- [Samson SRK-12 通用设备架支架][19] - 230 美元（[规格][20]）- 这是我的首选；这是一款完全兼容浅安装设备的音频设备架。它的一个优点是有轮子支撑，因此不必固定在墙上或地板上。不过，我的身高是 6 英尺 2 英寸，我想把机架安装在离地面约 4 英尺的地方，所以正如你所看到的，我还购买了一个 2U 的冷却风扇（进气口），我将把它放在设备的底部。如果你的房间全天候都有空调，而且你不介意安装在离地面较低的位置，那么这个机架可能会适合你。下面是一个[很好的例子，说明这种机架在安装时可以看起来多么整洁][21]。
- [NavePoint 9U 基本 IT 壁挂式网络机架（玻璃门锁定）][22] - 235 美元（[规格][23]）--这是一款外观非常漂亮的网络机柜。对我来说，问题在于我只在夏天使用办公室的空调，我不希望热量成为问题；因此，对于我的家庭设置来说，封闭式机柜并不适合我。 _**更新：** 这是一个非常坚固的壁挂式机架。我可以确认，所见即所得。没有任何问题需要报告。它完全达到了预期的效果。_

### 家庭实验室 UPS（不间断电源）

![CyberPower OR500LCDRM1U](https://static.linuxblog.io/wp-content/uploads/2020/02/CyberPower-OR500LCDRM1U-868x99.jpg "CyberPower OR500LCDRM1U")

在家里，我们有一台使用丙烷的备用发电机。它可以运行长达一周，这在热带地区非常有用。除了飓风季节，这里很少停电。2020 年至今，我们曾因雷击附近的电线杆而停过一次电。

切换到备用发电机需要一分钟左右的时间。因此，我正在寻找的机架式不间断电源解决方案是能够支持 100W 到 200W 的功率，持续几分钟。足够长的时间来故障切换到备用发电机或干净利落地关闭所有设备。将来，我可能会用更大的电池来扩展这个方案，但由于购买的东西无法退货，我有点担心投资了更大的备用电池却发现它是个哑弹。我会先测试一年，所以我决定这样做：

- [CyberPower OR500LCDRM1U UPS，500VA/300W，6 个插座，AVR，1U 机架式][24] - 220 美元（[规格][25]）--小型 1U 机架式 UPS，重 20 磅，运行时间约为 10 至 15 分钟。

最终，你必须决定是否需要在家中安装不间断电源。根据经验，不间断电源电池几乎总是让人失望，这主要是因为成本与回报的关系。如果你真的需要不间断电源，你可能要花费数千美元才能获得足够长的运行时间。如果你在家工作或在家里运行关键服务（你可能不应该这样做），那么这可能是值得的。我的建议是，购买一台运行时间足够长的 UPS，让所有设备都能干净利落地关闭，并且只将 UPS 用于家庭实验室中最重要和最高效的设备。考虑到所有因素，在推荐其他 UPS 型号之前，我还得再看看这部分内容。

_**更新：** 令人惊讶的是，到目前为止，这款 UPS 的电池性能超出了我的预期。我将它的电量降至 50% 左右，运行时间刚好超过 30 分钟，包括为 [2 个 PoE 接入点][26] 和一台 [27 英寸显示器][27] 供电。正如本文后面提到的，请注意你的耗电量。这也是我考虑过的问题，而且到目前为止已经得到了回报。以 AP 为例，每个 AP 的最大功耗仅为 6.5W。最大负载约为 UPS 容量的 20% 至 30%。_

### 通用家用实验室架子

![AC Infinity Vented Cantilever 1U Universal Rack Shelf](https://static.linuxblog.io/wp-content/uploads/2020/02/AC-Infinity-Vented-Cantilever-1U-Universal-Rack-Shelf-1-868x308.jpg "AC Infinity Vented Cantilever 1U Universal Rack Shelf")

你注意到 CyberPower 1U UPS 没有机架支架吗？当然，你也可以把它放在其他设备的顶部；不过，我不建议你这样做，因为我们应该尽可能保持电池的低温，并在设备之间留出空间，以减少滞留的热量。最后，对于这种设置，如果把它放在通风的 1U 机架上，会显得更专业：

- [AC Infinity 通风悬臂式 1U 通用机架搁板，10 英寸深，适用于 19 英寸][28] - 30 美元（[规格][29]）- 这些搁板的深度从 6 英寸到 16 英寸不等。备用电池为 9.5 英寸。在决定你的需要之前，请注意你的机架/机柜和设备的深度。

_**更新：** 非常坚固，由于有通风口和插槽，非常适合设备散热和线缆管理。_

### 机架式家庭实验室电源

![ADJ Products AC POWER STRIP PC 100A](https://static.linuxblog.io/wp-content/uploads/2020/02/ADJ-Products-AC-POWER-STRIP-PC-100A-868x89.jpg "ADJ Products AC POWER STRIP PC 100A")

前面提到的 CyberPower UPS 配有六个插座 - 四个后备 /w 浪涌 + 两个浪涌。目前，在我的办公桌下，我使用了七个插座，这还是在订购替代 ISP 调制解调器、路由器、交换机和服务器之前的情况，并没有考虑未来的扩展。在 UPS 的正上方，我将安装以下设备：

- [ADJ Products AC POWER STRIP (PC-100A)][30] - 30 美金 ([技术规格][31] / [购买备件][32]) - 将其插入 1U CyberPower UPS。

_**更新：** 这是一个非常方便的硬件。它可以直接插入不间断电源，方便地开关其他设备和装置。_

### 机架式家庭实验室散热风扇

![AC Infinity CLOUDPLATE T7-N](https://static.linuxblog.io/wp-content/uploads/2020/02/AC-Infinity-CLOUDPLATE-T7-N-868x269.jpg "AC Infinity CLOUDPLATE T7-N")

保持机架安装设备的最佳温度可防止过热，确保性能稳定，并延长其使用寿命。计划在机架底部安装一个进气风扇（记住热空气会上升）。测试之后，我将决定是否需要在机架顶部安装排气风扇。

- [AC Infinity CLOUDPLATE T7-N，机架安装风扇面板 2U，19 "机架进风口][33] - 130 美元（[规格][34]）--智能冷却风扇系统，提供安静的高气流冷却。 该系统安装在一个不到 4 英寸深的坚固铝制 2U 机箱中。它包括一个恒温器，可在温度变化时自动调节风扇转速。最大风量为 220 CFM，可为服务器、网络和其他设备提供有效冷却。
- [AC Infinity CLOUDPLATE T1-N，机架安装风扇面板 1U，19 "机架进风口][35] - 150 美元（[规格][36]）--更紧凑的 1U 设计，可在空闲机架设备较少的情况下减少空气流量（最多 60 CFM）。
- [AC Infinity CLOUDPLATE T2，1U 机架安装风扇面板，顶部排风，适用于 19 英寸机架][37] - 150 美元（[规格][38]） - 这款 1U 顶部排风冷却风扇的风量可达 300 CFM。它的深度为 13.5 英寸，对于我的机架来说，要么很挤，要么需要改装。因此，在仔细检查之前，我还没有订购。

_**更新：** 风扇转速最低时，机架温度可降低约 2 至 3 华氏度。我将在夏天再次更新我的想法。_

_**更新 2：** 截至 2022 年 9 月，四个风扇中有两个出现故障。我已将其从机架上拆下，并尝试用压缩空气进行清洁。在过去两年的使用过程中，它们已经积满了灰尘！我仍然建议购买这些设备，但我也建议比我更经常地清理它们！_

_**更新 3：** 截至 2023 年 9 月，4 个风扇中有 3 个再次出现故障。_

### 家庭实验室路由器和交换机

![Ubiquiti Networks EdgeRouter ER-10X](https://static.linuxblog.io/wp-content/uploads/2020/02/Ubiquiti-Networks-EdgeRouter-ER-10X-868x304.jpg "Ubiquiti Networks EdgeRouter ER-10X")  
经过数周的研究、在线比较、阅读评论、观看 YouTube 视频以及在 [/r/homelab][39] 上花费无数个小时之后，我可以肯定地说，以下三家公司的设备将完全满足你的所有路由和交换需求： [思科][40] > [Ubiquiti][41] > [TP-Link][42]。对不起，TP，不是针对你，你只是第三名，但不是最后一名；这样更好吗？

就我的设置而言，就设备而言，我更倾向于小型企业，而不是家庭办公室。我希望将来能够获得更多的功能。以下是我的选择，然后是亚军。

**路由器**

- **多广域网负载平衡:** [Peplink Balance 20X \[CAT 7\] | Futureproof Gigabit Dual WAN Router][43] – 500 美金 – 双频（2.4GHz/5GHz）、Wi-Fi 5 1x WAN 端口、4 x LAN 端口、1 个带冗余 SIM 卡插槽的嵌入式蜂窝调制解调器、1 个 USB 接口， 1 Gbps（千兆）带宽。
- **小型企业用途:** [Ubiquiti EdgeRouter ER-10X, 10 Port Gigabit Router with PoE Flexibility][44] – 220 美金 ([技术规格][45]) – 10 个千兆位 RJ45 端口，都支持 PoE 供电，双核、880 MHz、MIPS1004Kc 处理器，512 MB DDR3 内存，512 MB NAND 闪存，内部交换机，串行控制台端口。
- **家庭实验室:** [TP-Link ER7206 Multi-WAN VPN Router][46] – 150 美金 (技术规格) – 1 个千兆 SFP WAN 端口 + 1 个千兆 WAN 端口 + 2 个千兆 WAN/LAN 端口 + 1 个千兆 LAN 端口。支持多达 100 个 LAN 到 LAN IPsec、50 个 OpenVPN、50 个 L2TP 和 50 个 PPTP VPN 连接。

**交换机**

- **企业用途:** [Ubiquiti EdgeSwitch ES-10XP, Managed 10-Port Gigabit Switch with PoE][47] – 215 美金 ([技术规格][48]) – 8 个千兆位 RJ45 端口所有 RJ45 端口均有 24V 无源 PoE 输出。2 个 SFP 端口。交换机有 10 Gbps 总无阻塞吞吐量，20 Gbps 交换容量。
- **家庭实验室:** [TP-Link 8-Port Gigabit Ethernet Easy Smart Switch (TL-SG108E)][49] – 40 美金 ([技术规格][50]) 非托管专业版。支持即插即用，屏蔽端口。

还有 [Netgear][51]、[pfSense][52]，以及很多很多其他选择，但你希望我完成这篇文章，不是吗？当然，这意味着你仍需自行研究这些推荐产品，因为并非我推荐的所有产品都符合你的要求。

_**更新**： 正合我意。路由器运行修改过的 Debian。真酷 它包含了很多企业级功能。我很高兴能学习完整的命令行管理。_

### 家庭实验室配线架和网线

![16 port patch panel](https://static.linuxblog.io/wp-content/uploads/2020/02/16-port-patch-panel-2-868x234.jpg)

事后看来，我应该选择 [24 端口配线架][53]。相反，我却选了 [这个 16 端口配线架][54]，因为我喜欢它居中的样子，看起来不那么忙乱。我知道。我不想听。但看看那东西！如果这 16 个端口还不明显的话，那就是上面的图片了。

我的网络运营商提供的最快上网计划是下行 160Mbps / 上行 30Mbps。对于我的家庭实验室来说，我很快就不需要 CAT8 或 CAT7 了，也不需要很大的局域网流量。因此，我购买了 [250 英尺的普通 CAT6 卷轴][55] 和 [一些不同长度的 Cat6][56]，因为我可以接受 1000Mbps 的限制。是的，我还喜欢有时间喝黑咖啡。如果你想要更流畅的网络流量，那么请至少选择 [CAT6a][57]。不过，一定要使用[屏蔽配线架][58]。如果你的 RJ45 接头和配线架不支持 CAT7 或 CAT6a，那么使用 CAT7 或 CAT6a 就是浪费钱。"保持简单，笨蛋！" 不，我不是在跟你说话；这是我在选择配线架和电缆时对自己说的话。

_**更新：** 高质量！易于打孔。我的所有补丁连接第一次就成功了。_

### 家庭实验室服务器

![Thinkcentre as a server](https://static.linuxblog.io/wp-content/uploads/2020/02/thinkcentre-as-a-server-868x175.jpg "Thinkcentre as a server")

出于本文的目的，我不会推荐任何特定的服务器，因为这将根据你要托管的内容而有很大的不同。NAS 存储、虚拟机、网络服务器、备份服务器、邮件服务器、广告拦截器等等，都是如此。根据我的要求，我从 eBay 上购买了一台 [ThinkCentre M73][59] 和一台 [ThinkCentre M715q][60]；两台都是二手货。至于成熟的服务器，一些不错的选择是 [戴尔][61]、[惠普][62]、[思科][63] 和 [联想][64]。对于家庭实验室来说，最好从 Craigslist 或 eBay 购买二手服务器。你可以使用维基百科搜索老一代产品的规格，例如[戴尔 PowerEdge 型号历史][65]。

_**更新：** AMD 提高了标准。我对 M715q 的 CPU 性能印象最深。在使用 Ubuntu Server 和 Windows 10.0 时，它们都能安静、低温运行。_

## 总结和结论

![homelab](https://static.linuxblog.io/wp-content/uploads/2020/02/homelab-868x376.jpg "homelab")  
_[图片][66]: 你的设置就是你的设置。传统的、定制的，随你喜欢！_

在撰写本指南时，我尽力传达我的热情、想法和整个选择过程中的考虑因素。在建造家庭实验室时，找到自己的激情非常重要。你将用它来做什么？它将如何造福于你和他人？

如果你有计划，如果你的实验室是你乐于学习、失败和成功的地方，那么它就会以这样或那样的方式为自己带来回报。尽管如此，还是要注意耗电量！你不想最终…… _房贷 1100 美元，电费 1200 美元，走进家庭实验室的感觉……不是无价的_。

计划时要留有扩展余地，可以从小处着手。你不必从机架、机柜、接线板和所有其他设备开始。先把脚浸湿，更换 ISP 调制解调器，然后再从那里开始建设。避免贸然决定硬件，而是先做做准备。然后，在 **[新社区论坛][67]** 上发布一两个问题，从其他技术人员和系统管理员那里获得宝贵的反馈意见。你会发现，你研究得越多，就会发现更多的方法，让事情变得恰到好处或大错特错。更重要的是，要玩得开心！与你的配偶、同事、孩子以及街对面那位五年后仍然只会挥手的邻居分享你的家庭实验室目标。

我希望这篇文章能给你带来帮助和启发，并开启我们之间的对话。请随时 [联系我][68]。我喜欢聆听、支持和向你们学习！

## _更新 1 – 2020.3.10:_

到今天为止，我已经基本完成了新家庭实验室的安装，现在它已经完全可以正常使用了。我对购买的所有物品都很满意。在这次更新中，我在文章中添加了一些亮点、技巧和发现，并用大写字母标注在每个硬件项目下面。

在最初的文章和家庭实验室设置中，我忽略了一件事，那就是同轴电缆。现有的电缆比要求的短了三英尺。明天，我将换上更长的电缆。如你所见，我还将 ISP 调制解调器换成了下面列出的摩托罗拉型号。

不幸的是，[Ubiquiti EdgeRouter 和 EdgeSwitch][69] 太宽了大约一英寸。我没有考虑到这一点，因为我测量了它们的总宽度，然后将其与机架的内部宽度进行了比较，而不是与机架架子的宽度进行比较。哎呀！现在，为了不让交换机一直放在路由器上，我刚刚订购了两个 [Ubiquiti 机架支架][70]。这样不仅能更好地散热和美观，而且还能将路由器和交换机放置在下图中 16 端口配线架的正下方。 一两周后再来查看更新。

![homelab update March 2020](https://static.linuxblog.io/wp-content/uploads/2020/02/homelab_update-868x670.jpg "homelab update March 2020")  
_我的家庭实验室，正在建设中（以下列出了所有图片）_

## _更新 2 – 2020.3.25: 我会尽快跟进细节和反馈。以下是最新状态照片:_

![homelab update 2](https://static.linuxblog.io/wp-content/uploads/2020/03/homelab_update2-868x868.jpeg)

## _更新 3 – 2020.4.15:_

在过去几周里，我增加了一些内容。

- [Netgear 4G LTE 调制解调器][71] （和[天线][72]），用于从 ISP1（有线网络）自动故障切换到 ISP2（4G 网络）。
- [1U 消隐板][73] 用于提高冷却风扇的效率。
- 之前的两个通风 1U 隔板现在位于机架顶部。它将用于安装显示器。(见下文待办事项)
- 快速访问 [1U mess cover][74]，防止意外切换电源开关。
- 用于 [E][75] [dgeRouter ER-10X][76] 和 [EdgeSwitch ES-10XP][77] 的 [机架安装套件][78]。
- 清理所有电线和电缆。给网线贴上标签，当然没有给配线架贴标签！
- 添加了 VLAN，限制了访客设备和其他一些家庭设备的带宽，加固了防火墙。
- 安装了 Zabbix 服务器，以便对 150 多台远程服务器进行额外监控。
- 为静态 IP 添加了一个域，其中有几个面向公众的子域。
- 删除或淡化了一些标识和文字，使外观更整洁。（又名强迫症）
- 添加 [x2 UAPs][79] 和 [x2 beacon][80].
- [插座保护器][81]，这样我就可以使用所有可用的电源插座。
- 添加了 ISP1 出现故障时的推送通知，因为切换到备用 ISP2 是完全无缝的。

待办事项：

- 添加一个单独的 21 英寸显示器，用于显示 Zabbix 主机/仪表板。
- 尝试使用 [pfSense][82]。将一切重置为默认值，然后根据经验教训重新配置。
- 添加室内 PoE 监控摄像头（目前只有室外摄像头）。
- 安装 KVM 桌面切换器，以便在两台服务器和桌面之间更方便地切换。
- 从 6 月到 8 月检查机架温度，以确定设置的冷却效率是否与计划相符。

最新家庭实验室照片：

![Home Lab #homelab](https://static.linuxblog.io/wp-content/uploads/2020/03/homelab.jpg "Home Lab #homelab")  
![Home Lab cables](https://static.linuxblog.io/wp-content/uploads/2020/03/homelab_cable_runs-868x338.jpg "Home Lab cables")

## _更新 4 – 2020.5.1:_

- 添加了一个单独的 21 英寸显示器，通过配合 Raspberry Pi 和 Zabbix，用于显示远程主机/仪表板。

![May 2020 home lab](https://static.linuxblog.io/wp-content/uploads/2020/03/may_2020_home_lab.jpeg "May 2020 home lab")

## _更新 5 – 2020.6.7:_

- 添加了键盘和鼠标，以便随时访问 Zabbix 用户界面。
- 将网状安全罩换成有色有机玻璃。
- 至此，我的家庭实验室就完成了。是这样吗？）

![home lab June 2020](https://static.linuxblog.io/wp-content/uploads/2020/03/home-lab.jpg)

## _更新 – 2021.8.19:_

一个月前，一位朋友问我能否为他们家安装类似的设备。他们想要一个简单的全屋 VPN 设置。下图就是结果。通过一台 700VA UPS，总耗电量不到 40 瓦。

- [StarTech.com 6U 壁挂式网络设备机架 - 14 英寸深][83]
- [AC Infinity 通风悬臂式 1U 通用机架，10 英寸深][84]
- [C2G 12 端口跳线板][85]
- [VCE UL 认证的 CAT6 RJ45 Keystone Jack 内联耦合器][86]
- [Vilros - Raspberry Pi 4 2GB 基本套件][87] - 运行 [Unifi 控制器][88] 。
- [Brume (GL-MV1000)][89] - [Edge Gateway + VPN (wireguard)][90] - 正在运行 [Unifi 控制器][91] 。
- [Edgeswitch 10xp][92]
- [StarTech.com 8 个插座水平 1U 机架安装 PDU 电源条][93]
- [CyberPower SL700U 备用 UPS 系统，700VA/370W，8 个插座，2 个 USB][94]

![Whole Home VPN - Homelab](https://static.linuxblog.io/wp-content/uploads/2021/08/whole-home-VPN-homelab.jpg "Whole Home VPN - Homelab")

## _更新 – 2022.10.7:_

_添加了关于 AC Infinity CLOUDPLATE T7-N、机架安装风扇面板 2U（进气口）的更新。确保每隔几个月清理一次这些设备上的灰尘。在 2 年未进行任何维护的情况下，4 个风扇中有 2 个瘫痪了。如果清洁后它们能重新工作，我会及时更新。_

## _更新 – 2022.12.13:_

_我们二月份搬到了新家。所以我搬走了家庭实验室--电缆和所有东西。终于有时间安装了。我只做了很小的改动，因为我真的很喜欢现在的样子。_

_**变更:**_

- _安装高度更符合人体工学。_
- _将一些设备左右翻转（以便于拔出插头/按下电源按钮）_
- _用新的 [Peplink Balance 20x][95]更换了 ISP 的 EdgeRouter。[使用 "最快响应 "方法实现负载平衡][96]_

_[![Peplink Balance 20x Router Review](https://static.linuxblog.io/wp-content/uploads/2023/02/Balance-20x-blog-article-image-868x580.png "Peplink Balance 20x Router Review")][97]_

## _更新: 2023.5.3:_

- _我购买了一台[1500VA 的 CyberPower 不间断电源（UPS）][98]，并拆下三个 PC 显示器和一个游戏用电脑。这样，机架内的 1U UPS 只连接服务器和网络设备。这使得在需要时电池供电的运行时间最长可达 3 小时_。 **更新: 2023.9.24:**
- _添加了有关 AC Infinity CLOUDPLATE T7-N 机架式进气风扇故障的信息。_
- _添加了对 Peplink Balance 20x 路由器评测的链接。_

_发布日期：2020 年 2 月 25 日|最后更新日期：2024 年 3 月 8 日_

**相关文章:**

- [五种适用于居家办公和小企业的网络设备][99].
- [找到兼容 Linux 的打印机][100].
- [家庭实验室灵感 - 来自读者的信][101]
- [在使用了十年的 Linux 之后，我切换到了 Windows。接下来会怎样？][102]

[1]: https://linuxblog.io/about-me/ "Posts by Hayden James"
[2]: https://linuxblog.io/category/articles/
[3]: https://linuxblog.io/category/linux/
[4]: https://linuxblog.io/web-server-services/
[5]: https://stacklinux.com/
[6]: http://www.yvesephraim.com/
[7]: https://www.cwnetworks.com/
[8]: https://www.google.com/intl/en/ipv6/statistics.html
[9]: https://www.bgp4.as/
[10]: https://linuxblog.io/20-top-server-monitoring-application-performance-monitoring-apm-solutions/
[11]: https://linuxcommunity.io/t/how-to-build-a-homelab/49
[12]: https://www.smartdraw.com/network-diagram/how-to-draw-network-diagrams.htm
[13]: https://www.reddit.com/r/homelab/comments/ep9bqy/i_see_your_fancy_rack_and_raise_you_a_stylish_rack/
[14]: https://amzn.to/32lbV1h
[15]: https://amzn.to/3ZwNtrn
[16]: https://amzn.to/3a5Lmzx
[17]: https://amzn.to/39XLcdz
[18]: https://www.startech.com/Server-Management/Racks/12u-wall-mount-rack~WALLMNT12
[19]: https://amzn.to/2STvDy3
[20]: http://www.samsontech.com/samson/products/accessories/racks/srk8/
[21]: https://imgur.com/BAGlEvA
[22]: https://amzn.to/3974q0c
[23]: https://navepoint.com/navepoint-9u-450mm-depth-wallmount-networking-cabinet-assembled-basic-series/
[24]: https://amzn.to/38QM7wi
[25]: https://www.cyberpowersystems.com/product/ups/smart-app-lcd/or500lcdrm1u/
[26]: https://amzn.to/2vdi1EO
[27]: https://amzn.to/3T8OXnf
[28]: https://amzn.to/2SVmwga
[29]: https://www.acinfinity.com/rack-accessories/rack-shelves/vented-cantilever-1u-rack-shelf-10/
[30]: https://amzn.to/2SWNG6p
[31]: https://www.adj.com/pc-100a
[32]: https://amzn.to/3c4nbDx
[33]: https://amzn.to/2T65qes
[34]: https://www.acinfinity.com/component-cooling/rack-fan-systems/cloudplate-t7-n-quiet-rack-cooling-fan-system-2u-intake/
[35]: https://amzn.to/2T65qes
[36]: https://www.acinfinity.com/component-cooling/rack-fan-systems/cloudplate-t7-n-quiet-rack-cooling-fan-system-2u-intake/
[37]: https://amzn.to/38VfUUt
[38]: https://www.acinfinity.com/component-cooling/rack-fan-systems/cloudplate-t2-quiet-rack-cooling-fan-system-1u-top-exhaust/
[39]: https://www.reddit.com/r/homelab/
[40]: https://www.cisco.com/c/en_my/solutions/small-business/products/routers-switches.html
[41]: https://store.ui.com/collections/routing-switching
[42]: https://www.tp-link.com/en/business-networking/
[43]: https://amzn.to/46qVSPa
[44]: https://amzn.to/38WhPIE
[45]: https://www.ui.com/edgemax/edgerouter-10x/
[46]: https://amzn.to/46vx1Ki
[47]: https://amzn.to/2HPDuGi
[48]: https://www.ui.com/edgemax/edgeswitch-10xp/
[49]: https://amzn.to/3a4v0Yi
[50]: https://www.tp-link.com/en/business-networking/easy-smart-switch/tl-sg108e/
[51]: https://www.netgear.com/home/products/networking/switches/
[52]: https://www.pfsense.org/
[53]: https://amzn.to/2Tflgn9
[54]: https://amzn.to/2Vh9lYA
[55]: https://amzn.to/2PldEy5
[56]: https://amzn.to/37XehEK
[57]: https://blog.tripplite.com/cat6-vs-cat6a-ethernet-cables-everything-you-need-to-know
[58]: https://amzn.to/2w07tc3
[59]: https://www.lenovo.com/us/en/desktops/thinkcentre/m-series-tiny/m73/
[60]: https://www.lenovo.com/us/en/desktops-and-all-in-ones/thinkcentre/m-series-tiny/ThinkCentre-M715q-Tiny/p/11TC1MT715Q
[61]: https://www.dell.com/en-us/work/shop/servers/cp/servers-storage-networking
[62]: https://www.hpe.com/us/en/servers.html
[63]: https://www.cisco.com/c/en/us/products/servers-unified-computing/index.html
[64]: https://www.lenovo.com/gb/en/data-center/servers/c/servers
[65]: https://en.wikipedia.org/wiki/List_of_Dell_PowerEdge_Servers
[66]: https://imgur.com/gallery/i8YdrnU
[67]: https://linuxcommunity.io/t/how-to-build-a-homelab/49
[68]: https://linuxcommunity.io/
[69]: https://www.ui.com/products/#edgemax
[70]: https://amzn.to/2PZPFVu
[71]: https://amzn.to/2wNWCTg
[72]: https://amzn.to/2XORKIE
[73]: https://amzn.to/2XPIC6v
[74]: https://amzn.to/2XLWejd
[75]: https://amzn.to/38WhPIE
[76]: https://amzn.to/38WhPIE
[77]: https://amzn.to/2HPDuGi
[78]: https://amzn.to/3bpqZOU
[79]: https://amzn.to/3bn1YEc
[80]: https://amzn.to/3anxuAq
[81]: https://amzn.to/2VFwkez
[82]: https://www.pfsense.org/
[83]: https://amzn.to/3z7IejK
[84]: https://amzn.to/2UvZ6S7
[85]: https://amzn.to/3z7I2kw
[86]: https://amzn.to/3y2E6QT
[87]: https://amzn.to/3gjDVuq
[88]: https://www.ui.com/
[89]: https://amzn.to/3mgx8W1
[90]: https://linuxblog.io/5-network-devices-for-work-from-home-and-small-business/
[91]: https://www.ui.com/
[92]: https://www.ui.com/edgemax/edgeswitch-10xp/
[93]: https://amzn.to/3y2nHf1
[94]: https://amzn.to/3gh8gK0
[95]: https://www.peplink.com/products/balance-20x/
[96]: https://www.peplink.com/technology/load-balancing-algorithms/
[97]: https://linuxblog.io/peplink-balance-20x-router-review/
[98]: https://www.cyberpowersystems.com/products/ups-systems/homeoffice-ups/pfsa1500g
[99]: https://linuxblog.io/5-network-devices-for-work-from-home-and-small-business/ "5 Network Devices for work-from-home and Small Business"
[100]: https://linuxblog.io/finding-linux-compatible-printers/
[101]: https://linuxblog.io/home-lab-inspiration/ "Home Lab inspiration – A letter from a reader"
[102]: https://linuxblog.io/10-yrs-of-linux-switched-to-windows-what-next/ "After 10 Yrs of Linux, I Switched to Windows. What next?"
