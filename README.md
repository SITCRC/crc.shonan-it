# SITCRC Official Website

**Official Website:** [crc.shonan-it.college](http://crc.shonan-it.college)

まず初めに、**SITCRC** とは、湘南工科大学 (Shonan Institute of Technology) の **コンピュータ研究部 (Computer Research Club)** のことを指します。

---

## 🔍 Overview

**SITCRC (Computer Research Club)** は、湘南工科大学の学生が主体となり、プログラミング、Web開発、ハードウェアの制作など幅広いIT関連の活動を行っています。学生が主体的に学び、実践する場として、日々スキル向上に取り組んでいます。

このレポジトリは、SITCRCの公式ウェブサイトを運営するためのものです。

---

## 🚀 Features

- Astroを使用した静的サイトジェネレーター
- GitHub Pagesによるデプロイ対応
- Markdownベースの記事投稿システム
- 多言語対応 (ja-JP, en-US, zh-TW, zh-CN)
- レスポンシブデザイン対応

---

## 🛠️ 編集環境

本プロジェクトの編集環境は、以下のツールを使用することを推奨しています。

### 必要なツール

- Linux (または WSL) ※推奨環境
- pnpm (パッケージ管理ツール)

### 環境構築手順

1. 必要なパッケージのインストール

   - **`curl`**: URLからデータをダウンロードするためのコマンドラインツールです。pnpmのインストールに使用します。

   ```bash
   sudo apt install curl
   ```

   - **`git`**: バージョン管理システムで、プロジェクトのクローンや変更履歴の管理に使用します。

   ```bash
   sudo apt install git
   ```

   - **`nodejs`**: JavaScriptの実行環境です。Astroのビルドや実行に使用します。

   ```bash
   sudo apt install nodejs
   ```

   - **`npm`**: Node.jsのパッケージマネージャで、`pnpm` のインストールに使用します。

   ```bash
   sudo apt install npm
   ```

2. pnpm のインストール

   ```bash
   curl -fsSL https://get.pnpm.io/install.sh | sh -
   ```

3. Node.jsのバージョン確認 (v18以上推奨)

   ```bash
   node -v
   ```

4. プロジェクトのクローンとインストール

   ```bash
   git clone https://github.com/SITCRC/crc.shonan-it.git
   cd crc.shonan-it
   pnpm install
   ```

---

## 📂 ファイル構成

### コンテンツ作成時の言語ルール

- 日本語の記事: `ファイル名.mdx`
- 英語の記事: `ファイル名_en-US.mdx`
- 繁体中国語の記事: `ファイル名_zh-TW.mdx`
- 簡体中国語の記事: `ファイル名_zh-CN.mdx`

### 翻訳ルール

- **日本語で書かれたコンテンツ** は翻訳が必須ではありませんが、可能であれば英語への翻訳が望ましいです。

- **日本語以外の言語で書かれたコンテンツ** は、日本語への翻訳が必須です。

このルールを徹底することで、言語ごとの管理が容易になります。



```
/
├── public/             # 画像や動画などの静的ファイル
├── src/
│   ├── components/     # 再利用可能なUIコンポーネント
│   ├── layouts/        # ページのレイアウトテンプレート
│   ├── pages/          # サイトの各ページ (.astro, .md, .mdx対応)
│   │   ├── index.astro # トップページ
│   │   ├── about.astro # Aboutページ
│   │   ├── blog/       # ブログ記事一覧
│   │   │   └── index.astro
│   │   ├── portfolio/  # ポートフォリオ一覧
│   │   │   ├── 2025.astro
│   │   │   └── 20XX.astro
│   │   ├── works.astro  # 実績ページ
│   │   └── contact.astro # お問い合わせページ
│   └── styles/         # CSSファイル
├── astro.config.mjs    # Astroの設定ファイル
├── package.json        # パッケージ情報
├── pnpm-lock.yaml      # pnpmのロックファイル
├── .gitignore          # Gitで無視するファイル
└── README.md           # 本ファイル
```

---

## 🌐 プレビュー方法

1. サーバーを起動

```bash
pnpm dev
```

2. ブラウザで以下のURLにアクセス

```
http://localhost:3000/
```

---

## 🔄 デプロイ方法

### 注意点

- 本サイトの多言語対応では、Google Translateを利用して翻訳を行う場合があります。そのため、誤訳や不自然な表現が含まれる可能性があります。見つけた際は、ご指摘いただけると幸いです。

- `main` ブランチに変更をプッシュすると、自動的にGitHub Pagesにデプロイされます。

- `public/` フォルダは静的ファイル用です。大きなファイルは避けてください。デプロイスクリプトの仕様上、毎回全ファイルが再アップロードされます。

- `preview/` は開発用のプレビュー用途のみで使用されます。たとえば、以下のような場面で活用できます：

  - 本番環境に公開する前にレイアウトの確認をしたいとき
  - コンテンツの仮配置やデザイン調整を行いたいとき
  - 外部ツールで生成したデータを仮保存し、確認したいとき

ここを編集しても本番サイトは更新されません。

---

## 📋 Pull Requestの流れ

SITCRCは、より多くの方々の協力を歓迎しています。以下の貢献方法が特に役立ちます：

- サイトデザインの改善
- コンテンツの翻訳 (特に英語・中国語対応)
- Markdownの記事執筆
- 新機能の提案や実装
- ドキュメントの修正や拡充

### Pull Requestの手順

1. Issueを立てる
2. 新しいブランチを作成
3. コードの変更を行い、Pull Requestを作成
4. レビュー後に `main` へマージ

---

## 📝 Astroファイルの書き方

Astroは、HTMLベースのフレームワークで、直感的かつ柔軟にWebページを作成できます。以下に、Astroファイルの基本的な構造や機能の説明を示します。

### Astroファイルの基本構造

以下は、Astroファイルでの基本的なページ構成の例です。ページ上部には `フロントマター`、中間には `HTML`、最後には `CSS` や `JavaScript` が組み合わさります。

Astroファイル (`.astro`) は、以下の3つのパートで構成されます：

```astro
---
// ここにJavaScript/TypeScriptのコード (サーバーサイド) を記述
const message = 'ようこそ、SITCRCへ！';
---

<html>
  <head>
    <title>{message}</title>
  </head>
  <body>
    <h1>{message}</h1>
  </body>
</html>
```

### パート解説

1. **`---`**\*\* (フロントマター)\*\*

   - 上部の3本線 `---` で囲まれた部分にJavaScript/TypeScriptのコードを記述します。変数定義やデータの取得などに使用します。

2. **HTML部分**

   - Astroは基本的にHTMLと同じ記述方法です。`{}` (中括弧) 内でフロントマターで定義した変数を埋め込めます。

### レイアウトの使用

複数のページに共通するレイアウトは `<Layout>` コンポーネントとして管理できます。以下はその使用例です。

#### `src/layouts/BaseLayout.astro`

```astro
---
const { title } = Astro.props;
---

<html>
  <head>
    <title>{title}</title>
  </head>
  <body>
    <slot /> <!-- ここにページ固有の内容が挿入される -->
  </body>
</html>
```

#### `src/pages/index.astro`

```astro
---
import BaseLayout from "../layouts/BaseLayout.astro";
---

<BaseLayout title="ホーム">
  <h1>ようこそ、SITCRCへ！</h1>
</BaseLayout>
```

### CSS & JavaScript

Astroファイル内にインラインで記述できますが、外部ファイルとして分離するのが推奨です。

#### インラインCSSの例

```astro
<style>
  h1 {
    color: #0070f3;
  }
</style>
```

#### インラインJavaScriptの例

```astro
<script>
  console.log('ページが読み込まれました');
</script>
```

### 画像の取り扱い

画像は `public/_images/` ディレクトリに配置し、次のように `import` で参照できます。

```astro
import Logo from '/_images/logo.png';
<img src={Logo} alt="SITCRCのロゴ" />
```

### Markdown の利用

ブログ記事や静的コンテンツの作成には Markdown (`.md`, `.mdx`) 形式が利用できます。Markdownファイル内でもAstroコンポーネントの利用が可能です。

### よくあるエラーと対策

- **「Page Not Found」エラー**：GitHub Pagesのデプロイ後にURL末尾が `/` で終わらないリンクが動作しない場合があります。`astro.config.mjs` の `base` 設定が正しいか確認してください。

- **「Unexpected token」エラー**：`---` (フロントマター) の記述漏れが原因の場合があります。

- **「Cannot find module」エラー**：パス指定の誤りが原因の場合があります。パスが `/` から始まっているか確認してください。

- **「Unexpected token」エラー**：`---` (フロントマター) の記述漏れが原因の場合があります。

- **「Cannot find module」エラー**：パス指定の誤りが原因の場合があります。パスが `/` から始まっているか確認してください。

これらの基本ルールを守ることで、効率的にAstroを活用できます。

- Astroファイルは基本的にHTMLのような構造で記述できます。
- レイアウトは `<Layout>` コンポーネントで共通化できます。既存のページを参考にしてください。
- CSSやJavaScriptはファイル末尾に直接記述できます。
- 画像は `_images/` に保存し、`import` で読み込みます。
- Markdown (`.md`, `.mdx`) でも同様にページを作成できます。既存のページを参考にしてください。

---

このレポジトリの基盤は、SITCRCの活動に関心を持ち、積極的に貢献している **[MotoYucchi](https://github.com/MotoYucchi)** によって作成されました。

---

## 📧 お問い合わせ

- お問い合わせ: [sit.comken@gmail.com](mailto\:sit.comken@gmail.com)
- GitHub: [SITCRC](https://github.com/SITCRC)

