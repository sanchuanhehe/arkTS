# vscode-naily-ets

## 1.1.8

### Patch Changes

- 2fc2eb9: feat(language-service): 添加 module.json5 requestPermissions 部分补全功能
- 9fdbf59: feat: 抽象资源补全为一个 namespace，并添加 module.json5 文件路径补全和跳转、引用表达式错误诊断

## 1.1.7

### Patch Changes

- 1f5690f: feat: 优化资源跳转性能，合并重复代码逻辑

## 1.1.6

### Patch Changes

- f7e47c6: 添加媒体文件夹、profile 文件夹等相关跳转警告 (#167)

## 1.1.5

### Patch Changes

- a69a6d3: perf: 移除`chokidar`监听器，改用 vscode 自带的 FileWatcher (e8ad061898edba6df7fb61be1557586ded9073f4)
- ae09c59: chore: 切换`ohos-typescript`源到`gitcode`
- c401902: feat: 添加`@arkts/language-service`包，将公共服务抽离进该包 (aba71f4a7be11623dbeb07732d80ae1db1089af8) (#157)
- 5c31dd3: feat: 更新中文翻译 (498e7ce6039b265327f65e1fbbd662101f5c88cc)
- dfda7e8: feat: 添加 json 基础跳转源码检查 (48b47a9ce31fde88aaacd50adb95a8bd631c89a8)
- 828387a: feat: 添加媒体文件夹检查，重构多个 project detector 方法 (442c94f81659c2861d61dd103258f838e6073762)
- bfaf59c: fix(language-server): 添加`ets/onDidChangeTextDocument`事件，修复`onDidChangeTextDocument`钩子不能在 lsp 启动时监听导致 volar 提示服务冲突的问题

  volar 内部貌似用了 onDidChangeTextDocument 钩子，该钩子似乎只运行在 Initialize 时监听一次，不允许多次监听，所以应该实现一个自定义的事件来解决监听 TextDocuments 的问题。目前已经添加了一个`ets/onDidChangeTextDocument`事件用于监听，vscode 侧已经添加了相应的监听逻辑。

- e6089b0: feat: 重构使用 @arkts/project-detector 查找资源 (#164)
- fc4c7b8: feat: 迁移 resource diagnostics 和 definition 到重构后的新服务，并添加 json 为 documentSelector (8740d298767070ca5c0a7af8ff662817f7fe3c6e)
- 19a8a75: 1c8ea58: feat: 添加 string/color 等 element file 在 module.json5 中的跳转功能 (1c8ea586d42547ed98c8b29851af5504d2e02041)
- 78432f5: feat: 更新`ArkTSLinter`的行为

## 1.1.4

### Patch Changes

- 6f22ab2: refactor: 删除旧版格式化逻辑，使用`language-service`替代并删除用于格式化的 languageService，大幅提高性能
- 4b92a91: chore: 移除位于 vscode 插件内部的资源自动补全机制
- 9737adc: fix: 替换不安全的`new Function()`, 改为 createRequire 加载 SDK 中的`sysResource.js`

## 1.1.3

### Patch Changes

- d8eaa76: fix: update galleryBanner theme color
- be25ace: feat: 支持$r()资源引用补全 (#6) 感谢 github @frezs 的贡献 🎉!

## 1.1.2

### Patch Changes

- b0826c9: feat: add galleryBanner settings
- a73646f: fix: update tsdown.config.ts (github #134)

## 1.1.1

### Patch Changes

- 7c47b93: Fixes issue #130 by correcting the argument order in affected functions, ensuring that parameters are passed in the expected sequence. This resolves errors related to incorrect argument handling.

## 1.1.0

### Minor Changes

- e8fcbef: feat: 添加`$this`语法支持 (#122)

## 1.0.28

### Patch Changes

- 00db764: fix: update engines.vscode to ^1.22.0

## 1.0.27

### Patch Changes

- 0926e57: fix: add check to prevent duplicate Reflect fix application (#112)

## 1.0.26

### Patch Changes

- 915e262: ci: release

## 1.0.25

### Patch Changes

- abf2a30: feat: update README
- 66c21bd: chore: update deps

## 1.0.24

### Patch Changes

- df60843: feat: 移除 hilog 相关逻辑等待后续实现；还原并增强猜测 SDK 版本功能

## 1.0.23

### Patch Changes

- b9a93ed: feat: 添加\`hms\`SDK 支持 (#35)

## 1.0.22

### Patch Changes

- [#79](https://github.com/Groupguanfang/arkTS/pull/79) [`9ba4308`](https://github.com/Groupguanfang/arkTS/commit/9ba43080331108778424e7a5bc94bec3477baa84) Thanks [@github-actions](https://github.com/apps/github-actions)! - fix: compiled webview

## 1.0.21

### Patch Changes

- [#78](https://github.com/Groupguanfang/arkTS/pull/78) [`9af013a`](https://github.com/Groupguanfang/arkTS/commit/9af013abf63638fb27ed9fcb88cc89a014360334) Thanks [@github-actions](https://github.com/apps/github-actions)! - feat: update useCompiledWebview hook & deps

- [#78](https://github.com/Groupguanfang/arkTS/pull/78) [`f421410`](https://github.com/Groupguanfang/arkTS/commit/f4214104fe92ce5aab0d52741a4fae36d01bdde3) Thanks [@github-actions](https://github.com/apps/github-actions)! - feat: update module.schema.json

- [#78](https://github.com/Groupguanfang/arkTS/pull/78) [`d251b2d`](https://github.com/Groupguanfang/arkTS/commit/d251b2d31fc15038240890eb75bc141912e59488) Thanks [@github-actions](https://github.com/apps/github-actions)! - feat: test hilog & using env variable to pass the extension configuration to typescript plugin

## 1.0.20

### Patch Changes

- [`c1bb990`](https://github.com/Groupguanfang/arkTS/commit/c1bb990f0b0f8e52296351da99777a7075303dc4) Thanks [@Groupguanfang](https://github.com/Groupguanfang)! - feat: add debounce when restart ETS server

## 1.0.19

### Patch Changes

- [`f650268`](https://github.com/Groupguanfang/arkTS/commit/f650268cbad8ca60873f9fbb8cf3d20e48873739) Thanks [@Groupguanfang](https://github.com/Groupguanfang)! - fix: windows 下路径问题

## 1.0.18

### Patch Changes

- [`84bb0a8`](https://github.com/Groupguanfang/arkTS/commit/84bb0a8d7ff284c9be77e7957d035c5b97abaf7f) Thanks [@Groupguanfang](https://github.com/Groupguanfang)! - fix: json5 高亮, watcher

## 1.0.17

### Patch Changes

- [`19428dc`](https://github.com/Groupguanfang/arkTS/commit/19428dcdb6f8e27914067ea48a53ce644c26f7e6) Thanks [@Groupguanfang](https://github.com/Groupguanfang)! - feat: 添加多模块支持

## 0.1.22

### Patch Changes

- 29de400: feat: 添加 lincode jsdoc 以方面跳转到组件源码

## 0.1.21

### Patch Changes

- 1604e2a: fix: `static`上下文不一致 (#42)

## 0.1.20

### Patch Changes

- ec55308: fix: 上下文\`this\`不能赋值给 struct reference (#41)

## 0.1.19

### Patch Changes

- 82087f9: feat: add $this support

## 0.1.18

### Patch Changes

- b878c07: 修复 struct reference 与.d.ets 内出现装饰器时报错

## 0.1.7

### Patch Changes

- 37a24d8: feat: release

## 0.1.6

### Patch Changes

- feat: update version
