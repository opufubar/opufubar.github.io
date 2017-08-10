# 大阪府立大学プログラミングサークルFu-barの公式HP

## サイト管理用ツール
- Hugo ver0.21

## 新規の日記投稿手順
   
```sh
? hugo new post/20170809.md
? less content/post/20170809.md
+++
date = "2017-08-09T01:11:22+09:00"
title = "20170809"

+++
```

1. このタイトルをテキストエディタで，その投稿のタイトルに変える
2. 2つ目の+++の下に中身を書く
3. 日記一案のページで一部分だけ見えるようにしている．見える部分と見えない部分を分けるところに

```html
<!--more-->
```

を入れる

## デプロイ

- 基本的にはドキュメントルートにあるdeploy.shで一気にデプロイできる
- HP自体はMasterブランチを公開しているが，それをHugoで生成するための材料をgh-pagesブランチで管理している
- どちらかだけPushに失敗するなどのことがあればそれぞれ手動で直すこと

```sh
? ./deploy.sh
```

エラーが返らなければ完了

## 別の変更履歴のプル

基本的にはフェッチ→マージを行うのが良い

```sh
? git fetch
? git merge
```

わからなければとりあえずプルしとけばいい．困ったら都度相談or検索！

```sh
? git pull
```

## 新しいメンバーの紹介を追加

```sh
? hugo new member/new-member-name.md
? less content/member/new-member-name.md
+++
date = "2017-06-08T18:28:31+09:00"
title = "new-member-name"
+++
```

このdateの1行を消して，titleの欄には各自の名前をローマ字でいれる．
