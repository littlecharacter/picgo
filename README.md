# Typora+PicGo-Core+GitHub+Jsdelivr实现高效图文写作

## 01、Typora

下载地址（最后一个免费版）：https://download.typora.io/windows/typora-setup-x64-0.11.18.exe

配置：文件》偏好设置》图像

![image-20220623011110090](https://cdn.jsdelivr.net/gh/littlecharacter/picgo/img/20220623/20220623011111.png)

其中，

②会下载到：``C:\Users\{UserName}\AppData\Roaming\Typora\picgo\win64``

③配置如下：``C:\Users\{UserName}\.picgo\config.json``

```json
{
  // GitHub配置
  "picBed": {
    "uploader": "github",
    "current": "github",
    "github": {
      "repo": "littlecharacter/picgo",
      "branch": "main",
      "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
      "path": "img/",
      // Jsdelivr配置
      "customUrl": "https://cdn.jsdelivr.net/gh/littlecharacter/picgo"
    },
    "transformer": "path"
  },
  // "settings": {
  //   "server": {
  //     "enable": true,
  //     "host": "127.0.0.1",
  //     "port": 36677
  //   },
  //   "privacyEnsure": true,
  //   "showUpdateTip": true,
  //   "autoRename": true,
  //   "pasteStyle": "markdown",
  //   "rename": true
  // },
  // 插件：C:\Users\{UserName}\AppData\Roaming\Typora\picgo\win64\picgo install xx
  "picgoPlugins": {
    // 文件重命名插件
    "picgo-plugin-rename-file": true,
    // GitHub增强插件
    "picgo-plugin-github-plus": true,
    // 配置文件目录插件
    "picgo-plugin-super-prefix": true
    // 水印插件：picgo-plugin-watermark
  },
  // 插件配置
  "picgo-plugin-super-prefix": {
    "prefixFormat": "YYYYMMDD/",
    "fileFormat": "YYYYMMDDHHmmss"
  },
  "picgo-plugin-rename-file": {
    // "format": "{origin}-{y}{m}{d}{h}{i}{s}"
  }
}
```

## 02、GitHub

1. 注意github仓库的分支
2. 生成token时，需要勾上``repo``

## 03、[Jsdelivr](https://www.jsdelivr.com/?docs=gh)  

![image-20220623013726639](https://cdn.jsdelivr.net/gh/littlecharacter/picgo/img/20220623/20220623013728.png)

<font color="red">注：</font>Jsdelivr的url，可以不加仓库的分支``https://cdn.jsdelivr.net/gh/user/repo/xx/file`` 


