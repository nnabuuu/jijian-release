# 即见(jijian)工具发布

即见品牌下各本地工具的发布总仓。源码在内部 monorepo;这里放各产品的 **GitHub Release**(tarball)+ 安装入口。

## jijian-bridge — 本地同步桥
把**任意**即见 solution 的 workspace 同步进你自己的 Claude Code / Codex 并双向回写(solution-agnostic;
live-lesson 只是一个配置目标)。

**安装(Node ≥ 20):**
```bash
npm i -g https://github.com/nnabuuu/jijian-release/releases/download/jijian-bridge-v0.2.4/kedge-agentic-jijian-bridge-0.2.4.tgz
jijian --version && jijian install && jijian doctor
```
或:`gh release download jijian-bridge-v0.2.4 -R nnabuuu/jijian-release -p '*.tgz' && npm i -g ./kedge-agentic-jijian-bridge-0.2.4.tgz`

> 装完 `jijian: command not found`?**asdf** 用户需 `asdf reshim nodejs`(对所有全局 npm 工具都这样);**nvm** 装到当前激活的 node 版本;**普通 node** 直接可用。验证 `jijian --version`。

上手:`jijian install`(装常驻同步桥 launchd/systemd)→ `jijian config` 配 target → `jijian login`(登录后常驻桥自动挂上)
→ 之后在即见网页右上角点「连接」即可,**零命令**。兼容性见 Release 里的 `COMPATIBILITY.md`(也在 tarball 内)。

<!-- 未来的即见工具作为新 section + 新 Release tag 追加于此 -->
