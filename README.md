# README.md

### 情景导入

##### 举个例子：

本人使用的go-cqhttp+Nonebot2机器人在频繁的异地登录下触发的tx风控机制,无法发送长消息，图片，以及合并转发消息 ，严重着无法发送任何消息(本地显示发送但是对方无法接受到)

##### 解决办法：

- 最原始的办法：暂停 bot业务并使用gocq挂一段时间（看tx心情解除风控），短则1.2天，长则几个月（我的小号被风控了几个月）
- 本人实测可能有用的方法
  - 改密码（一般情况去QQ安全中心改密可以解）
  - 在设置-账号安全-登录设备管理，删除掉所有的已验证设备（注意不要删除"本机"），修改密码，建议使用强密码（除了在本地的bot以外，若在服务器上运行，在操作前务必改变网络环境，将自身IP代理到服务器网络再执行上述操作，以免再次出现异地登陆风控。此方法目前实测十分有效！）
  - 给你的bot开svip？？？，据有人反映有一点点用？？？？
  - 不要使用一些违规业务比如发色图，发xml/json卡片，重复发送相同的消息，大量上传群文件，同时大量艾特成员，有效避免被查才是最佳方案
  - 换个Q号吧，注册一个新号迁移被风控的老号数据然后注销😊

### 你可能遇到的问题：

##### 我的bot不在本地，不会改变网络环境怎么办：

-------如果你是服务器linux用户使用[x-ui](https://github.com/vaxilu/x-ui)部署vmess代理，手机上使用你喜欢的客户端，添加vmess配置即可(这里不再教如何配置)

--------使用windows请自行解决

### Tip:

附上x-ui一键部署代码（安装&升级）

```
bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)
```

### 最后：

祝各位bot开发者在新的一年里，天天被风控[手动滑稽](~~不是~~
