# CDEScript 添加新插件 — AI 提示词

将以下内容发给 AI，填写源仓库信息即可：

---

请将以下源仓库的插件添加到 CDEScript 仓库。

## 源仓库信息
- GitHub 地址：[填写]
- 本地路径（如有）：[填写]
- 需要添加的插件 internalName 列表：[填写]

## CDEScript 仓库信息
- 本地路径：D:\UserData\Documents\CloudStream\CDEScript
- GitHub：https://github.com/GD2021/CDEScript

## 操作流程
1. 探索源仓库结构 — 确认是源码仓库还是仅 builds 仓库
2. 验证 .cs3 文件是否存在（检查 builds 分支）
3. 从源仓库的 plugins.json 提取完整元数据
4. 更新 CDEScript 的 plugins.json（URL 直接引用源仓库 builds 分支，不本地拷贝 .cs3）
5. 更新 README.md 的插件表格
6. 更新 .github/workflows/sync.yml 的 SOURCES 字典（添加源 URL 和 internalName 列表）
7. 提交并推送

## 注意事项
- 作者保持源仓库原始作者，不加 "GD2021"
- 如果源仓库无 description，可以自定义
- 保留源仓库 plugins.json 中的 fileHash（如有）
- URL 格式统一为 https://raw.githubusercontent.com/author/repo/builds/PluginName.cs3
- 不要本地拷贝 .cs3 文件，全部引用源仓库 URL
