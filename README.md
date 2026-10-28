# bspluginlist

BIMSee 插件列表。

- `pluginlist_win.json` — Windows (win64/x64)
- `pluginlist_linux.json` — Linux (linux64/x64)
- `schema.json` — 列表 JSON Schema

BIMSee 每次打开「插件管理」都会从对应平台的 raw 文件读取：

- Windows: https://raw.githubusercontent.com/bimsee/bspluginlist/main/pluginlist_win.json
- Linux: https://raw.githubusercontent.com/bimsee/bspluginlist/main/pluginlist_linux.json

插件 ZIP 放在 `packages/<platform>/` 下；列表条目的 `download` 指向 raw URL
（也可以填任意稳定 URL，例如 GitHub Releases 资源）。

发布新版本：修改对应平台的 JSON，更新 `version` / `appVersion` / `releaseNotes` /
`download` / `sha256` / `size`，把 ZIP 放进 `packages/<platform>/`，提交 PR。
