# @arkts/language-server

## 1.1.6

### Patch Changes

- 9fdbf59: feat: 抽象资源补全为一个 namespace，并添加 module.json5 文件路径补全和跳转、引用表达式错误诊断
- Updated dependencies [2fc2eb9]
- Updated dependencies [9fdbf59]
  - @arkts/language-service@1.1.4

## 1.1.5

### Patch Changes

- Updated dependencies [1f5690f]
  - @arkts/language-service@1.1.3

## 1.1.4

### Patch Changes

- f7e47c6: 添加媒体文件夹、profile 文件夹等相关跳转警告 (#167)
- Updated dependencies [f7e47c6]
  - @arkts/language-service@1.1.2

## 1.1.3

### Patch Changes

- a69a6d3: perf: 移除`chokidar`监听器，改用 vscode 自带的 FileWatcher (e8ad061898edba6df7fb61be1557586ded9073f4)
- c401902: feat: 添加`@arkts/language-service`包，将公共服务抽离进该包 (aba71f4a7be11623dbeb07732d80ae1db1089af8) (#157)
- dfda7e8: feat: 添加 json 基础跳转源码检查 (48b47a9ce31fde88aaacd50adb95a8bd631c89a8)
- 828387a: feat: 添加媒体文件夹检查，重构多个 project detector 方法 (442c94f81659c2861d61dd103258f838e6073762)
- bfaf59c: fix(language-server): 添加`ets/onDidChangeTextDocument`事件，修复`onDidChangeTextDocument`钩子不能在 lsp 启动时监听导致 volar 提示服务冲突的问题

  volar 内部貌似用了 onDidChangeTextDocument 钩子，该钩子似乎只运行在 Initialize 时监听一次，不允许多次监听，所以应该实现一个自定义的事件来解决监听 TextDocuments 的问题。目前已经添加了一个`ets/onDidChangeTextDocument`事件用于监听，vscode 侧已经添加了相应的监听逻辑。

- e6089b0: feat: 重构使用 @arkts/project-detector 查找资源 (#164)
- fc4c7b8: feat: 迁移 resource diagnostics 和 definition 到重构后的新服务，并添加 json 为 documentSelector (8740d298767070ca5c0a7af8ff662817f7fe3c6e)
- 19a8a75: 1c8ea58: feat: 添加 string/color 等 element file 在 module.json5 中的跳转功能 (1c8ea586d42547ed98c8b29851af5504d2e02041)
- 78432f5: feat: 更新`ArkTSLinter`的行为
- Updated dependencies [a69a6d3]
- Updated dependencies [702f67a]
- Updated dependencies [c401902]
- Updated dependencies [df97ae7]
- Updated dependencies [dfda7e8]
- Updated dependencies [828387a]
- Updated dependencies [e6089b0]
- Updated dependencies [8a29c5a]
- Updated dependencies [fc4c7b8]
- Updated dependencies [19a8a75]
  - @arkts/language-service@1.1.1

## 1.1.2

### Patch Changes

- d5f73b0: fix: rename the current services
- 6f22ab2: refactor: 删除旧版格式化逻辑，使用`language-service`替代并删除用于格式化的 languageService，大幅提高性能
- 387cf2e: fix: prepare add new resource watcher
- 9737adc: fix: 替换不安全的`new Function()`, 改为 createRequire 加载 SDK 中的`sysResource.js`

## 1.1.1

### Patch Changes

- be25ace: feat: 支持$r()资源引用补全 (#6) 感谢 github @frezs 的贡献 🎉!

## 1.1.0

### Minor Changes

- e8fcbef: feat: 添加`$this`语法支持 (#122)

## 1.0.6

### Patch Changes

- 915e262: ci: release

## 1.0.5

### Patch Changes

- 66c21bd: chore: update deps

## 1.0.4

### Patch Changes

- df60843: feat: 移除 hilog 相关逻辑等待后续实现；还原并增强猜测 SDK 版本功能

## 1.0.3

### Patch Changes

- b9a93ed: feat: 添加\`hms\`SDK 支持 (#35)

## 1.0.2

### Patch Changes

- [`9c1b704`](https://github.com/Groupguanfang/arkTS/commit/9c1b7048a8b38bd0d129b2c850307e3d3c905613) Thanks [@Groupguanfang](https://github.com/Groupguanfang)! - fix: API10 与最新版 ohos-typescript 兼容性问题

## 1.0.1

### Patch Changes

- [`19428dc`](https://github.com/Groupguanfang/arkTS/commit/19428dcdb6f8e27914067ea48a53ce644c26f7e6) Thanks [@Groupguanfang](https://github.com/Groupguanfang)! - feat: 添加多模块支持
