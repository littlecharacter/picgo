# Typora+PicGo-Core+Git+Jsdelivr实现高效图文写作

## 01、Typora

下载地址（最后一个免费版）：https://download.typora.io/windows/typora-setup-x64-0.11.18.exe

配置：文件》偏好设置》图像

![image-20220705215955](https://gitee.com/littlecharacter/picgo/raw/master/img/20220705215955.png)

其中，
1. 会下载到：``C:\Users\{UserName}\AppData\Roaming\Typora\picgo\win64``
2. 配置如下：``C:\Users\{UserName}\.picgo\config.json``

```json
{
  // Gitee配置
  "picBed": {
    "uploader": "gitee",
    "current": "gitee",
    "gitee": {
      "repo": "littlecharacter/picgo",
      "branch": "master",
      "token": "e65cab40a673cc5ba2ff0c57558c980c",
      "path": "img/",
      "customPath": "default",
      "customUrl": ""
    },
    "transformer": "path"
  },
  // GitHub配置
  // "picBed": {
  //   "uploader": "github",
  //   "current": "github",
  //   "github": {
  //     "repo": "littlecharacter/picgo",
  //     "branch": "main",
  //     "token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
  //     "path": "img/",
  //     // Jsdelivr配置
  //     "customUrl": "https://cdn.jsdelivr.net/gh/littlecharacter/picgo"
  //   },
  //   "transformer": "path"
  // },
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
    "picgo-plugin-super-prefix": true,
    // Gitee上传插件
    "picgo-plugin-gitee-uploader": true
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

## 02、Gitee OR GitHub

1. 注意git仓库的分支
2. github生成token时，需要勾上``repo``，Gitee默认即可

## 03、[Jsdelivr](https://www.jsdelivr.com/?docs=gh)  

![image-20220623013726639](https://cdn.jsdelivr.net/gh/littlecharacter/picgo/img/20220623/20220623013728.png)

<font color="red">注：</font>Jsdelivr的url，可以不加仓库的分支``https://cdn.jsdelivr.net/gh/user/repo/xx/file`` 

> cdn加速，如果使用github等国外git需要cdn加速，不过加速可能随时不靠谱


