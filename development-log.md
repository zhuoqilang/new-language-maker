# 项目开发日志

## 2024年X月X日

### 今日进展

1. **项目文件整理**
   - 将原始HTML文件重命名为`new-language-maker-V0.1.html`，作为第一个版本的记录
   - 创建了`README.md`文件，包含项目介绍、核心功能、技术特点和后续计划
   - 创建了`development-log.md`日志文件，用于记录开发过程
   - 保留了`email_list_implementation.md`文件，作为未来实现邮箱列表功能的参考方案

2. **GitHub Pages确认**
   - 确认GitHub Pages已成功激活
   - 项目可通过以下URL访问：https://zhuoqilang.github.io/new-language-maker/

3. **功能回顾与评估**
   - 分析了外星通讯工具的现有功能：词汇表管理、联系人管理、通讯中心、聊天记录和破解笔记
   - 确认当前实现完全基于客户端，使用localStorage进行数据存储
   - 识别出未来可能的功能增强点

### 讨论内容

1. **项目升级方向**
   - 讨论了通过邮箱列表实现用户间基础交互的方案
   - 考虑简化服务器需求，通过GitHub Pages收集用户邮箱信息
   - 探索用户间通过邮箱直接交互的可能性

2. **技术方案探讨**
   - 分析了GitHub Pages的静态特性限制
   - 讨论了使用第三方表单服务或GitHub Issues API收集用户邮箱的可能性
   - 考虑了邮箱列表的展示和更新机制

### 后续计划

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

## 联系方式

项目负责人：zqwolf@163.com

---

日志将持续更新，记录项目的每一步进展和重要决策。

2019-2-16:
It's just a idea, for now.

It starts from a question: why don't people make a new language (natural language)? Actually, it's a wrong question. Many people working or worked on it. But all these new languages are not vitality enough.

Rethinking from this, I believe there will be many new languages, its vitality depend on its benefit. In other words, why and how necessary you need a new language？

I think I need a new language, in which I can talk freely. There must be lots of other kind of benefit, and they will give birth to other new langueages. Some of them will grow up, who knows. So it's necessary for a environment, which is helpful for a new language to be born.

2019-3-1
“new-language-maker” is an environment.

First consider the case of a PC, using a standard keyboard input.

The environment includes input methods and has the functions like word association and spell checking. This requires everyone to have their own thesaurus.

There are two types of thesaurus, one of which is public, that is, everyone can selected and participate in the update. One is private which is shared and renewed only among a group of users who have recognized each other.

The former produces some "common language" and the latter produces "private language."

The above only considers vocabulary. If you need to develop grammar, the situation is hard to imagine. It is better not to develop a grammar, let the grammar generate itself, and then summarize it after a language is mature. Just like every existing natural language was born.

2019-3-3
Consider a game in which players can communicate with each other using text entered by the keyboard. But the text you enter, in other people's eyes, is no longer the original, but is converted by some kind of algorithm, which means it looks garbled. But this garbled corresponds to the originally entered text, that is, the first person enters a certain word, and the other person seems to be a certain "garbled". Different people see different forms of garbled characters. This is similar to the information that everyone receives with their own private key. If the person enters this garbled back to the first person, the first person receives the word he originally entered.

The highest goal of the game is that players can communicate with each other. But first we have to choose a suitable algorithm to avoid it is easy to be reversed.

At this time, the creator needs to describe his new words, and the recipient has to learn to understand the meaning of the word (he does not see the original letter combination, but "garbled").

How to describe new words is difficult. In the case where there is no word shared by both parties. Need to have a suitable feedback mechanism.

In real life, this feedback mechanism comes from real life scenes. What should be in this game?

2019-3-3 考虑一种游戏，在这个游戏中，游戏者可以互相以键盘输入的文本来交流。但是你输入的文本，在其他人看来却不再是原来的样子，而是经过某种算法的转换，也就是说看起来成了乱码。但是这个乱码和原来输入的文本是对应的，也就是第一个人输入某一个确定的词，再另一人看来就一定是确定的“乱码”。不同人看到的是不同形式的乱码。这个类似每个人把收到的信息，用自己的私钥进行过加密。如果这个人输入这个乱码回去给第一个人，第一个人收到的就是原本他输入的那个词。 游戏的最高目标是玩家互相可以交流。但是首先我们要选择一个合适的算法，避免其易于被反向破解。 这时，造词者需要描述他的新词语，接收者则要学习后才理解这个词语的含义（他看到的并非原本的字母组合，而是“乱码”）。 如何描述新词汇是困难的。在双方没有双方共同认识的词语的情况下。需要有一个合适的反馈机制。 现实生活中，这个反馈机制来源于现实的生活场景。而在这个游戏中应该为何？

2019/3/12 I designed the following experimental protocol, which is a test about the origin of language. First, we use a hash algorithm software (https://www.jianguoyun.com/p/Db2_B4QQ-aSRBhjDoaYB) to make our symbols unrecognizable and cannot be reversed. Open this "hasher" software, the verification type is the default MD5. Then build your own symbol library. You can use existing text, such as "yes", "no", "0", "1", and so on. Enter "yes" into the string input box of hasher and it will be hashed to: EFDFAD1EC7B4099DEC98B579737146BB. --- But there is a problem with this. Although the hash value cannot be cracked, it can be tested. For example, if you input the word "yes" and find that the hash value is the same, then you know what my original string is. It is. So everyone has to put a string (equivalent to the private key) in front of the string and keep it secret to others. For example, if my string is "myid:", you should enter "myid: yes" when you enter "yes" to get EE452B7B6063A18A3F4C3468C68FE778 (my "yes" here is a Chinese character, but this does not affect the discussion below). This way, you don't have to worry about the original string being tested. Now let me give you an example of communication: I have set multiple characters. And send you the transformed hash value. I need to seriously consider the need to set those symbols, and how they are combined, and then send them to you, hoping to help you use the combination of symbols to interpret the symbols so that you can understand them more easily. Now I set "yes", "no", "0", "1", and convert "myid: yes", "myid: no", "myid:0", "myid:1" to a hash value Four hash values: EE452B7B6063A18A3F4C3468C68FE778; 95194BCBEBE20754877C5A125CE072FB; 9308818AE16C68E79D967E0A8AF4EED0; D98FF4589F45A47EE7261D0C22B1713F. In addition, I feel that there is a sufficient need for everyone to have a common identifiable signal representing “empty”. This signal is defined as a hash of a space (enter a space in the string), 7215EE9C7D9DC229D2921A40E899EC5F, everyone uses this symbol, do not add their own private key. In other words, we see that 7215EE9C7D9DC229D2921A40E899EC5F everyone knows that this represents empty, everyone uses this representative. Now I want to send you the following signal: "0 is 0 1 is 1 0 no 1 1 no 0", I hope this helps you understand the meaning of "yes" and "no". In the above quotation marks, all characters "0, 1, yes, no, and spaces" are converted to hash values, which I sent to you in the above order. When you receive this string of hashes, the only thing that knows beforehand is the empty hash value, and then you can only distinguish whether the hash values of other unknown meanings are equal. The three symbols representing the empty symbols may allow you to consider that the string is four parts, then examine each part and find that the first and third are the same hash value, the second The hash values are all EE452B7B6063A18A3F4C3468C68FE778. In the first and third different cases, the middle is 95194BCBEBE20754877C5A125CE072FB. From this, I wishfully guessed that you might be able to confirm that the two represent "yes" and "no" respectively. More likely, your understanding may be different, but quite close, for example, if you think it means "equal" and "not equal." You will record my "yes" and "no" hashes and remark them as "equal" or "not equal". When you think you understand, there is another trouble, how do you let me know that you understand. I guess you will send me a sentence with a similar structure. But you can't send my hash value directly to me. According to the rules of the game, all the symbols you send should also be hashed. Suppose your vocabulary has four characters "equal", "not equal", "A" and "B". Before adding your private key "yourid:", you are actually sending the converted "A equals A sequence of ABs equal to the hash value of BA which is not equal to BB not equal to A". When I see your feedback like this, I tend to think that you understand my meaning of "yes" and "no". Of course, I am sure that your "A" and "B" will happen to correspond to my "0". 1". So I put two hashes of your "equal" and "not equal", and me to "yes" and "no". As for your "A" and "B" I am still remarking as "Unknown number 1" and "Unknown number 2". Now we have a set of vocabulary between each other. When you send the two hashes "equal" and "not equal" later, I think I understand what they mean. Although it seems that the mutual understanding between us is simple and rough, it is not practical. However, at least a consensus has been reached. Is this the beginning of language when it first originated? Starting with the basic symbols, if you can continue to develop more symbols of mutual understanding, can you develop more and more complex symbols until the language is formed? In addition, I feel that there are some conditions that are too restrictive in the formulation of the rules of the game. In addition to the null value, this hash value is known by default. There is no other living environment between us to identify the symbol. (The two primitives can look at an apple plan and immediately understand each other with the word Apple.) This setting will increase the difficulty, but it is not meaningless. Suppose an alien civilization can only communicate with us by transmitting signals. How to understand each other is similar to the situation in the game. This experiment requires multiple participants. I built a QQ group, 779728193 "Language Test"

2019/3/12 我设计了如下实验方案，是关于语言起源的试验。 首先我们利用一个哈希算法的软件（https://www.jianguoyun.com/p/Db2_B4QQ-aSRBhjDoaYB），让自己的符号变得不可识别，并基本无法反向破解。 打开这个“hasher”的软件，校验类型是默认的MD5。然后建立自己的符号库。可以用现有文字，就比如“是”、“否”、“0”、“1”等等。把“是”输入hasher的字符串输入框，就会的到哈希值：EFDFAD1EC7B4099DEC98B579737146BB。---但这样做有一个问题，虽然哈希值无法破解，但是可以被试探出来，比方你也输入“是”这个字符，发现哈希值相同，则你便知道我的原字符串是什么了。因此每个人要在字符串前加一个固定的、只有自己知道的字符串（相当于私钥），比如我的输入是“myid：是”，得到EE452B7B6063A18A3F4C3468C68FE778。这样就不担心被试探出原字符串。 现在我举个交流的例子： 我设置了多个字符。并向你发送其变换后的哈希值。我会认真考虑需要设定那些符号，以及这些符号用什么方式组合起来发送给你，并有助于利用符号的组合来解释符号，以便让你理解这些符号。 现在我设置了“是”、“否”、“0”、“1”，并将“myid：是”，“myid：否”，“myid：0”，“myid：1”变换为哈希值4个哈希值：EE452B7B6063A18A3F4C3468C68FE778；95194BCBEBE20754877C5A125CE072FB；9308818AE16C68E79D967E0A8AF4EED0；D98FF4589F45A47EE7261D0C22B1713F。 另外，我觉得有充分的必要让大家有一个共同可以识别的，代表“空”的信号。这个信号定义为一个空格的哈希值（字符串中输入一个空格），7215EE9C7D9DC229D2921A40E899EC5F，大家使用这个符号，都不在前面加自己的私钥。也就是说看到7215EE9C7D9DC229D2921A40E899EC5F大家都知道这代表空，大家都用这个代表空。 现在我想向你发送原意为如下的信号：“0是0 1是1 0否1 1否0 ”，希望这有助于你理解其中“是”和“否”的含义。上述引号中，所有字符“0、1、是、否、以及空格”，都转换为哈希值了，我按照上述顺序发送给你。 当你收到这一串哈希值的时候，唯一事先知道的仅有代表空的哈希值，然后只能辨别其他未知含义的哈希值是否相等。代表空的符号形成三个间隔，可能会让你考虑到这串符号是四个部分，然后考察每个部分，发现了第一个和第三个是相同哈希值的情况下，第二个哈希值都是EE452B7B6063A18A3F4C3468C68FE778。而第一个和第三个不同的情况，中间的是95194BCBEBE20754877C5A125CE072FB。由此，我一厢情愿地猜测你可能可以确认这两个分别代表“是”和“否”。更可能的，你的理解可能会有所不同，但相当接近，比方你认为是代表“等于”和“不等于”。你会把我的“是”和“否”两个哈希值，记录下来，并分别备注为“等于”“不等于”。 当你认为理解之后，又有个麻烦事，你如何让我了解到你已经理解。我猜想你会向我发送一个类似结构的句子。但是你不能直接发送我的哈希值给我，根据游戏规则，凡是你发送的符号，也应该是经过哈希变换的。假设你的词汇表中有“等于”“不等于”“A”“B”四个字符，前面加上了你的私钥“yourid：”，则你发送的实际上是变换后的“A等于A B等于B A不等于B B不等于A”这组字符串的哈希值组成的序列。当我看到你这样的反馈，我倾向于认为你理解了我的“是”和“否”的意思，当然我肯定没把握你的“A”“B”会刚巧对应我的“0”“1”。因此我把你的“等于”和“不等于”的两个哈希值，在我这里备注成“是”和“否”。至于你的“A”和“B”我仍是备注为“未知数1”“未知数2”。 现在我们之间就互相有一套词汇表。当你以后再发送“等于”“不等于”这两个哈希值的时候，我就认为我懂得它们的意思。 虽然目前看来我们两者间的相互理解程度简单粗糙没啥实用性，不过至少达成了一点共识，语言刚起源的时候是不是就是这样开始的呢？从基础的符号开始，如果能够继续发展更多的互相认识的符号，是不是就可以发展出越来越复杂的符号直至形成语言？ 另外，我感觉游戏规则的制定中，有一点条件限定过强。就是除了空值这个哈希值是大家默认共知的，我们之间没有其他任何可以共同体验的生活环境来指认符号。（正如两个原始人还可以一起瞅着一个苹果比划，马上就对苹果这个单词互相理解。）这样的设定会让难度增加，不过也不是没有意义。假定一个外星文明只能和我们进行信号交流，如何互相理解，就和游戏中的状况类似了。 这个试验需要多人参与。我建了一个QQ群，779728193 “语言试验”