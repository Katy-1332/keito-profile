# Keito Yamada | Profile

山田啓人の個人プロフィールページ。HTML/CSSだけで作った静的サイトです。名刺と同じ白＋ネイビーのデザインです。

## ファイル構成

```text
keito-profile/
├── index.html
├── style.css
└── README.md
```

## ローカルで確認する

`index.html` をブラウザで開くか、VS Code の Live Server 等で確認してください。スマートフォン幅でもレイアウトが変わります。

## GitHub Pagesで公開する

1. GitHub（Katy-1332）で **公開リポジトリ** `keito-profile` を新規作成します（既存のリポジトリと重複しないことを確認）。
2. この3ファイルをリポジトリのルートに配置し、`main` にコミット・Pushします。
3. リポジトリの **Settings → Pages → Build and deployment** で、Sourceを **Deploy from a branch**、Branchを **main**、Folderを **/(root)** にして保存します。
4. 公開後に実際にアクセスし、リンク・スマホ表示を確認します。
5. 公開先のURLを使って実際のQRコードを生成し、名刺に配置します。推測したURLやダミーQRコードで名刺を印刷しないでください。

通常の公開URLの形式は `https://Katy-1332.github.io/keito-profile/` です。公開設定前には使えません。

## 後から編集する

### noteのリンクを追加

`index.html` 内の「リンク準備中」と「noteのURLを後から追加します」の部分を更新。カードの末尾に、例えば次のリンクを追加できます。

```html
<a href="https://note.com/自分のアカウント" target="_blank" rel="noopener noreferrer">noteの記事を見る ↗</a>
```

URLは自分の実際のURLに置き換え、リンク準備中という表記も変更してください。

### プロフィール写真を追加

写真を `assets/profile.jpg` に保存し、`index.html` の `.hero-art` の内側にある `KY` 表示を次の画像に差し替えます。

```html
<img class="profile-photo" src="assets/profile.jpg" alt="山田啓人のプロフィール写真">
```

`style.css` に以下を追加します。

```css
.profile-photo { position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover; z-index: 1; }
```

写真の利用許諾や背景に他人が写っていないかも確認してください。

### アンケートを追加

Googleフォーム等でフォームを作ったら、`U-15 Talent Platform` のカード末尾に実際のURLへのリンクを追加します。未成年の個人情報を取得する質問については、公開前に十分検討してください。

### 指導歴・資格を追加

`ABOUT` セクションのテキストや `<dl class="details">` 内の項目を更新します。名刺に載せなくてもWeb側だけ増やせます。

### その他

文言は `index.html`、色・余白・フォントは `style.css` で変更します。更新ファイルを `main` にPushするとGitHub Pagesが再公開します。**同じリポジトリ名・公開URLを維持すれば名刺のQRを変更する必要はありません。**

## 注意

- このサイトは個人のプロフィールであり、所属校の公式サイトではありません。
- 公開サイトには電話番号を掲載していません（名刺掲載とは公開範囲が異なるため）。必要なら公開範囲を確認の上で追加してください。
- note・アンケート・写真は現時点では準備中です。架空のURLや読み取れないQRコードは置いていません。
