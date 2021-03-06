# Cubism Web Samples

Live2D Cubism 4 Editorで出力したモデルを表示するアプリケーションのサンプル実装です。

Cubism Coreライブラリと組み合わせて使用します。


## 注意事項

本SDKを使用する前に、注意事項をご確認ください。

[こちら](./NOTICE.md)


## ディレクトリ構成

```
.
├─ .vscode              # Visual Studio Codeのタスクや設定が含まれるディレクトリ
├─ Core                 # Cubism Coreが含まれるディレクトリ
├─ Framework            # レンダリングやアニメーション機能などのソースコードが含まれるディレクトリ
└─ Samples
   └─ TypeScript
      └─ Demo           # サンプルプロジェクトが含まれるディレクトリ
         ├─ Resources   # モデルのファイルや画像などのリソースが含まれるディレクトリ
         └─ src
```


## Live2D Cubism Core for Web

用于加载模型的库。
该存储库不管理Cubism Core。 从此处下载Cubism SDK for Web，然后将文件复制到Core目录中。

当リポジトリではCubism Coreを管理していません。
[こちら](https://www.live2d.com/download/cubism-sdk/download-web/)からCubism SDK for Webをダウンロードして、
Coreディレクトリのファイルをコピーしてください。


## 開発環境の構築方法
如何建立开发环境

1. [Node.js](https://nodejs.org/)をインストールします。

1. [Visual Studio Code](https://code.visualstudio.com/)をインストールします。

1. Visual Studio Codeの拡張機能として下記を追加します。
   - [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
   - [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)


## ビルド方法
建立方法

1. Visual Studio Codeでプロジェクトディレクトリを開きます。
在Visual Studio Code中打开项目目录。

1. ビルドに必要な物をインストールします。
   ctrl+shift+P(macOSでは⌘+⇧+P)で`Tasks: Run Task`から`npm: install`を選択、
   または、`package.json`があるディレクトリ上にてターミナル上で`npm install`でサーバが起動します。
安装您需要构建的东西。 选择npm：从任务中安装：使用ctrl + shift + P运行任务（在macOS上为⌘+⇧+ P），或者在终端上package.json所在目录的终端上使用npm install启动服务器。

1. ビルドを行います。
   ctrl+shift+B(macOSでは⌘+⇧+B)でビルドタスクを選択、またはターミナル上でnpmコマンドを実行してJavaScriptを生成します。
   建立。 使用ctrl + shift + B（在macOS上为⌘+⇧+ B）选择构建任务，或在终端上执行npm命令以生成JavaScript。

### ビルドタスクの説明
生成任务说明

| コマンド | 説明 |
| --- | --- |
| `npm: build-framework` | フレームワークのみをビルドし、JavaScriptファイルを生成します |（仅构建框架并生成JavaScript文件）
| `npm: watch-framework` | フレームワークのみをウォッチし、変更が保存された際にJavaScriptファイルを再生成します |（保存更改后，仅查看框架并重新生成JavaScript文件）
| `npm: build-sample` | サンプルをビルドします |（建立sample）
| `npm: watch-sample` | サンプルをウォッチします |
| `npm: build-all` | フレームワークとサンプルをビルドします |(建立框架和样本)
| `npm: watch-all` | フレームワークとサンプルをウォッチします |


## ローカルサーバの起動方法
启动本地服务器

ビルドした成果物はそのままファイルを開くだけでは正常に動作しないため、ローカルサーバを起動する必要があります。
按原样打开该文件无法与内置产品一起正常工作，因此您需要启动本地服务器。

### 開発時

Visual Studio Codeの画面下の水色のフッターから「Go Live」をクリックするとサーバが起動します。
ブラウザ上で`index.html`のパスまで進むと動作を確認することが出来ます。
在Visual Studio代码屏幕底部的浅蓝色页脚中，单击“启动”，以启动服务器。 您可以转到浏览器上的index.html路径来检查操作。

ファイルの更新が行われると自動でブラウザのリロードが行われます。
また、`F5`を押すとでDebugger for Chromeの拡張が起動してデバッグを行うことが出来ます。
文件更新后，浏览器将自动重新加载。 同样，按F5键启动Chrome扩展调试器并进行调试。

### 検証時

ctrl+shift+P(macOSでは⌘+⇧+P)で`Tasks: Run Task`から`npm: serve`を選択、
または、`package.json`があるディレクトリ上にてターミナル上で`npm run serve`でサーバが起動します。
ブラウザ上で`index.html`のパスまで進むと動作を確認することが出来ます。
从任务中选择npm：serve：使用ctrl + shift + P（在macOS上为⌘+⇧+ P）运行Task，或者在package.json所在目录的终端上运行npm run serve。 您可以转到浏览器上的index.html路径来检查操作。

シンプルな構成のサーバのため検証時におすすめです。
由于服务器配置简单，建议进行验证。

## SDKマニュアル
SDK手册
[Cubism SDK Manual](https://docs.live2d.com/cubism-sdk-manual/top/)


## 変更履歴

当リポジトリの変更履歴については[CHANGELOG.md](/CHANGELOG.md)を参照ください。


## 動作確認環境

| Node.js | バージョン |
| --- | --- |
| Latest | 13.1.0 |
| LTS | 12.13.0 |

| プラットフォーム | ブラウザ | バージョン |
| --- | --- | --- |
| Android | Google Chrome | 78.0.3904.96 |
| Android | Microsoft Edge | 42.0.4.3989 |
| Android | Mozilla Firefox | 68.2.0 |
| iOS / iPadOS | Google Chrome | 78.0.3904.84 |
| iOS / iPadOS | Microsoft Edge | 44.10.7 |
| iOS / iPadOS | Mozilla Firefox | 20.1 |
| iOS / iPadOS | Safari | 13.0.3 |
| macOS | Google Chrome | 78.0.3904.97 |
| macOS | Mozilla Firefox | 70.0.1 |
| macOS | Safari | 13.0.3 |
| Windows | Google Chrome | 78.0.3904.97 |
| Windows | Internet Explorer 11 | 11.476.18362.0 |
| Windows | Microsoft Edge | 44.18362.449.0 |
| Windows | Mozilla Firefox | 70.0.1 |

Note: 動作確認時のサーバの起動は[検証時](/README.md#検証時)の方法で行っています。


## ライセンス

Cubism Web Samples は Live2D Open Software License で提供しています。
- Live2D Open Software License

  [日本語](https://www.live2d.com/eula/live2d-open-software-license-agreement_jp.html)
  [English](https://www.live2d.com/eula/live2d-open-software-license-agreement_en.html)

Live2D Cubism Core for Web は Live2D Proprietary Software License で提供しています。
- Live2D Proprietary Software License

  [日本語](https://www.live2d.com/eula/live2d-proprietary-software-license-agreement_jp.html)
  [English](https://www.live2d.com/eula/live2d-proprietary-software-license-agreement_en.html)

Live2D のサンプルモデルは Free Material License で提供しています。
- Free Material License

  [日本語](https://www.live2d.com/eula/live2d-free-material-license-agreement_jp.html)
  [English](https://www.live2d.com/eula/live2d-free-material-license-agreement_en.html)
  - `./Sample/TypeScript/Demo/Resources/Haru`
  - `./Sample/TypeScript/Demo/Resources/Hiyori`
  - `./Sample/TypeScript/Demo/Resources/Mark`
  - `./Sample/TypeScript/Demo/Resources/Natori`
  - `./Sample/TypeScript/Demo/Resources/Rice`

上記のモデルをご利用になられる場合、[こちら](https://docs.live2d.com/cubism-editor-manual/sample-model/)で各モデルに設定された利用条件に同意して頂く必要がございます。

直近会計年度の売上高が 1000 万円以上の事業者様がご利用になる場合は、SDKリリース(出版許諾)ライセンスに同意していただく必要がございます。
- [SDKリリース(出版許諾)ライセンス](https://www.live2d.com/ja/products/releaselicense)

*All business* users must obtain a Publication License. "Business" means an entity with the annual gross revenue more than ten million (10,000,000) JPY for the most recent fiscal year.
- [SDK Release (Publication) License](https://www.live2d.com/en/products/releaselicense)
