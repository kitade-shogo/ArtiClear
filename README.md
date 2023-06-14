# ArtiClear 

## サービス概要
読まないままにしているブックマークを読む機会を提供する
「いつ」にフォーカスしたブックマーク管理サービスです

**サービスURL**: https://articlear.vercel.app/

**拡張機能URL**: https://chrome.google.com/webstore/detail/articlear-chromeextension/bflmbecdlbonjancnhafkkpepmfgpkke?hl=ja&authuser=0

**Githubリポジトリ**
- フロントエンド: https://github.com/kitade-shogo/ArtiClear-front
- バックエンド: https://github.com/kitade-shogo/ArtiClear-backend

## サービス利用方法
#### 1. ログイン後、連携したChrome拡張機能を追加
#### 2. ブックマークに追加したいページへ移動後、Chrome拡張機能から保存(ブックマーク登録) ![5a7375403ba1b148f5ab017710d85331](https://github.com/kitade-shogo/bookmark-app/assets/108001521/e8970c3b-957f-48ed-a06c-c5c089a8c537)

#### 3. 登録したブックマークはいつでもマイページのブックマークリストからご確認いただけます。<img width="1324" alt="Bookmark" src="https://github.com/kitade-shogo/bookmark-app/assets/108001521/96dace18-f5ab-4c55-94f6-6915ac558a0b">

#### 4. LINEと連携することにより、未読リストを一定期間ごとにユーザーに通知します(こちらの機能は未実装です)

## メインのターゲットユーザー
- プログラミング学習中の方
- 読んでいないブックマークが溜まっている方

## ユーザーが抱える課題
1. ブックマークをよく登録するが、数が多くなり整理できていない。
2. デフォルトのブックマーク機能はウィンドウが小さく、フォルダ内に大量のブックマークがあると見づらく・アクセスしづらい。
3. 既存のブックマークマネージャには「いつ」ブックマークしたのかを直感的に理解できるUIが導入されていない
4. あとで読むためにブックマークするが、忘れてしまう

## 解決方法
1. フォルダを作成して整理する。
2. フォルダの整理・アクセスを連携したアプリケーションに切り出すことで、探す手間を少なくする。
3. カレンダー機能を導入することにより、ブックマークした日時を視覚的に理解できるようにする。学習ログのような使い方も期待できる。
4. 未読のブックマークをユーザに通知するリマインド機能を実装する

## 実装した機能
- **ログイン、ログアウト機能**
  - FirebaseAuthenticationを使用したGoogleログイン・ログアウトができる
- **フォルダ作成機能**
  - アプリ本体からフォルダを作成できる
  - 拡張機能からフォルダを作成できる
- **ブックマーク機能**
  - 拡張機能から現在開いているタブを保存できる
- **ブックマークリスト機能**
  - アプリ本体でブックマークした記事を確認・アクセスできる

## 実装予定の機能
- **OGP表示機能**
  - それぞれのブックマークに取得元のサイトのOGPを表示する
- **カレンダー機能**
  - [pixela](https://pixe.la/ja)を使用してブックマーク履歴を可視化する
- **通知機能(LINEメッセージでの通知)**
  - 拡張機能から、「後で読む」ボタンを押して保存された記事を未読リストに追加する
  - 未読リストを一定期間ごとにLINEで通知する 

## なぜこのサービスを作りたいのか？
ブックマークした時には『後で読みたい』と思っていたのにそのまま忘れてしまうことがよくあり、せっかくの学習機会を捨てていて勿体無いと感じたからです。
また、ブックマークした時から時間が経っているほど、何を学習中にどういった理由でブックマークしたのか思い出しづらいので、適切なタイミングでリマインドしてくれるサービスが欲しいと思ったからです。

## 主な使用技術
### フロントエンド
- React
- JavaScript
- TailwindCSS
- NextUI
- react-three-fiber
### バックエンド
- Ruby on Rails(APIモード)
### 拡張機能
- React
- JavaScript
- Chrome Extensions API
### インフラ
- vercel
- Fly.io

### サードパーティ
- Firebase Authentication
