# legal-pages — GitHub Pages公開手順

LifeRulerのプライバシーポリシー・利用規約を、GitHub Pagesで無料公開するための手順です。

## 1. リポジトリを作成する

GitHub上に `liferuler-legal` という名前の **public** リポジトリを新規作成します。

## 2. ファイルをアップロードする

このフォルダ内の以下のファイルを、`liferuler-legal` リポジトリのルートにアップロードします。

- `privacy.html`
- `terms.html`

## 3. GitHub Pagesを有効化する

1. `liferuler-legal` リポジトリの **Settings** タブを開く
2. 左メニューの **Pages** を開く
3. Source を `Deploy from a branch` にし、Branch を `main` / `(root)` に設定して保存

数分後、以下のURLでアクセスできるようになります。

```
https://YOUR_GITHUB_USERNAME.github.io/liferuler-legal/privacy.html
https://YOUR_GITHUB_USERNAME.github.io/liferuler-legal/terms.html
```

（`YOUR_GITHUB_USERNAME` は実際のGitHubユーザー名に置き換わります）

## 4. アプリ側のURLを差し替える

公開後、以下のファイルのURLを実際のURLに書き換えます。

```
src/config/support.ts

export const TERMS_URL   = 'https://YOUR_GITHUB_USERNAME.github.io/liferuler-legal/terms.html';
export const PRIVACY_URL = 'https://YOUR_GITHUB_USERNAME.github.io/liferuler-legal/privacy.html';
```

`YOUR_GITHUB_USERNAME` の部分を実際のGitHubユーザー名に置き換えてください。
（このファイルだけを修正すれば、Settings画面の「利用規約」「プライバシーポリシー」リンクが
正しいURLを開くようになります）

## 5. App Store Connectに登録する

App Store Connect の **App Privacy** / **Privacy Policy URL** 欄に、
`privacy.html` の公開URLを入力します。

```
https://YOUR_GITHUB_USERNAME.github.io/liferuler-legal/privacy.html
```
