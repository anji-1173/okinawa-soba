# アンジの沖縄そば巡りの旅 — ブログサイト

**公開中のブログ：[沖縄そば巡りの旅｜沖縄本島の沖縄そば屋 食べ歩きレビュー](https://okinawa-soba.apps-okinawa.workers.dev/)**

沖縄本島の沖縄そば屋の全店制覇を目指す食べ歩きブログです。写真付きの実食レビューと、麺・スープ・具の星評価でお店を紹介しています。

- [お店の一覧と地図](https://okinawa-soba.apps-okinawa.workers.dev/)
- [沖縄そばのうんちく（歴史・沖縄そばの日・木灰そば・麺と製麺所など）](https://okinawa-soba.apps-okinawa.workers.dev/trivia/)
- English: [Okinawa Soba Journey](https://okinawa-soba.apps-okinawa.workers.dev/en/trivia/) ／ 한국어: [오키나와 소바 순례 여행](https://okinawa-soba.apps-okinawa.workers.dev/ko/trivia/) ／ 繁體中文: [沖繩麵巡禮之旅](https://okinawa-soba.apps-okinawa.workers.dev/zh-TW/trivia/)

---

note（ https://note.com/anjiijna ）で連載中の「沖縄そば巡りの旅」をもとにした、
アンジ専用の沖縄そばブログサイトです。

- `index.html` … サイト本体（1ファイル完結・そのままブラウザで開けます）
- GitHub Pages を有効にすると `https://<ユーザー名>.github.io/<リポジトリ名>/okinawa-soba/` で公開できます

## 写真の入れ方（お店フォルダごとアップロード）

写真ファイルが「1.jpg, 2.jpg…」のように番号で、お店ごとのフォルダに
分かれている場合は、**フォルダ構造を保ったままアップロード**してください。
（同じ番号のファイルが多数あるため、1か所にまとめると上書きされて消えます）

### GitHub Web からのアップロード手順
1. リポジトリを開き、ブランチ `claude/okinawa-soba-blog-site-s7h78g` に切り替え
2. `okinawa-soba` フォルダを開く →「Add file」→「Upload files」
3. `E:\ノート（素材）` を開き、**`沖縄そば` フォルダごと**アップロード欄にドラッグ
   → `okinawa-soba/沖縄そば/<店名>/1.jpg` の階層が保たれる
4. 「Commit changes」

### アップロード後
- 各お店フォルダの写真から1枚をカードのメイン写真に採用
- `index.html` の `SOBA_SHOPS` の各店 `photo:null` を
  `photo:"沖縄そば/EIBUN/1.jpg"` のように書き換えると画像が表示される
  （この作業は自動でまとめて反映可能）
- フォルダ名の一覧＝訪問した全店舗リストになるため、
  未掲載のお店もフォルダ名から追加できる

## 少数の写真だけ試す場合
`okinawa-soba/photos/` フォルダを作って写真を置き、
`photo:"photos/eibun.jpg"` のように個別指定してもOKです。

## お店の追加・編集

`index.html` の `SOBA_SHOPS` 配列に1ブロック追加するだけです。

```js
{name:"店名", area:"市町村", region:"naha|south|central|north|other",
 tags:["オススメ"], desc:"紹介文", url:"noteの記事URL", photo:null},
```

## メモ

- 各カードの紹介文は note記事のタイトル・要約をもとにした短い引用ダイジェストです。
  全文は各カードの「noteで読む」リンクから note へ飛べます。
- 記事の全文をサイトに載せたい場合は、note の本文を貼っていただければ
  記事ページを追加できます。
