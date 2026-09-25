# 麦姬大人的拼豆图纸

拼豆图纸编辑器，包含四叶草、雨衣踩水系列，以及 MARD 221 + 70 标准色卡。

## 在另一台电脑运行

安装 Node.js，克隆本仓库，然后在仓库目录运行：

```sh
node preview-server.cjs
```

打开 http://127.0.0.1:8765/ 。无需安装其他依赖。

## 图纸保存和两台电脑协作

- 图纸源数据是 `public/patterns/library.json`。保存时可选择覆盖当前图纸或另存新图。
- 本地服务会同时更新 `dist/patterns/library.json`，删除也会同步到这两个文件。
- 换电脑编辑前先拉取最新代码；编辑保存后提交并推送。避免两台电脑同时修改图纸库，以免发生冲突。
- 网页代码在 `public/`；发布副本在 `dist/`，修改后同步对应文件。

## 线上版本

Sites 静态发布目录为 `dist`，项目配置为 `.openai/hosting.json`。
线上支持查看、导出和试改；保存到源码、删除图纸需要本地服务。在线试改不会自动同步到 GitHub。
每次先本地确认，再发布到现有 Sites 项目，保持现有访问范围。

## 色卡

`mard-291.json` 为完整 221 + 70 色库，`mard-221.json` 为标准 221 色子集；`standard-palette.js` 供编辑器使用。
色值参考 https://www.pixel-beads.com/zh-tw/mard-bead-color-chart ，特殊材质仅展示近似色。
