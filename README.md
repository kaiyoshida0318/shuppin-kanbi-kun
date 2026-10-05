# 出品登録完備くん

商品ごとに「登録日付・商品名・商品コード・商品画像」を記録し、出品までの準備（画像圧縮・文字反映・IG登録など）をチェックで管理する表ツールです。

公開URL: https://kaiyoshida0318.github.io/shuppin-kanbi-kun/

## しくみ

```
[公開リポジトリ] shuppin-kanbi-kun    → このツール本体（GitHub Pages）
        ↓ ブラウザで開いてトークンを入力
[非公開リポジトリ] shuppin-kanbi-data  → 商品データと画像
```

- ツール本体（このリポジトリ）にはデータもトークンも入っていません。
- 商品データは `shuppin-kanbi-data` の `data/items.json`、画像は `images/` に保存されます。
- トークンは各自のブラウザの中だけに保存されます。

## 使う人の準備（最初の1回）

1. データ用リポジトリ `shuppin-kanbi-data` に招待してもらう（Settings → Collaborators）
2. 自分の GitHub でトークンを作る
   - 右上のアイコン → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token
   - Resource owner: `kaiyoshida0318`（招待された側は、リポジトリの持ち主を選ぶ）
   - Repository access: Only select repositories → `shuppin-kanbi-data`
   - Permissions → Contents: **Read and write**
3. 公開URLを開き、「GitHub につなぐ」画面にトークンを貼って「接続する」

## 使い方

- 上のフォームで商品を登録（画像は任意、JPG・PNG・WebP・GIF、10MBまで）
- チェック欄をクリックすると約1秒後に自動で保存されます
- 全項目にチェックが入ると「完備」になります
- 「チェック項目を編集」で項目の追加・名前変更・並べ替えができます
- ほかの人の変更は1分ごと、またはタブに戻ったときに反映されます。すぐ見たいときは「最新にする」

## データの場所

| 内容 | 場所 |
| --- | --- |
| 商品一覧とチェック項目 | `shuppin-kanbi-data/data/items.json` |
| 商品画像 | `shuppin-kanbi-data/images/` |

変更はすべてコミット履歴に残るので、誤って消した場合も GitHub の履歴から戻せます。
