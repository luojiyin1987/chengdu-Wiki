---
title: 如何快速学习
date: 2024-06-22T16:21:51.250Z
authors:
  - dethan3
authorURL: https://www.joshwcomeau.com/
original: https://www.joshwcomeau.com/blog/how-to-learn-stuff-quickly/
translator: "yiwei"
reviewer: "tianheg"
categories:
  - Article
  - Translation
toc: true
photos:
  - https://www.joshwcomeau.com/_next/image/?url=%2Fimages%2Fhow-to-learn-stuff-quickly%2Fguided-graph.png&w=640&q=75
---

人们常说互联网已经实现了教育民主化：人类知识的总和只需要谷歌搜索即可获取！然而，获取信息只是故事的一半；你还需要能够将原始信息转化为可用的技能。

对于我们很多人来说，这两者之间的差距可能会导致类似于 _教程地狱_ 的情况——不断地做一个又一个教程，却从未觉得自己在取得实质性的进展。

学习如何有效地学习是非常重要的，_尤其_ 是作为一名软件开发人员；学习新知识几乎就是整个工作的全部！如果你能快速掌握新语言/框架/工具，你会比一般的开发人员 _更高效_ 。这有点像超级能力。

在这篇博文中，我将分享我关于学习的心得，并展示我如何快速掌握新技能！

<!-- more -->

## 混合指导学习和非指导学习

广义上讲，有两类学习：

1. **指导型学习：** 阅读教程、参加课程、观看 YouTube 视频。任何你在跟随指导的活动。
2. **非指导型学习：** 从头开始创建自己的项目、扩展教程、在文档中查找信息。任何你不跟随指导的活动。

如果你只跟随指导资源，你会陷入*教程地狱*。你将无法掌握作为一名开发人员取得成功所需的解决问题的技能。当你尝试创建自己的项目时，你不知道从哪里开始。会觉得自己花了很多时间练习却没有获得任何实际的、实用的技能。

另一方面，如果你完全专注于非指导学习，学习过程会*非常漫长*。没有经验丰富的指导，你需要重新发明每一个轮子，花费几天或几周解决已经解决的问题。这是一条漫长而令人沮丧的道路。在最坏的情况下，你可能会完全放弃，错误地认为你不够聪明。

一些课程意识到了这种对立关系，并会包括非指导学习的机会。比如扩展目标、思维实验和挑战性练习。我希望这种类型的资源能更常见一些！

让我们看看如何将一些非指导学习融入指导资源中的一些想法。

### 故意犯错

如果你和我一样，你不喜欢犯错。你希望一切都能第一次就完美进行。

这种心态在生活中通常是有帮助的，在其他领域也有帮助。如果你是一名汽车修理工，错误可能会花费数百美元的零件费用。如果你是一名牙医，一个错误可能会毁掉某人的微笑。

但是在软件开发中，错误是免费的！如果我们犯了错误，可以切换回编辑器，修改代码，然后再试一次。我们甚至还有一些有用的错误信息（有时）可以指引我们方向。这是一种不可思议的奢侈，我们并没有充分利用它。

当我跟随教程时，我喜欢玩代码。不要逐字逐句地复制/粘贴提供的代码，试着进行实验：如果省略其中一行会发生什么？或者更改某些值会发生什么？

我尝试像科学家一样行事。如果我对这段代码的工作方式有一个假设，我会通过更改代码并观察它是否以我预期的方式崩溃来检验这个假设。当我发现我的假设有缺陷时，我可能会从教程中偏离，去谷歌上做一些研究。或者如果这个问题看起来太深，我可能会把它列入“稍后探索的事情”清单中。

这个过程帮助我们避免了无主动意识地跟随教程，复制/粘贴代码而不真正理解它做了什么或为什么我们要这样做的危险循环。

学习是一个主动的过程。探究代码有助于我们建立对正在发生的事情的心理模型。

> #### 教程渐隐
>
> 多年前，当我刚起步时，我使用了一个我称之为“教程渐隐”的方法。
>
> 具体操作如下：
>
> 1. 按照教程逐字逐句地操作，一步一步地进行。
> 2. 完成后，将代码重置为初始状态，并最小化教程。看看在不看教程的情况下你能走多远。当你卡住时，重新打开教程，但一旦你解开困惑，就再次将其最小化。
> 3. 重复这个过程，直到你可以从头到尾完成教程而不看说明。 就像上面描述的科学家心态一样，这个过程很有用，因为它迫使你集中注意力。教程逐渐淡出，你最终学会了在没有指导的情况下创建事物。
>
> 这种方法非常有效，但并不是每个人都喜欢反复创建同样的东西。不过，如果你曾经挣扎于“教程地狱”，这可能值得一试！

### 扩展教程

假设我们通过这个 [官方教程][1] 学习 React 并创建了一个井字棋游戏。

当你完成教程时，你将创建一个功能齐全但非常简单的游戏。

<video
  autoplay loop muted playsinline
  src="https://www.joshwcomeau.com/videos/how-to-learn-stuff-quickly/tic-tac-toe.mp4"
  aria-label="单人玩的井字游戏">
</video>

我们可以为它添加各种有趣的功能：

- 记录每个玩家赢得了多少场比赛
- 用更多的展示组件增强 UI
- 允许配置棋盘大小（4x4, 5x5）
- 添加一个可以与玩家对战的 AI
- 趣味元素！（动画、音效、胜利时的彩带等）

要有创造力，并选择你真正感兴趣的事情！

这种策略很好，因为你避免了空白画布的压力。你已经有了一个功能齐全、理解透彻的项目。你是在坚实的基础上添加砖块。

它还有一个好处：如果你对教程项目进行了显著扩展，可以在你的作品集中将其作为亮点！我在我的书[《创建一个有效的开发者作品集》][2]中深入探讨了这个策略。

### 创建相关项目

一旦你完成了井字棋项目，你可能会有点不确定接下来该做什么。

在跳到另一个教程之前，尝试从头开始创建一个类似的项目可能是个好主意。

例如，也许你可以制作一个宾果游戏！你可以利用一些新技能（状态管理、事件监听），但在一个稍微不同的背景下。你可能会遇到一些教程中没有涉及的难题；你可以在谷歌上做些调查，尝试找到解决方案！

如果你真的无法解决，可以暂时搁置这个项目。再做几个教程，然后回来看你是否已经学到足够的知识来突破自己的知识局限。

我见过这种策略被描述为“一个有指导，一个无指导”。跟随一个有指导资源，如教程，然后花费相同的时间创建一个类似的（但无指导的）项目。如果教程教你如何创建一个 Instagram 克隆版，尝试自己创建一个 Twitter 克隆版！

> #### 找到正确的平衡点
>
> 当我刚开始学习旅程时，我倾向于主要专注于有指导的学习。当我还在努力掌握语法和基础知识时，很难以无指导的方式构建任何东西！
>
> 然而，当我变得越来越熟悉后，平衡就会发生变化。我花更多的时间进行无指导的学习，构建那些对我来说有趣的东西。当遇到新的或不熟悉的问题时，我会寻找教程，但随着经验的积累，这种情况会越来越少。
>
> 我的图表看起来像这样：
>
> ![Line Chart](https://www.joshwcomeau.com/_next/image/?url=%2Fimages%2Fhow-to-learn-stuff-quickly%2Fguided-graph.png&w=640&q=75)
>
> 你的图表可能看起来有些不同；最终，找到正确的平衡点取决于你自己！重要的是，我们不要只专注于有指导的学习或无指导的学习。

## 心态培养

多年前，我和一些朋友去打保龄球。

我表现得很差。我的大多数球都进了沟。到比赛结束时，我的得分是小组中最低的。

有两种不同的方式来解释这种情况：

1. 我就是不擅长打保龄球，我永远不会擅长。保龄球根本不是我的菜。
2. 我不擅长打保龄球。但如果我愿意，我可以成为一个优秀的保龄球选手。

这有一种自我实现预言的性质：无论你选择哪种解释都是正确的。如果你认为你的保龄球技能水平是固定的，它就会是。如果你相信自己可以提高，你就会提高！

如果你想快速学习新技能，培养正确的心态至关重要。

软件开发从来都不是一帆风顺的。不可避免地，我们会遇到一个困难的问题，即代码无法达到我们的预期。

这可能会导致一个充满沮丧和自我怀疑以及冒名顶替综合症的下行螺旋，或者它可以被视为一个极好的学习机会。只要你有正确的心态，没有什么比难以理解的错误信息更能帮助你快速学习。

说实话，**我们从挣扎和失败中学到的比从轻松成功中学到的要多得多**。有了成长心态，虽然挣扎可能不一定*有趣*，但感觉很有成效，就像一次好的锻炼。

了解更多关于 [培养成长心态][3] 的信息。

## 目标和动机

我们生活在一个社交媒体炒作的世界里，很容易感到有压力，要跟上潮流，学习每一个在 Twitter 上出现的流行 JS 库。

就我个人而言，每次我试图这样做，结果都不太好。😅

我只是对为了学习而学习并没有特别的动力。为了让我保持动力，我需要有一个令人兴奋和具体的目标。

例如：几年前，我发现了 Beat Saber，这是一款 VR 视频游戏。在这个游戏中，你用光剑攻击方块，与音乐同步。每首歌都有一个独特的编舞。

有软件让用户可以创建自己的编舞（在社区中称为“地图”），但我并不是它的忠实粉丝。我想为 Beat Saber 创建自己的地图编辑器。

经过几个月的艰苦和偶尔令人沮丧的工作，我实现了我的目标：

<iframe
  frameborder="0" allow="autoplay; fullscreen" allowfullscreen
  src="https://player.vimeo.com/video/652869239?pip=true"
></iframe>

（如果你对这个项目感兴趣，可以[在线观看][4]，在 [Github 上查看代码][5]，或[观看关于其开发的会议演讲][6]！）

在这个项目之前，我没有任何 3D 经验，我必须学习大量关于 WebGL、Three.js 和 react-three-fiber 的知识。学习是困难的，无论你的成长心态有多么培养得当，总会有些日子事情进展不顺利。

但因为我有一个具体的目标，是我*真正*想要的，我能够克服挫折并继续进步。如果我只是为了好玩或者因为我认为它会让我的简历看起来更好而学习这些东西，我可能很快就放弃了。

不同的人受到不同事物的激励，所以我并不是说你需要找到一个特定的项目来创建。但我确实认为有一个明确的目标是很重要的，某个你真正感兴趣的东西。否则，在最初的新奇感消失后，维持所需的动力将变得很困难。

## 记忆事物

我的记忆力 _非常_ 差。

这可能有点问题；如果你不能记住事情，学习东西会很难！幸运的是，我有一个系统：**间隔重复**。

这里是间隔重复的核心思想：为了增强记忆，你需要在记忆即将消退时访问它。每次你增强记忆，它的持续时间就会稍微长一点。

这听起来很复杂，但有一些工具可以帮你跟踪这个过程。我个人使用 Leitner 盒，这是一个装有几百张索引卡的物理盒子。每天，我会复习一小部分卡片。

如果你对间隔重复感兴趣，我*强烈*建议你看看 Nicky Case 的这篇可探索的解释：[《如何永远记住任何事情》][7]。

## 建立日常习惯

假设我们承诺每周花 7 个小时学习新东西。你认为是每天花一个小时在这个活动上更有效，还是每周日连续花 7 个小时更有效？

据我的经验，花费较少的时间但更频繁地进行会 _更_ 有效。

我意识到并非每个人都有这种奢侈的结构，但如果你能做到，我强烈建议你尝试每天花一点时间在你试图学习的东西上。

我有一些关于为什么这种方式对我来说更有效的假设：

1. 每晚，大脑会处理并承诺当天学到的东西。我希望每天都能利用这一点，而不仅仅是每周一次！
2. 因为我每天都练习，可以直接从上次中断的地方继续。我不必花费大量时间刷新记忆和重新开始。
3. 正如我们所谈论的，在新奇感消失后维持动力可能很困难。如果你能将其融入日常生活，你就不必太担心动力问题；不管你感觉如何，它变成了你只需要*做*的事情。

## 公开学习

我是 Swyx 的 [公开学习][8] 理念的忠实粉丝。

主要思想是，通过发布我们所学的内容，我们可以帮助未来的自己。当我们发现新事物时，我们应该创建一个记录它的文档，比如博文、推文或 YouTube 视频。

这可能有点违背直觉；为什么要在“学习时间”写博文呢？这不是浪费时间吗？

公开学习有*很多*好处，我发现了以下几点：

1. 你有没有试图向某人解释某事，结果发现自己并不像你想象的那样彻底理解它？写博文有同样的效果。这是揭示你心理模型中的缺陷/漏洞的最佳方法，以便你可以修复它们。
2. 世界上最糟糕的感觉是遇到一个你*知道*自己已经解决过的 bug，但你记不起如何解决它。如果你写了一篇关于它的博文，你可以参考它！
3. 通过分享你的学习，你成为开发者社区的积极参与者。你可以结交朋友和建立联系。这既有趣又有成就感，更不用说在找新工作或启动新企业时的好处了！

需要注意的一点是：不要陷入设置完美博客数周的陷阱！从像 [Dev][9] 这样的平台上发布开始，甚至只是发布在 Twitter 上！在我建立博客之前，我在 Medium 上发布了数十篇博文。如果你发现自己真的喜欢公开学习，你可以随时迁移到一个华丽的定制博客。😄

## 技能网络

最近，我开始自学如何使用 [Blender][10] 创建 3D 插图。

我还是个初学者。目前，我大概投入了约 150 个小时的时间。但我已经能够创建一些看起来不错的艺术作品。以下是我制作的一些东西：

![3D 插图](https://www.joshwcomeau.com/images/how-to-learn-stuff-quickly/sneakers.png)
![3D 插图](https://www.joshwcomeau.com/images/how-to-learn-stuff-quickly/muffin.png)
![3D 插图](https://www.joshwcomeau.com/images/how-to-learn-stuff-quickly/chess.png)

我能够如此快速地学习，是因为遵循了这篇博文中列出的所有技巧。但还有一个我手中的王牌：_互补技能_ 。

事情是这样的，3D 插图不是一项单一的技能；它是多个技能组成的集合。其中一些，比如创建 3D 模型，对我来说是全新的，我必须从头学起。但其中一些是我有经验的技能网络的一部分。

例如：我有点业余摄影爱好。几年前，我学会了构图，如何在视口中排列元素以获得引人注目的镜头。我可以在我的渲染中定位对象时利用这些技能。

这是一个特别具体的例子，但其他的例子则更为模糊。多年来，我在前端开发工作的过程中培养了对细节的关注。所有这些像素推敲帮助我为倒角和厚度设定合适的值。而我做 UI 设计的工作帮助我理解色彩理论和美学。

你不一定会认为我已经拥有的技能会与 3D 插图产生协同作用，但它给了我一个极大的不公平优势。

在我看来，技能就像财富。你积累的技能越多，它们增长的速度就越快。在一个领域中获得的想法和技术可以在另一个领域中发挥作用。

我并不是说你应该成为一个完全的通才——拥有深厚的专业知识仍然是值得的！但你的技能网络越广，在学习新事物时你的优势就越大。

有时，学习资源会利用这一点。例如，我正在制作一个 CSS 课程，[《为 JavaScript 开发者准备的 CSS》][11]。我专门为 JS 开发者创建它，因为我知道我可以利用大量的预先存在的知识来简化学习 CSS 的过程。我们不是从零开始创建，而是利用你对 JS 的知识来解释 CSS，复制/粘贴你已经拥有的心理模型。

我的目标是改变你与 CSS 的关系。很多 JS 开发者觉得它令人沮丧且违反直觉。如果你想提升你的 CSS 技能，你可以[了解更多关于课程的信息][11]。

在这篇博文中我覆盖了 _很多_ 内容，真的很感谢你坚持到最后 💖 祝你在学习旅程中好运！

[1]: https://react.dev/learn/tutorial-tic-tac-toe
[2]: https://www.joshwcomeau.com/effective-portfolio/
[3]: https://www.youtube.com/watch?v=-71zdXCMU6A
[4]: https://beatmapper.app/
[5]: https://github.com/joshwcomeau/beatmapper
[6]: https://www.youtube.com/watch?v=9u0VapB-AbE
[7]: https://ncase.me/remember/
[8]: https://www.swyx.io/learn-in-public/
[9]: https://dev.to/
[10]: https://www.blender.org/
[11]: https://css-for-js.dev/