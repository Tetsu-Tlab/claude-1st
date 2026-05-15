# 明朝のデプロイ手順（3コマンド）

おはようございます。下の3つを順に実行すれば公開URLが出ます。

PowerShell で `Claude入門講座サイト` フォルダに移動してから実行してください。

## 1. Vercel CLI をインストール（初回のみ・約2分）

```powershell
npm i -g vercel
```

## 2. Vercel にログイン（ブラウザが開きます）

```powershell
vercel login
```

前回 `t-lab-skill-guide` をデプロイしたのと同じアカウントを選んでください。

## 3. デプロイ（初回は対話で5つくらい質問されます）

```powershell
vercel --prod
```

聞かれる内容と推奨回答：

| 質問 | 回答 |
|---|---|
| Set up and deploy? | `Y` |
| Which scope? | 前回と同じチーム（`team_dwhO01dInTp1IEKT1VaIYp9Q`）|
| Link to existing project? | `N`（新規作成）|
| Project name? | `t-lab-claude-guide` |
| Code directory? | そのまま Enter（`./`）|
| Modify settings? | `N` |

完了すると `https://t-lab-claude-guide-xxxx.vercel.app` のようなURLが出ます。
これを受講者に共有してください。

---

うまくいかない箇所があれば、ターミナルの出力をそのまま貼り付けてもらえれば、こちらで原因を見ます。

合言葉は前回と同じ **`tlab2026`** です。
