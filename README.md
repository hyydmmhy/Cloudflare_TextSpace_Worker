# Cloudflare Text Disk

基于 Cloudflare Workers + D1 + KV 的轻量级纯文本云盘。树形目录、文件分享、多级缓存，零服务器成本。

## 部署

1. Fork 本仓库
2. Cloudflare 控制台 → Workers & Pages → 连接 GitHub 仓库
3. 在项目 **Settings** 中配置：
   - **Environment Variables**：添加 `ADMIN_UUID`（管理员密码）
   - **Bindings**：D1 数据库绑定 `DB`，KV 命名空间绑定 `SHARE_KV`

之后每次 push 自动部署，`wrangler.toml` 已包含绑定配置。

## 使用

访问 `https://<your-domain>/admin`，输入 `ADMIN_UUID` 登录即可。

## 许可证

GPLv3
