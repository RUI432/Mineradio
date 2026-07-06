# Mineradio

![Mineradio 暗场启动页](./docs/assets/readme/cinema-beat-smoke.png)

Mineradio 是一款桌面沉浸式音乐播放器，支持 Windows 和 macOS，把天气电台、搜索播放、歌词舞台、粒子视觉和 3D 歌单架组合成一个更接近现场感的私人音乐空间。

## 立即下载

> Windows 国内用户可以优先使用蓝奏云下载；macOS 用户请从 GitHub Release 下载 `.dmg` 安装包。

| 系统 | 下载入口 | 推荐人群 | 链接 |
| --- | --- | --- | --- |
| Windows | 蓝奏云满速下载 | 国内 Windows 用户优先 | [下载 Mineradio 1.1.1 Windows 安装包](https://xxhuber.lanzout.com/s/Mineradio) |
| Windows | GitHub Release 备用 | 能稳定访问 GitHub 的 Windows 用户 | [Mineradio-1.1.1-Setup.exe](https://github.com/RUI432/Mineradio/releases/download/v1.1.1/Mineradio-1.1.1-Setup.exe) |
| macOS Apple Silicon | GitHub Release | M1/M2/M3/M4 Mac 用户 | [Mineradio-1.1.1-arm64.dmg](https://github.com/RUI432/Mineradio/releases/download/v1.1.1/Mineradio-1.1.1-arm64.dmg) |
| macOS Intel | 暂未提供 | Intel Mac 用户 | 可自行执行 `npm run build:mac` 生成 x64 安装包 |

Windows 安装时只需要下载并运行 `Mineradio-1.1.1-Setup.exe`。macOS Apple Silicon 用户下载并打开 `Mineradio-1.1.1-arm64.dmg`，把 `Mineradio.app` 拖进 `Applications`。不要下载 `Source code`、`.blockmap`、`latest.yml`，也不要把 `win-unpacked` / `mac-arm64` 当成正式安装包。

## 下载或安装被拦截怎么办

小众 Electron 桌面软件、未签名安装包有时会被浏览器、Windows Defender、SmartScreen 或 macOS Gatekeeper 提示风险。请先确认安装包来自上面的蓝奏云或 GitHub Release 官方入口，Windows 文件名是 `Mineradio-1.1.1-Setup.exe`，macOS 文件名是 `Mineradio-1.1.1-arm64.dmg`。

1. 浏览器下载栏提示风险时，打开下载列表，点这条下载右侧的 `...` 三个点，选择 `保留` / `仍要保留` / `显示更多` 后继续保留。
2. Windows SmartScreen 弹出蓝色拦截窗口时，点 `更多信息`，再点 `仍要运行`。
3. macOS 提示无法验证开发者时，可以在 Finder 里右键 `Mineradio.app` 选择 `打开`，或到 `系统设置 > 隐私与安全性` 允许打开。
4. 如果杀毒软件明确显示木马、高危或已经隔离，不要强行运行；删除该文件后重新从蓝奏云或 GitHub Release 下载，仍然异常请带截图反馈给作者。

## 作者支持

如果 Mineradio 陪你多听了一首歌，也欢迎请作者一杯咖啡。

[查看完整支持页](./docs/SUPPORT.md)

![Mineradio 作者支持渠道](./docs/assets/support/mineradio-author-support-poster.png)

1.1.1 的核心目标是把 Mineradio 重新整理成一份可公开下载的纯净安装版：默认视觉参数来自内置「默认测试」用户存档，首次启动就进入统一的视觉手感；3D 歌单架、歌词层级、用户存档和后台性能策略都在同一轮里收口。

## 当前版本

当前版本：`1.1.1`

状态：1.1.1 纯净安装发布版。

> 安全提示：`v1.0.10` 及更早旧安装包不再建议继续安装或传播，请先隔离旧安装包。请使用本页提供的 `Mineradio-1.1.1-Setup.exe` 或 `Mineradio-1.1.1-arm64.dmg` 进行纯净安装。

## 核心特性

- Open-Meteo 天气电台，根据当前位置、城市和天气 mood 生成更合适的播放队列
- 首页包含天气电台、每日推荐、私人电台、继续听、听歌画像和我的歌单入口
- Wallpaper 银河首页背景，未播放状态保持干净的星河氛围
- 播放后切换到 Emily / 默认播放态视觉，歌词舞台与粒子舞台同步工作
- 基于节奏的电影镜头视觉系统
- 面向长播客和 DJ 曲目的专属视觉模式
- 歌词舞台、自定义歌词、歌词位置与视觉控制
- 自定义专辑封面上传与裁剪
- 右键唤起 3D 歌单架，支持歌单队列浏览
- 网易云音乐账号、搜索、歌单、播客等体验接入
- QQ 音乐搜索、登录态与音源补充接入
- GitHub Releases 更新检测与下载入口
- 首次启动内置「默认测试」视觉用户存档，软件内默认视觉参数与该存档一致

## 使用说明

Windows 用户可以在 GitHub Releases 中下载安装包。

正式分发以 `Mineradio-1.1.1-Setup.exe` 为准，不建议直接下载 `win-unpacked` 目录作为正式分发包。安装包会创建桌面快捷方式；直接运行打包版 `Mineradio.exe` 时，应用也会在首次启动时补创建桌面快捷方式。

macOS 用户可以下载对应架构的 `Mineradio-版本-arm64.dmg` 或 `Mineradio-版本-x64.dmg`。Apple Silicon 机型优先使用 `arm64`，Intel Mac 使用 `x64`。未签名构建首次打开时如果被系统拦截，可以在 Finder 中右键应用选择“打开”，或到“系统设置 > 隐私与安全性”允许打开。

已经安装过旧版本的用户，建议卸载旧版本、隔离旧安装包后，再使用 `v1.1.1` 安装包纯净安装。

## 开发运行

```bash
npm install
npm start
npm run build:win
npm run build:mac
```

如果本机使用 pnpm，也可以执行 `pnpm install`、`pnpm start`、`pnpm run build:mac`。

桌面版入口由 Electron 主进程加载本地服务。`npm run build:win` 会生成 Windows NSIS 安装包，`npm run build:mac` 会生成 macOS x64/arm64 DMG/ZIP 安装包，产物位于 `dist/`。

## 更新机制

Mineradio 会请求 GitHub Releases latest 检测新版本。远端版本高于本地版本时，应用内更新入口会展示 Release 内容、下载安装包到本机用户数据目录，并通过系统打开安装包。

本地验证更新链路时，可以通过 `MINERADIO_UPDATE_MANIFEST` 指向一个本地 manifest JSON 或 HTTP 地址来模拟线上 Release。

## 第三方音乐平台说明

Mineradio 不是网易云音乐、QQ 音乐或腾讯音乐娱乐集团的官方客户端，也不隶属于任何音乐平台。

项目中的第三方平台接入仅用于个人学习、本地客户端体验和用户自有账号的播放辅助。请遵守对应平台的用户协议、版权规则和会员权益规则。项目不会提供绕过付费、绕过会员、破解音质或重新分发音乐内容的能力。

## 用户数据与隐私

登录 Cookie、搜索历史、自定义封面、自定义歌词、节奏分析缓存等数据只应保存在本机用户数据目录或浏览器本地存储中，不应提交到仓库。

更多说明见 [PRIVACY.md](./PRIVACY.md)。

## 致谢

Mineradio 由 XxHuberrr 主要设计与打造。emily 作为早期视觉底层想法与 `emily` 视觉预设改进方向的共创者和灵感来源之一，特此感谢。

同时感谢小天才e宝、应春日、锋将军、軌跡、林中、骊、风痕、花椰菜🥦在早期体验、测试反馈和发布准备中的帮助。

## 版权与授权

Copyright (C) 2026 XxHuberrr.

本项目采用 GPL-3.0 授权。详见 [LICENSE](./LICENSE)。

MR Logo、Mineradio 名称、界面视觉设计与原创视觉表达归作者所有；第三方依赖和第三方服务分别遵循其各自授权与服务条款。
