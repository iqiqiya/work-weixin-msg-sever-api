# work-weixin-msg-sever-api

使用企业微信给自己微信发送消息的API，基于vercel或腾讯云函数（可二选一）

## 与server酱对比

|       | server酱 Turbo版      | 腾讯云部署          | 调用vercel接口         |
|-------|---------------------|----------------|--------------------|
| 搭建时间  | 一般                  | 较长             | 较短，无需经过第三方网页       |
| 服务价格  | 8元/月                | 根据腾讯云函数进行收费    | 免费                 |
| 免费额度  | 5条/天                | 1000GBs/月      | vercel限制，超出限制可自行搭建 |
| 速度    | 信息加入异步推送队列，速度根据环境   | 非常快            | 受限于vercel的速度，较快    |
| 提醒    | 免费版只提醒收到消息，通知栏看不到详情 | 提醒消息全文         | 提醒消息全文             |
| 安全性   | 依据对项目的信任关系          | 开源项目           | 开源项目               |
| 数据隐私  | 推送内容保留1天/收费版7天      | 不会存储信息，无需绑定微信号 | 不会存储信息，无需绑定微信号     |
| 服务稳定性 | 一般                  | 高，腾讯云一般很难挂     | 高，vercel应该不会跑路     |

## 使用教程

[使用腾讯云函数快速部署](https://iqiqiya.com/posts/50818ca6.html)

[使用其他方式部署](https://blog.zhheo.com/p/1e9f35bc.html)

## 发送方式

get

## 参数

| 参数      | 类型  | 必选   | 描述               |
|---------|-----|------|------------------|
| id      | str | true | 企业微信公司id         |
| secert  | str | true | 企业微信应用的应用secert  |
| agentId | int | true | 企业微信应用的应用agentId |
| msg     | str | true | 需要发送的内容          |
