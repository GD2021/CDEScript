## 添加新插件清单

要添加新的源仓库插件，请提供以下信息：

### 1. 源仓库信息
- [ ] 源仓库 GitHub 地址（如 `https://github.com/author/repo`）
- [ ] 本地源仓库路径（如有，如 `D:\xxx\repo-master`）
- [ ] 源仓库的 `plugins.json` URL（通常在 builds 分支）
  ```
  https://raw.githubusercontent.com/author/repo/builds/plugins.json
  ```

### 2. 插件列表
- [ ] 插件 internalName 列表（如 `["Wcoflix", "Movix"]`）
- [ ] 插件显示名称（如 `"Wcoflix"`，可与 internalName 不同）
- [ ] 插件类型（如 `Movie`, `TvSeries`, `Anime`, `AsianDrama`, `Cartoon`, `AnimeMovie` 等）
- [ ] 插件语言代码（如 `en`, `fr`, `tr`, `mx`, `es`, `it`, `id`, `ar` 等）
- [ ] 插件作者（源仓库的原始作者名）
- [ ] 插件描述（可选，如源仓库无描述可自定义）

### 3. 验证要求
- [ ] 确认 `.cs3` 文件存在（验证 URL 返回 200）
- [ ] 确认 `plugins.json` 中存在对应条目
- [ ] 确认源仓库有 CI 自动构建（有 builds 分支或 GitHub Actions）

### 4. 输出文件（自动更新或手动修改）
- [ ] `plugins.json` — 添加插件条目，URL 直接引用源仓库
- [ ] `README.md` — 在插件表格中添加一行
- [ ] `.github/workflows/sync.yml` — 在 `SOURCES` 字典中添加源 URL 和 internalName 列表
