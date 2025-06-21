<div align="center">
<img src="chrome-extension/public/icon-128.png" alt="logo"/>
<h1> Sync your cookie to <br/>Cloudflare</h1>
</div>

[English](./README.md) | [中文](./README_ZH.md)

`Sync your cookie` 是一个 Chrome 扩展程序，它可以帮助您将 Cookie 同步到 Cloudflare。它是一个有用的工具，用于在不同设备之间共享 Cookie, 免去了登录流程的烦恼，此外也提供了cookie管理面板查看，管理已经过同步的 cookie。


<!-- // 使用gif展示功能 -->

### 功能
- 支持同步 Cookie 到 Cloudflare
- 支持为不同站点配置`Auto Merge`和`Auto Push`规则
- Cookie数据经过 protobuf 编码传输
- 提供了一个管理面板，方便查看、复制、管理已经同步的 Cookie 数据

### 项目截图

账号设置页面

<img width="600" src="./screenshots/settings.png" alt="account settings"/>

Cookie 同步页面

<img width="600" src="./screenshots/sync.png" alt="cookie sync popup"/>

Cookie 管理侧边栏面板

<img width="600" src="./screenshots/panel.png" alt="cookie manager sidebar panel"/>
### 使用

#### 安装步骤
1. 访问 [Chrome应用商店](https://chromewebstore.google.com/detail/sync-your-cookie/bcegpckmgklcpcapnbigfdadedcneopf) 安装扩展
2. 点击浏览器工具栏中的扩展图标打开设置页面
3. 在设置页面配置您的Cloudflare账户信息

#### 配置说明
在设置页面需要提供以下Cloudflare凭证：
1. **Authorization Token**:
   - 登录Cloudflare控制台
   - 进入"My Profile" → "API Tokens"
   - 创建新令牌，选择"Edit Cloudflare Workers"模板
   - 权限范围选择：Account.Workers KV Storage:Edit
   - 复制生成的令牌

2. **Account ID**:
   - 登录Cloudflare控制台
   - 进入主页，在右下角"API"部分找到Account ID

3. **Namespace ID**:
   - 登录Cloudflare控制台
   - 进入"Workers" → "KV"
   - 创建新命名空间（如"cookie-sync"）
   - 复制命名空间ID

#### 功能使用
- **Cookie同步**：在任意网站点击扩展图标，选择"同步Cookie"选项
- **自动同步配置**：在设置页面为特定域名配置自动同步规则
- **Cookie管理**：打开侧边栏面板查看和管理已同步的Cookie

#### 隐私政策
请参考[隐私政策](./private-policy.md)了解数据安全详情
