# 快速配置并登录CVM实例

如果您是首次购买和使用云服务器CVM的个人用户，腾讯云推荐您按照本文介绍的流程快速配置、购买和连接CVM实例。



![image-20190225171637625](/Users/reneewang/Library/Application Support/typora-user-images/image-20190225171637625.png)



## 1. 注册账号与选型

### 注册腾讯云账号

新用户需在腾讯云官网进行 [注册](https://cloud.tencent.com/register?s_url=https%3A%2F%2Fcloud.tencent.com%2F)。注册指引可参考 [如何注册腾讯云](https://cloud.tencent.com/doc/product/378/9603) 。

### 确定云服务器所在地域及可用区

地域选择原则：

- 靠近用户原则。
  请根据您的用户所在地理位置选择云服务器地域。云服务器越靠近访问客户，越能获得较小的访问时延和较高的访问速度。

- 内网通信同地域原则。

  - 相同地域下的云服务器可以通过内网相互通信（内网通信，免费）。

  - 不同地域之间的云服务器不能通过内网互相通信（通信需经过公网，收费）。

    需要多个云服务器**内网通信的用户须选择相同云服务器地域**。

### 确定云服务器配置方案

对于个人用户，腾讯云推荐您使用**入门配置**。

- **入门配置**：适用于起步阶段的个人网站。例如个人博客等小型网站。

或者根据需求您可以选择：

- **基础配置**：适合有一定访问量的网站或应用。例如较大型企业官网、小型电商网站。
- **普及配置**：适合常使用云计算等一定计算量的需求。例如门户网站、SaaS 软件、小型 App 。
- **专业配置**：适用于并发要求较高的应用及适合对云服务器网络及计算性能有一定要求的应用场景。例如大型门户、电商网站、游戏 App 。

若推荐的配置不能满足您的需求，您可以在[更多机型](https://buy.cloud.tencent.com/cvm?tabIndex=1)中根据实际需要比较各配置方案。当然您也可以在购买云服务器之后，根据您的需求随时进行 [配置升级](https://cloud.tencent.com/doc/product/213/%E8%B0%83%E6%95%B4CVM%E5%AE%9E%E4%BE%8B%E9%85%8D%E7%BD%AE#1.-%E9%85%8D%E7%BD%AE%E5%8D%87%E7%BA%A7) 或  [配置降级](https://cloud.tencent.com/doc/product/213/%E8%B0%83%E6%95%B4CVM%E5%AE%9E%E4%BE%8B%E9%85%8D%E7%BD%AE#2.-%E9%85%8D%E7%BD%AE%E9%99%8D%E7%BA%A7) 。

### 确定付费方式（按量付费只支持预付费？）

腾讯云提供**包年包月**和**按量付费**两种付费模式。具体详情可参见 [计费模式说明](https://cloud.tencent.com/doc/product/213/2180) 。
若您选择按量付费，则需先完成 [实名认证](https://console.cloud.tencent.com/developer/infomation) 。



## 2. 快速配置及购买CVM实例

腾讯云提供**快速配置**和**自定义配置**两种方式。本部分以快速配置为例说明，若快速配置不能满足您的需求，您可参考 [自定义配置 Linux 云服务器](https://cloud.tencent.com/doc/product/213/10517) 文档进行配置。

补截图@@@ 在截图说明。

完成云服务器的购买和创建后，云服务器的实例名称、公网 IP 地址、内网 IP 地址、登录名、初始登录密码等信息都将以 [站内信](https://console.cloud.tencent.com/message) 的方式发送到账户上。



## 3. 登录及连接CVM实例

配置及购买CVM实例后，您可以通过多种方式连接并登录CVM实例，腾讯云推荐您使用WebShell登录及连接CVM实例**。本文介绍在CVM WebShell快速连接并登录实例。**

### 使用WebShell登录CVM实例。

#### 适用本地操作系统：

Window，Linux或者Mac OS

#### 限制条件：

CVM实例存在公网IP

#### 鉴权方式：

密码 或 密钥。（密钥是否仅仅适用于Linux系统？？快速配置都是自动生成密码）

#### 操作方式：

1. 查找[腾讯云控制台](https://console.cloud.tencent.com/)，点击【实例】，选择您需要登录的云服务器并点击【登录】。——补一个截图
2. 在登录页面选择密码或者密钥的方式登录。
3. 如果登录成功，WebShell界面会出现Socket established提示。

如果您希望通过其他方式，比如远程登录软件或者SSH方式登录CVM实例，可以参考以下链接。

- 连接及登录Linux实例。
- 连接及登录Windows实例。



## 格式化与数据盘分区

如果您在创建CVM实例时购买了数据盘，初次连接CVM实例后您需要格式化数据盘后才能正常使用。

对于Linux实例中创建的大于2TB的硬盘，请 [使用GPT分区表分区并格式化](https://cloud.tencent.com/doc/product/213/2043) 。

==
警告(内容是否正确？)

- 磁盘分区和格式化是高风险行为，请慎重操作。本文档描述如何处理一个新买的数据盘，如果您的数据盘上有数据，**请务必对数据盘创建快照以避免可能的数据丢失**。 
- 云服务器 ECS 仅支持对 **数据盘** 进行分区，而不支持对 **系统盘** 进行分区。如果您强行使用第三方工具对系统盘进行分区操作，可能引发未知风险，如系统崩溃、数据丢失等。

==