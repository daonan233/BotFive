# BotFive

一个基于Mirai-Java框架的群聊机器人，完善中~

### 目前已完成以下内容：<br>

- 对用户的命令进行对应回应：BotFive-1.0.2（恭喜笨比bot55进入智能时代1.x.x）<br>
- 按名字搜索音乐并以xml形式发送：MiraiSongPlugin-2.7-1.2.1<br>
- 生成一些拍拍图等：petpet-5.3<br>
- 群聊大富翁文字版：MonopolyForMirai-0.1.2.mirai2<br>
- 生成5000兆円欲しい!风格图片：5000choyen-1.0.0<br>
- 基于chatGPT的智能问答：mirai-openai-plugin-1.1.0.mirai2<br>
- 基于kimi的ai猫娘回复：BotFiveNew-0.1.0<br>

___

### 具体使用方式：<br>

- 发送 ```#BotFive``` 获取主要功能帮助

___

### 其中用到的Jar包来源有：

1.   <https://github.com/heziblack/MonopolyForMirai>
2.   <https://github.com/Dituon/petpet>
3.   <https://github.com/xszqxszq/5000choyen-mirai>
4.   <https://github.com/cssxsh/mirai-openai-plugin>
5.   <https://github.com/daonan233/kimiChatBot>

### 参考网站：

1.   <https://github.com/mamoe/mirai>
2.   <https://mirai.mamoe.net/>

___

### 具体配置方法：

1. 先将本仓库克隆到本地，打开后删除bots文件夹（里面存储原账号的信息）

2. 然后进入/config/Console/autologin.yml，删除第二段  ***- # 账号, 现只支持 QQ 数字账号***  以下的内容

3. 返回根目录，打开mcl.cmd。等待全部加载完毕出现输入框后，输入

   ```
   login qq账号 qq密码
   ```

4. 如果想要将该账号添加为自动登录，可以输入

   ```
   autologin add qq账号 qq密码
   ```

5. 接下来会出现需要滑动验证的内容，我们以电脑端操作为例（虽然Mirai官方更推荐使用android手机端登陆验证），将最后一段的link后的网址复制到浏览器，f12打开看网页检查，监视网络，进行滑块验证后获取ticket。在mcl窗口提交ticket，即可登录。（当然也可以使用TxCaptchaHelper等工具进行辅助登录，可自行查询）。

![](https://link.jscdn.cn/1drv/aHR0cHM6Ly8xZHJ2Lm1zL3UvcyFBaEJzbFI3bFlkOTVnVTNFc0lQOXJqQjRDdzdPP2U9N1lTcE5x.jpg)

___

### 更新方式：

该上传的版本可能未将mcl升级到最新的2.14.0版本（该版本增加了短信验证登录功能）。如果需要，可以参考以下步骤：

- 打开根目录下的config.json，将原来对应的部分替换为

  ```yml
    "net.mamoe:mirai-console": {
        "channel": "maven-stable",
        "version": "2.13.3",
        "type": "libs",
        "versionLocked": false
      },
  ```

- 打开cmd.exe，进入本仓库根目录在本地的位置，输入

  ```
  mcl -u
  ```

- 等待更新即可。这也是一种打开mcl的方式。

---

- 2025/2/1更新，新编写了基于kimi-api的ai聊天插件BotFiveNew，默认预设为猫娘，可以使用#ChatFive-catgirl来启动，#shutdown来关闭，使用的时候需要@机器人+文本使用。

---

- 2024/10/22更新，已找到新的插件trpgbot用于防止出现code=45的报错，已删除之前的fix-protocal插件避免冲突。同时将pet升级到6.2版本，删除了原有的5.2版本。

---

- 2023/9/11更新，桃子的api-key也过期了，智能55bot暂时下线，直到找到下一个可用的api-key

___

- 2023/4/15更新，特此感谢 桃子 为我提供了OpenAI api-key，使得bot的chatGPT问答能够顺利进行。
- 当前库内的api-key已经过期。

___

- 2023/3/29更新，加入fix-protocol插件之后，在yml手动setConfig protocol MACOS，成功修复，本项目继续更新~****

___

- 2023/3/14更新，在过去的一周半内，目前该项目启动时在电脑上已经报出code=45/235/237三种错误，尝试过更新到mcl 2.14.0、删除device.json、删除bots根目录、保持手机登录等多种方法，在未知有新错误的情况下，应该是作者的四个qq号都被风控了

- 因此本项目暂时不再更新，后续更新时间未知。









