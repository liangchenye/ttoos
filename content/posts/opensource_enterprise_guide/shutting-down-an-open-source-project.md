---
categories:
- 开源
- 企业指南
date: 2019-01-16T10:48:03+08:00
description: "面对开源代码托管平台，GitHub、GitLab、Gitee......尸横遍野，是的，开源项目的淘汰率是很高的，高到有人甚至说85%，那么勇敢的准备好失败，乃是赢得信任和尊重的起码做法！这就是开源，不止于代码，有关人类社会那些美好的东西！"
keywords:
- Open Source
- Culture
- Reading
- News
tags:
- 开源企业指南
- 开源之道
title: "Linux基金会企业开源指南系列之十 —— 企业如何优雅的关闭一个失败的开源项目"
url: ""
---
## 特别声明

本文拥有创作共用授权之相同方式共享授权4.0版国际许可协议（Creative Commons Attribution ShareAlike 4.0 International License）授权许可。 开源之道独立精心翻译分享，欢迎同道中人商讨。

# 如何优雅的关闭一个失败的开源项目

当一款开源项目对于贵司来讲已经没有意义，或者说处于各种缘由，需要将投入开源项目的资源撤离，这个时候或许作为读者的你还有些困惑，请放心，本篇指南就是专门为你遇到这样的情况所准备的，该指南为贵司和贵司的开发团队提供一些关于关闭开源项目的建议。通过优雅的关闭项目，或者是将项目转移给愿意继续负责的团队，确保贵司是以一种责任感的方式来认真对待项目的整个生命周期的。基于这样一个前提，要为项目的用户设定合理的期望，以确保其能长期项目对项目代码的依赖关系保持下去，并也可以维护贵公司作为一个参与者在这个开源项目中负责的声誉。

本指南会帮助你决定一个项目何时不再有用、理解如何从项目撤离、确认准备进入开始一个新项目时，如何处理原有项目中的代码、仓库、网站，维基以及其他项目资产。

## 开源项目的生命周期规划

当软件开发者开始构思和开发新的且是关键业务需要的开源项目时，他们通常会为每个项目的生命周期制定明确且具体的规划，从其诞生到终止。且这些规划也要列为企业整体开源战略的一个部分来执行，和其它所有的项目一样受到监管。

这些努力均是为未来的项目所遇到的一些情形做好充分的准备，它们包括：关闭一个项目、项目要转交给更感兴趣的用户组、公司主动交出控制权等，优雅的关闭一个项目是企业对项目、用户以及支持这一切的开源社区所应承担责任中的一部分，尤其是转交的时候，顺利的过度是大家都希望看到的。

### 为什么说生命周期的计划很重要

其实为一个可能性很大的即将死掉的开源项目没有什么特别的，和多数的生命周期规划没啥区别，如私有软件规划、IT系统硬件部署、乃至更为广泛的业务决策等。对于开源的规划而言，项目的声明周期规划应包括传统的生命周期评估，如项目范围、发展愿景的概述，以及项目增长的估计，乃至开源特定的内容如规划社区构建、早期用户采用、用户的反馈和参与纳入等。

任何项目不可能永远保持增长的势头，用户的使用也有一个最高限度，这些都是意料中的事情。即使是最为成功的开源项目，也可能随着商业计划的改变、新技术的取代、更为创新的技术来临等因素，创始人和用户最终也要放弃它们。因此，凡是想周全了，再乐观的心态，也要有做好打算。

## 生命周期结束的开源项目该是个什么样子？

如果贵司的的开源项目遇到这样的情形，平日里较稳定的贡献或提交量突然出现了下降趋势，不要慌张，它并不意味着项目已经完蛋了。它大多数的情况是项目成熟的标志，已经达到了开发的预期目标，用户的需求减少不需要特别的跟踪和更新，这是一种好的现象。

但是，上述情况未必是经常有效。如果说项目的采用人数、以及使用代码的开发者都在明显的减少，那么这极有可能是人们对项目的兴趣正在降低，该项目正在走向死亡的路上。另外，判断项目是否就要完蛋的指标有：项目活动的整体水平、用户是否有发布问题并参与关于代码的问题在线讨论。

### 需要引起注意的问题迹象

一个死去的或者正在死去的路上的项目通常是有特定的问题的，诸如没有处理好关于开发方向的不同，又或者是过去关键的贡献者跑到了新的感兴趣的项目了，等等不一而足。一个明显迹象是，其他人与您的团队成员的观点缺少一致性，或社区询问是否要继续项目，还是要结束或彻底放弃项目。另一个迹象是您的社区不再修复或更新代码来解决其中的漏洞。

> “如果你的项目没有人提出问题、如果没有人作出贡献、而且看起来还没有什么用户使用、也没有什么其它项目依赖，那么所有这些很可能就是巨大的警告！或许项目没什么问题，但是如果项目真的遇到问题了，就要认真的去找下原因了。” – Dr. David A. Wheeler，Linux基金会[核心基础设施研究](https://www.coreinfrastructure.org/) （CII）开源专家和两个项目的领导者。

其实，即使是眼见确凿的数据都有可能是一种假象。因为有些情况确实特殊，比如经常对你的代码访问是通过其它应用程序间接的包管理器访问的，而不是通过直接下载的方式。那么遇到这种情形的话，就很难知道到底有多少用户，只能通过生命周期来进行更为准确的跟踪。

## 为什么要在一个项目尚未启动时就规划好其结束？

一如规划开源项目的其它事项，有关在某一天如何终止或转交项目的决策，同样是项目生命周期的重要部分。

为什么这么做了呢？因为没有周全的考虑，就不会保护好社区和用户，就可能对于公司的声誉在开源社区和项目本身内有所损害。如果你管理着一个开源软件项目，要记得开源项目从来不是一座孤岛，它有太多的依赖，而一旦被其它所依赖的话，就更要负起责任来了。当然，贵司可以选择改变项目方向或状态，但是你的责任是能够清晰的、及时的、开方式的沟通将这些变更传递给项目的用户，以让他们有充足的时间做好相应的应对方案。在没有将项目的规划告知用户就结束一个项目并彻底放弃代码的行为，是非常不负责任的行为。

### 维护贵司的声誉

让项目的其它用户陷入困境肯定不是贵司的初衷。在开源的世界里，尤其对这个问题不可以掉以轻心。当然这并不是说要在项目开始之前就去事无巨细的做所有可能的退出计划，但是一个高效的、开放的社区有利于让用户确保贵司不用轻易的放弃项目，尤其是不会一声不响的就丢弃掉，而且能够表达贵司会努力的让项目成功，而不会置用户于不管不顾。另外，通过构建、开发和推广代码的方式来将项目更加的易于 fork，你的项目是可以提供更为灵活的转交能力到其他参与到项目的开发者的。事情就是这么个道理，尽管你毋须事无巨细的规划每个退出的细节，但是有必要做一些基本的事项，如用户具有知情权，贵司需做到信息的透明和公开。

### 寻求建立多元化的贡献者的基础

代码贡献者的多样性，对于帮助开源项目的增长是有着非常大的帮助的，它可以为项目带来诸多益处，如新的想法、深入解决问题的可能性、以及代码可以让更多的开发者看到。而且对于贵司决定离开或结束项目也是有益处的。由于多样化社区的参与，你有很大机会找到对项目维护有兴趣的社区成员，扩大贵司未来转型的选择范围。如果最终贵司还是决定了要离开项目，那么就可以非常顺利而愉快的交接到更感兴趣的维护者手中，让项目继续前行，而不是让它悄无声息的死掉。

这些前提的基础工作对于项目成功的建立一定的信任度至为关键，其是一个健康的生态系统的前提，也是围绕项目构建必要的商业依赖的充分条件。

> “当你开启项目时，你需要尝试赢得人们的信任，消除他们对于加入项目的疑虑，而且放心的使用你的代码。在这之后，如果你说：‘大家好，这个项目可能无法继续了。‘ 这对于信任一点帮助都没有。而你应该说，如果有一天，项目可能不得不结束，您将会尽全力去解决问题， 并且应该保证您不会将用户弃之不顾。告诉他们，您会告知他们您的每一步工作的内容。在进行项目转交时，给他们时间去适应，您还需要努力帮助完成项目转交时可能有所帮助。” – Dr. David A. Wheeler，Linux基金会[核心基础设施研究](https://www.coreinfrastructure.org/) （CII）开源专家和两个项目的领导者。

## 决定您何时结束、转交或退出一个开源项目

无论什么原因，都可能遇到这样的几种情形：开源项目需要终结、需要转交给其它实体单位、亦或者是贵司决定从某参与的项目中退出，无论哪种情况，都要做出决断的。至于原因吗，有可能是贵司的目标发生了变化，也有可能是项目和新的方向不再匹配，又或者是项目的关键人物/团队离开了公司，亦或是项目的成长情况：参与度、更新周期、采用的下降等因素所导致。也有可能是因为在关于项目未来发展的问题上，社区成员之间出现了分歧，这些使项目看起来需要做出一些改变。

### 分歧会影响新项目的方向

在项目的社区内部如果发生了严重的分歧 ———— 不管这个分歧是什么，关于技术也罢，许可协议等等 ———— 你都得考虑项目需要分离，让对不同方面感兴趣的人们做他们认为重要的事情！我们可以回顾一个例子，就分离这件事对于1991年创建 Linux的开发者 Linus Torvalds 来说触动很大，Torvalds 一直以来都是基于Minix进行开发的，Minix 以一款类Unix的小型操作系统，其内核由Andrew S. Tanenbaum所开发，主要是用来教学。随着项目的发展，和Torvalds对其范围和愿景的不同，Torvalds 将项目从 Minix 分离出来创建了日后重要的开源项目Linux。

毫无疑问，随着时间的发展，项目的范围肯定会有所变化，一定范围的调整是必须的，但是如果项目不再被需要，那么就应该尽早的去考虑将之分离，或者转交。甚至可以重新调整项目的用途，从而找到让现有用户更为满意的方式，又或者是通过合并新功能来吸引新的用户。但是还是有可能最不愿意看到的结果，真的没有人需要贵司的软件了，那么也就说明这个项目的生命周期走到了终点。哪怕是这个世界上最为优秀的软件，如果再也没有人需要它，使用它来完成一些事情的话，那么它的存在意义就归于历史了。

> “项目总是不可避免的以不同的方式终结！在Facebook，我们可能会因为转向其它项目而停止使用现有的项目和代码，也可能是维护者由于其它事情而离开了项目，甚至离开了公司。再也没有人维护这些项目了，而且也不在我们的应用使用它们了，这些都是很正常的事，重要的是我们曾经使用过它们，它们发挥过作用！” – Christine Abernathy，Facebook 开源团队开发者布道师


### 来自一线用户的实例

对于企业用户来讲，决定一个开源项目是否终结所考虑的范围是很广的，对于软件厂商 AutoDesk 来说，拥有190多个开源项目，且都在使用中。其中对于项目开发来说参与者的减少是一个非常明确的信号，它说明该项目有过时的迹象，那么就会让该项目进入“维护模式”。在这样的情形下，项目的代码维护就不会太活跃，这时如果项目的使用者提出问题，那么极有可能得不到任何的答复。这个时候，也就意味着，项目的社区成员可以继续使用，但是社区不再提供任何的支持。

我们再来看看Facebook，截止目前为止，Facebook 已经开发了超过400多个开源项目，Facebook 会对所有的指标进行监控和追踪，比如补丁和维护的情况，而且做到了定期审核正在进行的项目的状况。同样，对于 Capital One 来说，大约有20个开源项目已经在内部启动并进入使用中，根据公司的需要，这些项目可能会定期转交给其他组织或结束。

## 如何关闭一个开源项目

无论你做什么，对于一个或终结或转交的开源项目来说，也许最为重要的就是做的每一步的想法都要和用户分享。公开你的打算有助于未来赢得社区开发者建立信任。

一旦你决定了往哪里走，你必须敲定在哪里结束，或者移交给其它的组织，或者是直接退出项目，从此不再直接参与。

### 该如何交接一个项目

通过转交项目给其它组织，让项目继续得到维护和发展，你需要做的是将项目的数据和其它资源要悉数提供，这样可以有效减少现有社区及其用户的担忧，如果项目使用的是通用或标准的界面，可能更容易提取或移动嵌入式数据，或者在需要时用其他有类似界面的项目来替代。当然，这并不总是有效，因为很明显，有一些开源项目是独一无二的。但是，在项目计划完成周期的早期阶段，提供和使用标准化界面有助于简化项目的转交过程。

> “ 结束项目的最佳实践就是将项目所有的信息都公开。如果你不再支持自己的项目，或者是打算关闭某个项目，对于任何会偶然发现你的代码的人来说，这么做对于他们来说是善莫大焉。你让他们知道该项目已不再维护，那么新人看到这些信息之后，就会考虑不再采用。” – Jared Smith，Capital One 开源社区经理

### 在交接项目时进行必要的更新

转交项目还有一个好处，就是在最初的开发社区首次创建并维护这个项目的之后很长一段时间内，还可以继续向其他用户提供代码。当然，不仅仅是代码可以继续使用。文档、参与者许可协议（CLAs）、项目存储库、wikis、用于项目转交的网站以及可能需要审查和更新的一些支持性基础架构也都可以继续使用。项目的转交可以通过实际的转交程序来完成，也可以通过将主要项目和其他资源转交给新的用户群来完成。

还有一种方法可以代替转交，企业可以把项目移动到一个新的托管平台，通过让社区成员访问一个可继续运行项目的中介网站然后来访问项目，而不必完全退出项目。

> “转交不会经常发生，但在过去，我们的一个项目就转交给了另一家公司。特别要说明的是，我们只是将该项目转交给其他公司，但对此转交过程没有任何硬性规定。当该项目需要在团队之间进行转交时，我们先在内部进行了一些调查，确认是否还有人在使用这个项目。因为我们一直致力于让我们的开源项目被内部使用，所以，可能会有一个和我们完全不同的团队正在使用这个项目。如果他们愿意维护这个项目，那么我们将毫不费力地将项目转交给这个与我们不同的团队。但这仅仅意味着项目的所有者改变了。” – Christine Abernathy，Facebook 开源团队开发者布道师

### 彻底的关闭项目

还有一些公司想着草草了事，简单粗暴的将项目直接关闭，至于原因有可能是法律方面，也有可能是来自竞争对手的压力。当然说到底贵司企业的方向的决定权仍然在贵司手上。其实完全没有必要做的那么绝，比如代码就不必删除，而是将其归档，亦或是置为“只读”，这样就给后来者有 Fork 的机会，即使没有贵司的参与，项目仍然可以继续发展。此外，代码也可以被移动到一个为用户进行存储的存档站点。

要始终谨记，虽然贵司对于项目的代码不再关心，但是这并不代表社区不需要这些代码。而且你应该提醒社区成员，在没有贵司参与的情况下去尽情的Fork代码吧，按照自己的需求来进行下一步的开发。同时，也应该告诉对开源代码有依赖的用户，最好的做法复制一份镜像保存下来，说不定哪天代码仓库就不再使用了，拥有一份可用的备份或镜像有备无患。

为了能够确保所选择的内容均能够有效实施，按部就班、井然有序的规划是保证一切进展顺利的最佳选择。这也就是意味着清晰而尽早的与用户沟通，并规划相应的时间点，以便那些会受到影响的用户能够有足够的时间来完成工作，并在有需要时转移数据到其他平台。那么问题来了，用户究竟需要多长时间算是足够了呢？这样看实际的情形了，至少6个月，或者更长点。关键点在于给用户设置合理的期望时间，并且要频繁地与用户清楚地沟通了解您的计划。

如果贵司是将项目转交给其它的组织，那么就更应该时常更新信息和用户保持同步，以保护用户的利益。

### 努力实现平稳过渡

当一家靠谱的合作伙伴定下来之后，接下来就要去实施你的退出计划了，这就像对待一款停止生产的产品一样。如果贵司要参与到项目交接过程中的话，那么请根据开发人员的时间，来决定贵司将如何参与，然后与新的伙伴紧密合作，从而为顺利过渡做好准备工作。请做好思想准备，实际交接过程可能需要几个月才能完成，在所有必要的准备工作都完成后，就可以将项目正式转交给新的项目所有者了。

说的是蛮轻松的，但是实际上可能会遇到各式各样的问题，比如说接手贵司项目的团队并不是你所期望的那样，这是经常发生的事情，那么你就有必要针对这样的情况作出必要的准备。那么你究竟该如何处理这样的情况了呢？好吧，如果你确实很依赖这些代码，以至于开始思考拒绝将项目转交给一个和贵司完全不同的组织、又或者价值观完全相悖的团队，对于结束项目的时机产生了怀疑。如果你真的有以上这些顾虑的话，那么问题只有一个：你不应该离开这个项目。

### 明确沟通的重要性

哪怕是项目已经完成交接，那么有关交接后的新的方向、退出计划、重新包装新的项目等和用户保持清晰的沟通，这些仍然是你的责任。请确保就项目的状态、新的运营者等信息和开发者、社区成员开诚布公，而且要给他们清晰的细节，如他们继续使用项目的话如何维护等。请不要忘记更新项目的站点、社交媒体频道、以及其它和社区有联系的渠道，从而让用户能够知道在哪里可以找到已经转交的项目，可以继续做出贡献并使用代码。

请务必谨记：以上所有沟通的信息要传达到项目下游的组织和用户，其中包括公司、非盈利组织、以及其它仅仅使用代码的用户、还有那些因为没有直接参与到开发周期中而可能不知道项目结束或转交的人。贵司应该通过官方网站、社交媒体频道、以及其它各种渠道，告诉以上这些人，尤其是项目已经很有名气且拥有大量追随者的情况下。

> “沟通中最重要的事情莫过于尽可能快速的将变更公布到社区中。千万不要让用户对项目的继续维护有虚假的希望，对于大部分情况，好的代码自己会进化，拥有强大的生命力。所以如果你的项目拥有优质的代码，请告诉人们该项目不再会维护了，而不是从GitHub将其撤掉。” – Guy Martin，Autodesk 开放总监

### 通过项目的仓库提供信息更新

另外一个贴出有关项目变更的信息的绝佳地方是项目 GitHub 的仓库或类似的地方。因为是源代码，你大可将详细的细节描述一番，以解释发生了什么，包括用自述文件向项目参与者发送信息以便了解情况。

随着项目的进行，是时候正式的交接项目的资产到新的运营者。如果在维护现有公司实际资产的过程中，你引入了新的管理人员，那么你将可以保留因为项目变化而受到影响的代码的版权，并让他们通过开源许可证来使用其所选择的代码。

为了保持项目仓库的维护井井有条，你应该考虑设置一个专门的地方，该地方用来存储和让人们访问那些贵司已经不再支持的开源项目（如 https://github.com/twitter-archive）。这样的话，用户仍然能够访问到项目并获取代码，另外用户也可以从 Readme 文件的解释中了解到项目的状态。此种特定的仓库可以为用户提供清晰的解释内容，帮助他们理解活跃项目和退休项目之间的区别，同时也可以确保企业能够在活跃的仓库中适当地展示其最新的开源项目。

### 锦囊妙计

归档项目的时需要参与一些具体的步骤。举例来说，仅仅将项目变成只读状态将有利于清楚地说明，在毋须更改访问地址的情况下，现在该项目已经归档，不再像以前那样可以定期更新。

另外一个蛮重要的事情就是为用户提供项目的可替代方案，如如何获取代码，Fork 代码以便于未来的使用。作为开源项目责任的一部分，你还应该提供能够让用户联系到你的方式，从而他们能够将其所 fork 的项目列出并提供给其他感兴趣的用户。一些公司会提供这种帮助，而其他公司则不会提供。

一旦仓库归档完成，你就不能在添加或删除合作者或团队了，而且 issues 也会变成只读的。如果要对归档的仓库进行更改，那么你要首先将仓库解档。请参考 GitHub 文档了解详细细节[https://help.github.com/articles/about-archiving-repositories/](https://help.github.com/articles/about-archiving-repositories/)

### 当关闭项目时基础设施也要更新

关闭一个项目也会影响都项目的基础设施和支持环境，至于影响到什么程度，则取决于项目当初的设置，并且要实事求是的根据实际情况进行灵活的判断。一些项目使用和维护的是较小的代码，这样的话就不需做太多。如果项目包含了全部代码，并且已经被发布到了仓库中，那么说明已经完成了所有工作，而不需要再采取其他行动再来转交或维护项目

还有一些项目，可能需要使用各种后台工具来完成工作，所以结束这些项目需要付出一定的努力。这些项目可能包括一些额外的用户多种目的的共享服务，如测试的基础设施。尽管这些测试的基础设施在过去有很多的用处，但是由于项目的转移，那么你可能也需要将之清理出来，以用于后面的其它的测试。它们或许在分离的过程蛮有难度，但是仍是那句话：功夫不负有心人！只要去做就会完成。

> “ 作为公司 **真的需要** 对开源做出好的规划，在没有做任何的规划而只是简单的将项目扔在哪里，就指望公司以外的人参与进来，而且希望他们能够长久的进行贡献，这么去想无异于痴人说梦。你必须去做大量的准备，这些社区成员，有些是来自贵司，有些则是来自其它地方，但是无论是谁，既然参与进了项目，成为了社区成员，就应该有一个成长的路径，或成长，或退休，必须是善始善终的。” – Guy Martin，Autodesk 开放总监

### 要做好接受负反馈的准备

总是会有一些针对贵司行为的负面的公开讨论和交互，如不爽的用户、以及那些称关闭项目就是抛弃用户的道德绑架。请时刻谨记，大多数用户都能够理解贵司的意图，事情的优先顺序会随着时间而变化，公司不可能长期去维护一些没有实际意义的项目，大多数时候这些项目已经成熟。每个公司都必须这样做，所以请不要过于在意这些评论，而且也相信它不是针对你个人的。

## 最后的思考

项目关闭、转交给其它实体或个人、以及退出一个开源项目，对于一家商业公司来讲，这些都是很正常的事情，要在恰当的时间做出必要的准备才是应该直面的现实。事情要往好处想，这未必是一件会该贵司带来负面影响的坏事，相反，处理妥当，则会皆大欢喜。所谓的事在人为，当然这也对当事人们提出了一点点要求，正确的计划、明确和广泛的沟通以及法律和程序性任务的逐步完成，开源项目的过渡目标是可以圆满完成的。

即使你的项目还处于规划的首要阶段，也要去思考和规划一个简要的开源计划书，这样可以确保有一个健康的生命周期管理计划，该计划将会帮助贵司的开源项目从目标高远的开始到最终平稳结束的整个过程中，高效并成功地运作。

## 致谢

本指南贡献者：

* [Christine Abernathy](https://twitter.com/abernathyca)，Facebook 开源团队开发者布道师
* [Chris Aniszczyk](https://twitter.com/cra)，CNCF 首席技术官 （原Twitter的开源部门带头人）
* [Guy Martin](https://twitter.com/guyma)，Autodesk 开放总监
* Jared Smith，Capital One 开源社区经理
* [Dr. David A. Wheeler](https://www.dwheeler.com/)，Linux基金会核心基础设施研究（CII）开源专家和两个项目的领导者

> 这些资源是与TODO（公开对话，开放式开发）小组 – Linux基金会的专业开源程序网络小组合作创建的。 特别感谢那些贡献自己的时间和知识来制作这些综合指南的开源项目经理。 参与的公司包括Autodesk，Comcast，Dropbox，Facebook，Google，Intel，Microsoft，Netflix，Oath（Yahoo + AOL），Red Hat，Salesforce和Samsung。 要了解更多信息，请访问 [todogroup.org](http://todogroup.org/)。我们邀请您在GitHub上下载、传播，如果可以请积极的参与这些指南。
