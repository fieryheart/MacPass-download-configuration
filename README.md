# MacPass 安装&环境配置

## MacPass介绍
MacPass是基于KeePass的原生macOS的密码管理软件，兼容KeePass，可使用.kdb文件。
我安装的MacPass是

## MacPass的github链接
https://github.com/MacPass/MacPass

## 安装
> 以下按顺序安装，其中我碰到的问题会进行详细说明。
### 1. 下载MacPass源代码
> 需要另外更换源代码中的文件夹——DDHotKey & TransformerKit，这两个文件夹是链接另外的github库  
DDHotKey： https://github.com/mstarke/DDHotKey/tree/c7735ee66a0e73f1810d2d41f0b02004a4f5a330  
TransformerKit: https://github.com/mattt/TransformerKit/tree/337c309a4cf49ddec8902fd6de6d08b2cf8bd95f
### 2. 安装 Homebrew
> 官网链接：https://brew.sh/index_zh-cn  
安装过程中有可能碰到“/usr/local/bin is not a directory”错误，将这个文件删除就行，切记不要将此路径与“/usr/bin”相混淆，如果需要管理员权限，就加上sudo可完事。
### 3. 安装 Carthage
在终端中输入brew install Carthage即可
### 4. 安装 依赖包
> 终端进入下载好的MacPass文件夹, 执行命令：carthage bootstrap --platform macOS
### 5. 构建&执行
> 依赖包安装完成后，执行一下命令：xcodebuild -scheme MacPass -target MacPass -configuration Release CODE_SIGNING_REQUIRED=NO NO_SPARKLE=NO_SPARKLE  
（注意，如果 DDHotKey 和 TransformerKit 这两个文件夹没有重新安装，会出现报错）
### 6. 运行
> 安装成功后，可以在搜索中搜索到了，最后放在程序坞中就大功告成了。