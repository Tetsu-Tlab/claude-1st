# T-Lab Claude Lab for Teachers

先生向けAI講座 T-Lab の限定公開ガイドサイト。
Claudeを「使う」から「相棒にする」までを、小学校教員向けに体系化した実践書です。
**Cursor の中の統合ターミナルで Claude Code を運用する** スタイルを軸に、30日でマスターまで連れていくロードマップ付き。

## サイト構成

```
Claude入門講座サイト/
├─ index.html   サイト本体（CSS・JSすべて内包した単一ファイル）
└─ README.md    このファイル
```

外部ファイルへの参照は Google Fonts のみ。インターネットがあれば、index.html を任意のフォルダに置くだけで動作します。

## 章立て

- **HERO / 教職の1日が変わる**：Before/After で「返ってくる時間」を見せる
- **STAGE 01 入門**：Claudeとは／6つの強み／教職で増える9シーン／他AIとの比較／プラン
- **STAGE 02 基本**：Projects・Artifacts／学級通信レシピ／スライド・掲示物／プロンプト4要素
- **STAGE 03 発展**：Cursor×Claude Code の哲学／インストール／CLAUDE.md／Permission Mode／校務実践4連発／Skill・Slash Commands・Hooks／共有
- **30日ロードマップ**：Week 1 慣れる → Week 2 整える → Week 3 仕組む → Week 4 広げる
- **教職の展望**：授業・校務・個別最適・チームづくり 4領域
- **資料室**：用語集／プロンプト集／CLAUDE.md テンプレ／チェックリスト／困ったときの対処
- **FAQ**：11問

## 動作確認（ローカル）

`index.html` をダブルクリックでブラウザに表示できます。
パスワードは **`tlab2026`**（Skill構築ガイドと共通）です。

> SHA-256 で照合しているため、サイト内に平文のパスワードはありません。

## パスワードの変更方法

1. PowerShell で新パスワードのハッシュを計算する
   ```powershell
   $bytes = [System.Text.Encoding]::UTF8.GetBytes("新しいパスワード")
   $sha = [System.Security.Cryptography.SHA256]::Create()
   ($sha.ComputeHash($bytes) | ForEach-Object { $_.ToString("x2") }) -join ""
   ```
2. 出力されたハッシュを `index.html` 末尾の `PASS_HASH` に貼り付ける
3. 保存して再読み込み

> 入力欄は「全角→半角」「前後の空白除去」を自動で行うので、IMEがオンのままでも認証できます。

## 公開する場合

このフォルダごと Vercel / Netlify / GitHub Pages 等にデプロイすれば公開できます。
静的ファイルだけなので追加設定は不要です。

> パスワード認証はクライアントサイドのため、本格的な機密保護には向きません。
> 「カジュアルな閲覧防止」の用途想定です。

## メンテナンス

- 文章を直したい：`index.html` の該当セクションを編集
- 30日プランを増減：`<section id="roadmap">` 内の `.week` ブロックを編集
- 色やレイアウトを変えたい：`<style>` の `:root` 変数や各セレクタを編集
- 認証や挙動を変えたい：末尾の `<script>` を編集

## 注意

- 本資料は T-Lab 受講者向けの限定公開教材です
- 児童の個人情報を含む内容は記載していません
- 他講座・他用途への転載は事前にご相談ください
