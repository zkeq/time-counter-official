## 网站在线人数统计 [官网]

![time-counter](https://socialify.git.ci/soxft/time-counter/image?description=1&font=Bitter&language=1&name=1&owner=1&stargazers=1&theme=Dark)

> 本项目是一个开箱即用的站点在线人数统计服务，同时开源支持私有化部署。

> 项目官网：https://time-counter.icodeq.com

> 项目仓库：https://github.com/soxft/time-counter

### 前言：

1. 在维护一个 [学习站点](https://tuostudy.com) 时，为了营造一种学习的氛围，开始猜想 能不能写一个实时在线人数 API 呢？
2. 这是从 Plausible 站点中得到的一个思路，加以扩展 即 想法变成 能否得到一个 `记录每人在线时间` 的 API 呢？
3. 🤔 此项目的 代码/架构 实现完全由 @soxft 开发，得到可以实现的肯定回答后，本项目上线于 2022.6.4 并投入使用
4. 在 9 月份，因为开学等原因 数据库丢失 下线 3 个月后，11月项目再次启动 稳定运行至今，处理 API 请求 已达近数十亿次
5. 2023.2.5 元宵节，本项目由单个站点扩展为 Room 机制，对外开放使用，同时开放源码支持独立部署：[soxft/time-counter](https://github.com/soxft/time-counter)

### 使用：

1. 选择一个独立的 `Room ID` (10字符以内)
1. 选择 `Iframe` 方式使用 or `js` 方式使用
1. Enjoy！

<!-- ### Room ID：

<label for="room-input">ROOMS:&emsp;</label><input type="text" id="room-input" />

|   Key   |   Value   |
| ---- | ---- |
|   online user   |   <span style="color: red;" id="online_user"></span>   |
|   my online time   |  <span style="color: red;" id="online_me"></span>    |
|   total online time   |   <span style="color: red;" id="online_total"></span>   | -->

### 用法：

1. Iframe 引入

```html
<center><iframe frameborder=0  height=50px marginwidth=0 scrolling=no src="https://time-counter.onmicrosoft.cn/room/{Room ID}"></iframe></center>
```

2. JS 引入

```html
<script src="https://time-counter.onmicrosoft.cn/counter.js" async="" id="online-counter" interval="240" api="https://time-counter.onmicrosoft.cn/counter" room="{Room ID}"></script>

本站当前在线人数 <span style="color: red;" id="online_user"></span> 人

你的在线总时间: <span style="color: red;" id="online_me"></span>

全站在线总时间:  <span style="color: red;" id="online_total"></span>
```

<!-- 
<center><iframe frameborder=0  height=50px marginwidth=0 scrolling=no src="https://time-counter.onmicrosoft.cn/room/info"></iframe></center> -->


 > <center>Powered by: 🚀 Gin + Redis ✨</center>
