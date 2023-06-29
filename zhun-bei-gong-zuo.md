# 准备工作

本章我们将会介绍在本书中会使用的各种软件和工具，但不是全部，对于部分涉及工具链的配置我们会在对应的项目部分说明。

注意，由于各平台的大多数操作都是相同的，在部分小节中笔者只会提及有差异的部分，并且由于笔者目前并没有体验过 Mac 的操作系统，故 Mac OS目前仍为 todo 状态。

## Windows

这是大多数人使用的系统，也是笔者的开发环境。

### 代理工具

虽然我并不想过多的谈及这个话题，但是鉴于大陆地区越来越严重的各类阻断和污染，使用代理工具和配置透明代理环境几乎已成为开发的必要操作了。

在这里我推荐使用开源的 Clash GUI，[clash verge](https://github.com/zzzgydi/clash-verge/releases) 用于配置代理。注意，为了能够代理所有流量，请在设置里启用服务模式并开启tun模式，此时 Clash 会为你的系统安装一个虚拟网卡用于分流和代理流量。

由于不是所有的 \[已删除] 都会提供已经配置好 Clash 分流规则的神秘链接，甚至部分\[已删除]都没有提供 Clash 格式的神秘链接，所以你可能需要一个转换服务，你可以访问[此项目](https://github.com/tindy2013/subconverter)用于自行搭建转换服务。

此外还有一些其他的代理软件选择，例如著名的 cfw (clash for windows) 和 v2rayN 等。

如果对于 \[已删除] 的安全性有担忧，可以考虑自己租用服务器并搭建，视频教程可以参考 youtube 频道 [不良](https://www.youtube.com/@bulianglin)&#x20;

### 包管理器

[Scoop](https://scoop.sh/)，Windows下非常实用的包管理器，在安装 Scoop 后推荐安装 gsudo 用于部分提权操作。

```powershell
scoop install sudo
```

### IDE和编辑器

1. [Visual Studio Code](https://code.visualstudio.com/)，全平台可用的编辑器，可以通过安装各类插件实现近似与 IDE 的开发体验。
2. [Jetbrains Toolbox](https://www.jetbrains.com/toolbox-app/)，用于管理 JB 的各种 IDE，全平台均可使用。
3. (可选) Visual Studio，微软的 IDE，主要被用于在Windows平台下开发 c++ 和 .net ，但是在本书中，我们只会用其来安装Windows下的MSVC 工具链。
4. (可选) Kate，KDE项目的文本编辑器，使用 C++ QT 编写，非常的快，只是想快速编辑文件时可以试试看。

### Shell和终端模拟器

在 Windows 平台上我推荐使用新的 powershell 和 Windows Terminal。

为了避免某些特殊问题，请使用安装版而不是商店版，简而言之，去对应的 GIthub 仓库寻找对应你系统的安装包，例如如果你是 x86-64 的 Windows 环境就在其中寻找包含 "x64" 和 "msi"或者"exe" 这种字段的安装包。

Windows Terminal 直接在微软商店搜索安装即可，注意，安装后其应用名称可能会变为"终端"。

### WSL

注意有很多时候开发或学习必须得使用 Linux 环境，传统方式下我们是在虚拟机下完成相关环境的配置。但是在绝大多数情况下，我们并不需要一个完整的桌面环境，此时，WSL2 就成了一个相当有吸引力的选择了。

简而言之，在微软商店里搜索有支持的 WSL 发行版即可，著名的 Ubuntu 就提供了对应的 WSL 发行版，安装后在 Windows Terminal 中会自动添加配置文件，需要使用其 shell 时在其下拉菜单中即可选中打开。

### 非跨平台实用工具

1. [powertoys](https://github.com/microsoft/PowerToys)，微软开发的实用工具集合。
2. [rufus](https://rufus.ie/zh/)，用于烧录系统。
3. [everything](https://www.voidtools.com/zh-cn/)，基于 NTFS 文件系统的文件搜索工具。
4. [utools](https://www.u.tools/)，国人开发的实用工具集合，非开源。

## Linux

由于笔者使用的发行版（实体机）只有 arch 系，所以这里以 arch 和 KDE 桌面环境为例。

### IDE和编辑器

{% hint style="info" %}
与 Windows 平台一致。
{% endhint %}

### 代理工具

[v2raya](https://github.com/v2rayA/v2rayA) ，开箱即用的透明代理，如果需要转换神秘链接，参考 [Windows 代理工具](zhun-bei-gong-zuo.md#dai-li-gong-ju) 一节。

### 包管理器

不同的 Linux 发行版会有不同的包管理器和打包格式，但是大体上使用方法都是类似的。为了精确查找对应的使用方法，你可以在对应发行版的 Wiki 上查找资料，或者使用搜索引擎查找相关的资料。

### shell和终端模拟器

一般来说 bash 已经可以满足大多数人的需求了，但是出于美观和实用性的考虑，绝大多数人都会使用 zsh 和 fish 等新的 shell，如果你需要进行美化工作，请使用搜索引擎查找对应的信息。

终端模拟器就更加百花齐放了，笔者只用过 konsole (KDE的默认终端模拟器) ，为了找到独属于你的心头肉，不妨尝试使用搜索引擎搜索对应的关键词，或者问问 new bing 有什么推荐（？

## Mac OS

todo ...

## 多平台均适用的工具

### USB烧录工具

[balenaEtcher](https://www.balena.io/etcher)，使用electron编写的跨平台USB烧录工具，虽然体积有些臃肿，但是操作非常简单友好，适用于装系统等简单的活计。

### 翻译工具

#### Deepl

在前 chatgpt 时代非常好用的翻译工具，翻译准确度相较于传统的谷歌翻译等有很大的提升。

#### 欧陆词典

多平台均可使用的专业词典。

#### Google Translate 插件

用于在浏览器中阅读时划词翻译。

#### 沉浸式翻译

调用各类翻译接口来翻译网页，特色是翻译后的结果并不会覆盖原文，而是以双语对照的形式呈现。

### 语言模型

#### chatgpt

基于 OpenAI 的大型语言模型的聊天bot，非常实用，对于大陆地区用户，注册需要接码平台。另外，其训练数据截止于2021年末，所以不能生成最新的信息。

#### New Bing

微软开发的AI助理，可以通过搜索引擎整合最新的信息，撰写文章和生成图片，但是对话时有上下文数量限制。注意，大陆地区用户需要为其配置非大陆的IP才能使用，可以考虑使用代理工具分流。

### 实用的网站

#### Cyberchef

[Cyberchef](https://gchq.github.io/CyberChef/), 赛博瑞士军刀，可以方便的进行各种编解码工作。

####

