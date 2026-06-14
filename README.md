# my-releases

mrzhaobh 个人项目公开发布产物的统一仓库。每个项目占一个子目录,互不干扰。

| 项目 | 说明 | 客户端检查更新 |
|---|---|---|
| [`ZBH_FongTV/`](./ZBH_FongTV/) | FongMi 影视 fork,支持 TV 盒子与移动端 | [`ZBH_FongTV/version.json`](./ZBH_FongTV/version.json) |

## 子目录结构约定

```
<项目名>/
├── version.json      客户端读这个比对 versionCode、下载 APK
└── dist/             实际产物(APK 等),稳定命名,每次发版覆盖
```

历史归档不在本仓内,完整带时间戳的版本另存于个人云盘(夸克同步)。
