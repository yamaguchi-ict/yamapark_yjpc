# YAMA PARK — 完成作品特設サイト

やまぐちジュニアプログラマーコンテスト(YJPC)2026 の優秀者が参加した「PICO PARK 風ショートゲームをつくろう！」ハッカソンで生まれた、2人協力ミニゲーム「YAMA PARK」12作品の特設サイトです。

| 項目 | 内容 |
|---|---|
| 主催 | 山口県教育委員会 |
| 運営 | 林兼コンピューター株式会社 |
| コンテスト | やまぐちジュニアプログラマーコンテスト (YJPC) 2026 — <https://jrp.yamaguchi-ict.info/> |
| コンセプトページ | <https://sites.google.com/g.ysn21.jp/yama-park/%E3%83%9B%E3%83%BC%E3%83%A0> |
| 素材 | ピコキャット画像 96枚(Google Drive「Characters」フォルダより取得) |

## 公開手順 (GitHub Pages)

### 1. リポジトリを作成
GitHub で新規リポジトリ (例: `yamapark`) を作成します。Public でOK。

### 2. このフォルダの中身を upload / push
`index.html` と `assets/` フォルダ(ロゴ・ピコキャット)を、リポジトリのルートにそのまま置きます。

```bash
git init
git add index.html assets/
git commit -m "YAMA PARK showcase site"
git branch -M main
git remote add origin https://github.com/<あなたのID>/yamapark.git
git push -u origin main
```

※ GitHub のウェブ画面から「Add file → Upload files」でもOK(drag & drop で `index.html` と `assets/` を一緒にアップロード)。

### 3. Pages を有効化
リポジトリの **Settings → Pages** → Source を `Deploy from a branch` → ブランチ `main` / フォルダ `/(root)` に設定して保存。

数分待つと、`https://<あなたのID>.github.io/yamapark/` で公開されます。

## 構成

| パス | 内容 |
|---|---|
| `index.html` | サイト本体(単一ファイル。ロゴ+ピコキャット23体は base64 で埋め込み済みなので、`index.html` 1枚だけでも開けます) |
| `assets/yamapark-logo.png` | YAMA PARK ロゴ画像 |
| `assets/picocat/` | ピコキャット素材 96枚(Google Drive「Characters」フォルダの原本) |
| `README.md` | 本ファイル |

## カスタマイズ方法

| 場所 | 内容 |
|---|---|
| `STAGES` 配列 (`index.html` 内スクリプト) | 12作品の順番・お題・作者名・説明文・Scratch プロジェクトID・使用キャラ(`cat`) |
| ヒーロー見出しコピー | キャッチコピー・サブコピー |
| クレジット (`#credits` 内の `organizer`) | 主催・運営・関連サイト |
| 配色 (`index.html` 内 `:root` CSS 変数) | `--bg1`, `--bg2`, `--bg3`, `--pk1`, `--pk2`, `--cyn`, `--grn`, `--yel` など |

ステージの並びは「お題ごとに整理し、ラストステージを最後(12番目)に配置」。変更したい場合は `STAGES` 配列の順序を入れ替えてください。

## 補足

- YJPC の略称に統一してあります(やまぐちジュニアプログラマーコンテスト)。
- サムネイル画像は Scratch の CDN から取得。取得できない場合はプレースホルダーが表示されます。
- ゲームは各カードの「PLAY」ボタンから、ページ内に Scratch の iframe で開きます。
- PC (キーボード1台で2人)での操作を想定しています。
- レスポンシブ対応: スマートフォン・タブレットではステージが1カラムに、760px以下ではナビがハンバーガーメニュー(タップ開閉)に切り替わります。

- 商標注記: 「PICO PARK」は TECOPARK株式会社の登録商標です。本イベント・本サイトはTECOPARK株式会社が主催・関与するものではありません。なお、イベント開催および広報素材の使用については、同社の許諾を得ています。

## お問い合わせ

運営: 林兼コンピューター株式会社 (やまぐちジュニアプログラマーコンテスト事務局)
