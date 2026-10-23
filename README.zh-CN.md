# Trip Fieldnotes

[English](README.md) | **简体中文**

[Fieldnotes](https://github.com/Tangerineeew/fieldnotes) 在 [TREK](https://github.com/mauriceboe/TREK) 旅行中的那一半。它为每次旅行添加 **Trip Fieldnotes** 标签页：全体同行者在这里阅读分享给这次旅行的笔记，把它们整理进旅行文件夹，再把有用的部分放进行程。

## 功能介绍

- **分享给旅行的内容集中在一处。** 实时引用始终显示原笔记的最新版本；快照显示加入时冻结的版本，并带有自己的图片副本，即使原文被删除或作者退出旅行，也依然可以阅读。
- **旅行文件夹。** 可以把旅行中的笔记归入「抵达」「第一天」等文件夹，与每位作者在自己图书馆里如何归档互不影响。
- **从旅行中新建笔记。** 「为此旅行新建笔记」会打开 Fieldnotes 编辑器；保存时，一步完成在你的图书馆中保留私有原文并把它关联到这次旅行。
- **放进日程。** 可以把任意笔记中 500 字以内的摘录，作为普通的 TREK 日程笔记复制到旅行中的某一天，原文不会被改动。
- **尊重旅行角色。** 旅行成员都可以阅读；只有有权编辑这次旅行的人，才能添加、移除或整理笔记。
- **十四种语言，** 跟随 TREK 的语言设置，阿拉伯语支持从右到左排版。

## 截图

![在旅行的 Fieldnotes 标签页中打开一条实时引用](./docs/screenshot.zh-CN.png)

## 权限说明

Trip Fieldnotes 自身不申请任何权限，清单中的权限列表为空。它展示或修改的所有内容，都通过 Fieldnotes 插件导出的 `trip` 函数完成，而 TREK 会以当前登录用户的身份运行这个函数。因此它只能读取你所在的旅行，也只能修改你有权编辑的旅行。Fieldnotes 本身需要的权限，请参阅[它的说明文档](https://github.com/Tangerineeew/fieldnotes/blob/main/README.zh-CN.md#权限说明)。

## 安装与设置

1. 先安装并启用 [Fieldnotes](https://github.com/Tangerineeew/fieldnotes)。Trip Fieldnotes 将它声明为依赖，缺少它就无法运行。
2. 在 TREK 中打开 **管理后台 → 插件**，安装 **Trip Fieldnotes** 并启用。上传后的插件默认处于停用状态。
3. 打开任意一次旅行，选择 **Trip Fieldnotes** 标签页。可以在 Fieldnotes 图书馆中通过「带入旅行」分享笔记，也可以在这里用「为此旅行新建笔记」直接创建。

卸载 Trip Fieldnotes 只会移除这个标签页。笔记、旅行关联和快照都属于 Fieldnotes，会继续保留。

## 源码

本仓库存放的是构建好的插件。它小巧的服务端入口是 `server/index.js`；界面与 Fieldnotes 使用同一套前端，两者都由 Fieldnotes 仓库的 [`source/`](https://github.com/Tangerineeew/fieldnotes/tree/main/source) 目录构建。

## 许可证

[MIT](./LICENSE)
