## [Typora+PicGO-Core (command line)+ Github实现写作时图片自动上传](https://www.cnblogs.com/chonglu/p/16894257.html)

### 摘要

在使用Typora写作时，经常会配上图片，使得文章图文并茂，一目了然，但默认图片是在本地的，发布在网络上，别人就看不到图片。Typora就可以实现粘贴图片自动上传，因大部分OSS或图床需要收费或很不稳定或配置麻烦，本文将以Typora+PicGo-core+Github作为演示。结尾附Typora破解方式，最新版（1.4.8）可用。

### Github配置

1、新建一个Github公开仓库

[![image-20221115214651248](https://github.com/jywangyou/Typora_Images/raw/main/img/202211171032490.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171032490.png)

2、生成一个Token，选择无限期，勾选**repo**，拉到最下方点击 **Generate token** 生成

[![image-20221115214815719](https://github.com/jywangyou/Typora_Images/raw/main/img/202211171034049.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171034049.png)

3、接下来在网页会出现一串token，复制保存，这串token不会再出现第二遍，但是可以更新生成新的token

### Typora配置

1、下载并安装Typora，https://typora.io/releases/all 截至2022.11.15本人亲测最新啊不版1.4.8可pojie

2、打开Typora，依次点击文件--偏好设置--图像

[![image-20221115215208986](https://github.com/jywangyou/Typora_Images/raw/main/img/202211171035131.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171035131.png)

3、点击**下载或更新**，下载PicGo插件

4、打开配置文件，按照如下修改

[![image-20221115215347422](https://github.com/jywangyou/Typora_Images/raw/main/img/202211171034043.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171034043.png)

```json
{
  "picBed": {
    "current": "github",
    "github": {
      "repo": "luchong0813/Typora_image", //自己的仓库名
      "branch": "main", //默认
      "token": "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", //github的token
      "path": "img/", //在仓库下再建一个img文件夹，可以为空
      "customUrl": "https://github.com/luchong0813/Typora_image/raw/main" //按自己的来
    },
    "uploader": "github",
    "transformer": "path"
  },
  "picgoPlugins": {
    "picgo-plugin-github-plus": true
  }
}
```

### 测试验证

1、点击图像中的**验证图片选项**

[![image-20221115220645932](https://github.com/jywangyou/Typora_Images/raw/main/img/202211171037284.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171037284.png)

Tips：由于Github原因，有时可能上传不成功，如果在编辑文档时上传，能显示Github地址，也表示上传成功，Typora不加载也没关系

2、查看Github仓库是否已上传图片

[![image-20221115220837593](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171037290.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171037290.png)

### Typora破解

1、下载我提供的包，将**winmm.dll**Copy至Typora根目录

下载地址：https://wwk.lanzoul.com/izEnN0fzv48j 密码:0813

[![image-20221115220008901](https://github.com/jywangyou/Typora_Images/raw/main/img/202211171038123.png)](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171038123.png)

[![image-20221115220121436](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171038346.png)-

2、打开Typora，在帮助--我的许可证中可以看到激活状态

[![image-20221115220215923](https://luc-images.oss-cn-shenzhen.aliyuncs.com/typora/202211171039868.png)
