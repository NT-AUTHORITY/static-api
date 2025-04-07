# Static-API
一个用于在 Notion、GitHub README 等环境下实现复制等操作的静态 API。  
可以通过 [Cloudflare Pages](https://dash.cloudflare.com) 部署。
## API 请求
永远为 `GET`；  
永远有 `closeType`。值为 1 或 2。  
1 为关闭窗口`window.close();`，2为返回`history.back();`。  
请在不同情况下使用不同的。例如，Notion默认使用新标签页打开，使用1；GitHub默认使用本标签页打开，使用2。
### `/copy`
**`text`** 需要复制的文本
### `/launch`
**`url`** 需要启动的网页 URL
### `/decryptEmail`
**`base64`** 使用 `Base64` 编码的电子邮件字符串
## Demo
### 复制
[点击此处将 `Hello World` 复制到剪贴板](https://static-api.lukezhang.win/copy?closeType=2&text=Hello+World)
### 在小窗口中打开
[打开 Bing.com](https://static-api.lukezhang.win/launch?closeType=2&url=https://www.bing.com)
