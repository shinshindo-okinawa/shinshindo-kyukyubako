# 心身堂 救急箱サポート／TEAM CARE BOX

心身堂鍼灸整骨院 読谷院の部活動・スポーツチーム向け「救急箱サポート企画」のサイトです。

> このリポジトリは公開（Public）です。患者様・チームの個人情報は絶対に入れないでください。

## ページ

| ページ | アドレス | 使う人 |
|---|---|---|
| テーピング動画ガイド（トップ） | https://shinshindo-okinawa.github.io/shinshindo-kyukyubako/ | ご案内サイトの「TEAM CARE BOX のご案内ページ」から |
| 部位ごとの動画ページ | `support/{slug}/` | トップから |
| TEAM CARE BOX サポートLP | https://shinshindo-okinawa.github.io/shinshindo-kyukyubako/team-care-box/ | **テーピングのスターターセットを購入したチームだけ**（QRなどで案内。特別感を残すため、ご案内サイトなどからはリンクしていません） |
| 管理画面 | `admin/` | スタッフ（ブラウザで `data/videos.json` を編集→ダウンロード→差替） |

## ファイル

- **公開ページ**: `index.html` / `support/{slug}/`
- **LP**: `team-care-box/index.html`、見た目は `assets/css/lp-tcb.css`、動きは `assets/js/lp-tcb.js`
- **データ**: `data/videos.json`（動画・LINE・予約・補充注文のリンク、医療機関へ行くべき症状）、`data/tcb-links.json`（LPの3つのボタン：テーピングガイド・症状絞り込みチェック・セルフケアガイド）

## TEAM CARE BOX LP から心身堂ご案内サイトへのリンク

LPを閉じずに、ご案内サイトの合うページへ **新しいタブで** 移動できます。
リンクは `team-care-box/index.html` に直接書いてあります（`data-guide="..."` がついている `<a>`）。

| 場所 | リンク先（ご案内サイト） |
|---|---|
| 「もっと知りたいときは」 | 学校でケガをしたときの手続き（`sports.html#school`） |
| 〃 | スポーツ中のケガに使える保険（`sports.html#sportsIns`） |
| 〃 | スポーツのケガ・競技のお悩み一覧（`symptoms.html#sym-g5`） |
| 〃 | スポーツ向けのコース（`sports.html#courses`） |
| 〃 | 来院の流れ・保険の使い方（`first.html`） |
| 〃 | 受付時間・休診日・場所（`menu.html#info`） |
| 〃 | 心身堂のご案内をすべて見る（トップ） |
| 紹介特典の下 | 心身堂ってどんなところ？（`about.html`） |
| 「医療機関へ」の注意の下 | 医療機関の受診が先になる症状について（`symptoms.html#redFlags`） |

リンク先を変えるときは `href` を書きかえます。新しいタブで開く設定（`target="_blank"`）は `assets/js/lp-tcb.js` でも自動でつきます。

## 変更の記録

### 2026-11-23 ご案内サイトへのリンクを追加
- 3つのツールの下に「もっと知りたいときは」コーナーを追加（保護者・コーチ・選手向けの6ページ＋ご案内トップ）
- 紹介特典の下に「心身堂ってどんなところ？」、医療機関への注意の下に「受診が先になる症状」へのリンク
- どのリンクもLPを残したまま新しいタブで開く
