---
title: alacritty与Zellij的使用
date: 2024-10-10T08:54:34.594Z
---

起初是在windows下使用alacritty，速度快，体验较好，发现没有多窗口功能，
在网上搜索了下，有使用tmux的，太麻烦，不是很适合自己的使用场景，看到了Zellij这个工具，Zellij没有windows版，一个偶然的机会，我在开发机器linux上装了Zellij，通过alacritty ssh连接linux进行开发，直接使用zellij的功能，达到满意的效果。


```shel
cat ~/.bashrc
eval "$(zellij setup --generate-auto-start bash)"

```

总结下我的需求，或者说是开发方式，windows+ ubuntu虚拟机，win下vscode ssh远程ubuntu编写代码，win下使用ssh客户端连接Ubuntu进行远程，主要是执行一些编译和系统配置。
![2024-10-10_165044.png](https://github.com/wuqingwei/tinymind-blog/blob/main/assets/images/2024-10-10/1728550260426.png?raw=true)