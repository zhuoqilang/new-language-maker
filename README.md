# 外星通讯工具 - Alien Communicator

## 项目介绍

外星通讯工具是一个基于Web的单页应用，旨在提供一个实验性的语言交流环境，让用户能够使用独特的符号系统进行通讯。该项目源于对语言起源和创造新语言可能性的探索。

### 项目起源

#### 2019-2-16
项目最初只是一个想法。它始于一个问题：为什么人们不创造一种新的自然语言？事实上，这是一个错误的问题。许多人正在或曾经致力于此。但所有这些新语言都不够有活力。

重新思考这个问题，我相信将会有许多新语言，其生命力取决于它的价值。换句话说，为什么以及如何需要一种新语言？

我认为我需要一种新语言，在其中我可以自由交谈。肯定还有许多其他类型的价值，它们将催生其他新语言。其中一些会成长起来，谁知道呢。

因此，为新语言的诞生创造一个有益的环境是必要的。

#### 2019-3-1

"new-language-maker"是一个环境。

首先考虑个人电脑的情况，使用标准键盘输入。

该环境包括输入法，具有词汇联想和拼写检查等功能。这要求每个人都有自己的词库。

词库有两种类型，一种是公共的，即每个人都可以选择和参与更新。一种是私有的，只在一组相互认可的用户之间共享和更新。

前者产生一些"共同语言"，后者产生"私人语言"。

上面只考虑了词汇。如果需要发展语法，情况难以想象。最好不要先发展语法，让语法自行生成，然后在语言成熟后再总结。就像每一种现存的自然语言的诞生一样。

#### 2019-3-3

考虑一种游戏，在这个游戏中，游戏者可以互相以键盘输入的文本来交流。但是你输入的文本，在其他人看来却不再是原来的样子，而是经过某种算法的转换，也就是说看起来成了乱码。但是这个乱码和原来输入的文本是对应的，也就是第一个人输入某一个确定的词，再另一人看来就一定是确定的"乱码"。不同人看到的是不同形式的乱码。

游戏的最高目标是玩家互相可以交流。但是首先我们要选择一个合适的算法，避免其易于被反向破解。

这时，造词者需要描述他的新词语，接收者则要学习后才理解这个词语的含义（他看到的并非原本的字母组合，而是"乱码"）。

如何描述新词汇是困难的。在双方没有双方共同认识的词语的情况下。需要有一个合适的反馈机制。

#### 2019/3/12

我设计了如下实验方案，是关于语言起源的试验。
首先我们利用一个哈希算法的软件，让自己的符号变得不可识别，并基本无法反向破解。然后建立自己的符号库，可以用现有文字，就比如"是"、"否"、"0"、"1"等等。

我举了一个交流的例子，展示了如何通过符号的组合来解释符号，以便让接收者理解这些符号。这个试验需要多人参与，并建立了一个QQ群"语言试验"（779728193）。

## 当前版本核心功能

1. **词汇表管理**
   - 添加和管理自定义词汇
   - 每个词汇自动生成唯一的3符号组合
   - 支持添加词汇注释

2. **联系人管理**
   - 创建和管理联系人列表
   - 记录每个联系人的基本信息

3. **通讯中心**
   - 使用词汇表将文本消息转换为符号序列（加密）
   - 将收到的符号序列转换回文本（解密）
   - 支持通过词汇表和破解笔记进行解密

4. **聊天记录**
   - 保存与每个联系人的通讯历史
   - 显示原始消息和转换后的符号序列

5. **破解笔记**
   - 记录未知符号的可能含义
   - 辅助解密过程

### 技术特点

- 使用Tailwind CSS构建现代化UI界面
- 基于localStorage实现数据持久化存储
- 采用16个独特符号构建通讯系统
- 完全客户端实现，无需后端服务器

## 今天的讨论内容

- 确认GitHub Pages已激活，项目可通过 https://zhuoqilang.github.io/new-language-maker/ 访问
- 将原始HTML文件重命名为new-language-maker-V0.1.html，作为版本记录
- 讨论了项目升级方案，考虑通过邮箱列表实现用户间的基础交互
- 创建了开发日志文件，记录项目开发过程

## 后续计划

1. **用户系统实现**
   - 探索基于邮箱的用户列表管理方案
   - 实现简单的用户间联系方式共享

2. **功能增强**
   - 优化符号生成算法，提高唯一性
   - 增加更多自定义符号选项
   - 改进消息加密和解密机制

3. **用户体验**
   - 添加响应式设计，支持移动设备
   - 优化UI界面和交互流程
   - 增加使用教程和引导

4. **数据同步**
   - 探索跨设备数据同步方案
   - 考虑引入云存储选项

---

# Alien Communicator

## Project Introduction

Alien Communicator is a web-based single page application designed to provide an experimental language communication environment, allowing users to communicate using a unique symbol system. This project stems from the exploration of language origins and the possibility of creating new languages.

### Project Origin

The project originated in 2019 with a simple question: why don't people create new natural languages? After some research, it was discovered that many people have worked on this, but most new languages lack vitality. The project evolved into an experiment to explore how new languages might emerge and gain vitality through a collaborative environment.

### Core Features

1. **Vocabulary Management**
   - Add and manage custom vocabulary
   - Each word automatically generates a unique 3-symbol combination
   - Support for adding word notes

2. **Contact Management**
   - Create and manage contact lists
   - Record basic information for each contact

3. **Communication Center**
   - Convert text messages to symbol sequences using vocabulary (encryption)
   - Convert received symbol sequences back to text (decryption)
   - Support for decryption through vocabulary and cracking notes

4. **Chat History**
   - Save communication history with each contact
   - Display original messages and converted symbol sequences

5. **Cracking Notes**
   - Record possible meanings of unknown symbols
   - Assist in the decryption process

### Technical Features

- Modern UI interface built with Tailwind CSS
- Data persistence using localStorage
- Communication system based on 16 unique symbols
- Fully client-side implementation, no backend server required

## Today's Discussion

- Confirmed GitHub Pages is activated, project accessible at https://zhuoqilang.github.io/new-language-maker/
- Renamed original HTML file to new-language-maker-V0.1.html as version record
- Discussed project upgrade plan, considering implementing basic user interaction through email list
- Created development log file to record project development process

## Future Plans

1. **User System Implementation**
   - Explore email-based user list management solution
   - Implement simple contact information sharing between users

2. **Feature Enhancement**
   - Optimize symbol generation algorithm to improve uniqueness
   - Add more custom symbol options
   - Improve message encryption and decryption mechanisms

3. **User Experience**
   - Add responsive design to support mobile devices
   - Optimize UI interface and interaction flow
   - Add usage tutorials and guidance

4. **Data Synchronization**
   - Explore cross-device data synchronization solutions
   - Consider introducing cloud storage options
