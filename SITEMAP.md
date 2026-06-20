# Do Lab AI — サイトマップ設計

issue #54 対応

---

## 1. サイトマップ図

```
Do Lab AI
│
├── /                          トップ（概要・特徴・3サービス一覧）
├── /apply.html                無料相談・応募ページ
│
├── /m1/                       M1 — 設計書Bot
│
├── /m2/                       M2 — AIパック
│
└── /m3/                       M3 — 学ぶ（トップ）
    ├── /m3/compare.html       AIツール比較表（ChatGPT/Gemini/Claude/Copilot）
    ├── /m3/prompts.html       プロンプト集
    ├── /m3/news.html          AI最新ニュース
    ├── /m3/claude-code.html   初めてのClaude Code
    ├── /m3/dojo.html          特命AI集中道場
    ├── /m3/webinar.html       ウェビナーアーカイブ
    ├── /m3/room.html          特命AI室
    └── /m3/tools/             AIツール紹介（一覧）
        ├── chatgpt.html       ChatGPT
        ├── gemini.html        Gemini
        ├── claude.html        Claude.ai
        ├── copilot.html       Microsoft Copilot
        ├── perplexity.html    Perplexity AI
        ├── midjourney.html    Midjourney
        ├── dalle3.html        DALL-E 3
        ├── adobe-firefly.html Adobe Firefly
        ├── canva-ai.html      Canva AI
        ├── elevenlabs.html    ElevenLabs
        ├── notta.html         Notta
        └── notebooklm.html    Google NotebookLM
```

---

## 2. 各ページのワイヤーフレーム概要

### `/` — トップ

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | ロゴ ＋ グローバルナビ（M3 / M1 / M2） |
| 2 | ヒーロー | キャッチコピー・サブコピー・CTAボタン2つ（M3へ / M1へ） |
| 3 | 3サービスカード | M3・M1・M2 の説明カード（各ページへリンク） |
| 4 | フッター | コピーライト |

---

### `/apply.html` — 無料相談・応募ページ

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「まず無料で相談する」 |
| 3 | 対象者説明 | こんな方向け（箇条書き） |
| 4 | 申し込みフォーム | Googleフォーム埋め込み |
| 5 | フッター | 共通フッター |

---

### `/m1/` — M1 設計書Bot

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「Claudeに話しかけると設計書が出てくる」 |
| 3 | 基礎版カード | 説明 ＋ Claude Projectsリンク |
| 4 | 選択式版カード | 説明 ＋ Claude Projectsリンク |
| 5 | 次のステップ誘導 | M2へのクロスリンク |
| 6 | フッター | 共通フッター |

---

### `/m2/` — M2 AIパック

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「受け取ったら即動かせるAI指示文セット」 |
| 3 | 社労士向けパック | セット内容 ＋ Google Driveリンク |
| 4 | 追加予定パック | プレースホルダー（他業種） |
| 5 | 次のステップ誘導 | M3へのクロスリンク |
| 6 | フッター | 共通フッター |

---

### `/m3/` — M3 学ぶ（トップ）

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「AIを使いこなす力を身につける」 |
| 3 | コンテンツカード群 | 初めてのClaude Code / 比較表 / プロンプト集 / ツール紹介 / ニュース / 道場 |
| 4 | フッター | 共通フッター |

---

### `/m3/compare.html` — AIツール比較表

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「ChatGPT / Gemini / Claude / Copilot 比較表」 |
| 3 | 比較テーブル | 料金・日本語精度・主な用途・特徴 |
| 4 | 各ツール詳細リンク | /m3/tools/ 各ページへ |
| 5 | フッター | 共通フッター |

---

### `/m3/prompts.html` — プロンプト集

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「コピーして使えるプロンプト集」 |
| 3 | カテゴリナビ | 業務別タブ or アンカーリンク |
| 4 | プロンプト一覧 | 各プロンプト ＋ コピーボタン |
| 5 | フッター | 共通フッター |

---

### `/m3/news.html` — AI最新ニュース

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「AI最新ニュース」 |
| 3 | ニュース一覧 | 日付・タイトル・要約（週次更新） |
| 4 | フッター | 共通フッター |

---

### `/m3/claude-code.html` — 初めてのClaude Code

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「初めてのClaude Code」 |
| 3 | ステップ解説 | インストール → 初回起動 → 動作確認（番号付きステップ） |
| 4 | FAQ | 詰まりポイントのQ&A |
| 5 | 次のステップ誘導 | M1 設計書Botへ |
| 6 | フッター | 共通フッター |

---

### `/m3/dojo.html` — 特命AI集中道場

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「特命AI集中道場」 |
| 3 | プログラム概要 | 期間・内容・対象者 |
| 4 | カリキュラム | ステップ別コンテンツ |
| 5 | 申し込みCTA | /apply.html へ誘導 |
| 6 | フッター | 共通フッター |

---

### `/m3/webinar.html` — ウェビナーアーカイブ

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「ウェビナーアーカイブ」 |
| 3 | ウェビナー一覧 | 日付・テーマ・動画埋め込み or リンク |
| 4 | 次回予告 | 次回開催案内 |
| 5 | フッター | 共通フッター |

---

### `/m3/room.html` — 特命AI室

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「特命AI室」 |
| 3 | サービス説明 | 概要・特典・参加条件 |
| 4 | 参加CTA | /apply.html へ誘導 |
| 5 | フッター | 共通フッター |

---

### `/m3/tools/` — AIツール紹介（一覧）

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ページタイトル | 「AIツール紹介」 |
| 3 | カテゴリフィルター | チャット系 / 画像生成 / 動画生成 / 文字起こし 等 |
| 4 | ツールカード一覧 | 各ツール：名前・用途・料金・詳細ページへリンク |
| 5 | フッター | 共通フッター |

---

### `/m3/tools/{tool}.html` — 各AIツール詳細ページ（共通構成）

| # | ブロック | 内容 |
|---|---------|------|
| 1 | ヘッダー | 共通ヘッダー |
| 2 | ツール名 ＋ ひとこと説明 | — |
| 3 | 基本情報 | 料金プラン・対応言語・公式リンク |
| 4 | 主な機能 | 機能リスト or カード |
| 5 | こんな人向け | ユースケース |
| 6 | 関連ツール | 比較対象ツールへのリンク |
| 7 | 比較表へ戻る | /m3/compare.html へ |
| 8 | フッター | 共通フッター |

対象ツール：ChatGPT / Gemini / Claude.ai / Microsoft Copilot / Perplexity AI / Midjourney / DALL-E 3 / Adobe Firefly / Canva AI / ElevenLabs / Notta / Google NotebookLM

---

## 3. ページ間の動線ルール

### グローバルナビ（全ページ共通）

```
[Do Lab AI ロゴ] → /
[学ぶ（M3）]    → /m3/
[設計書Bot（M1)] → /m1/
[AIパック（M2）] → /m2/
```

### メイン動線（ユーザー行動フロー）

```
/ (トップ)
  ├─ [まずM3で学ぶ] → /m3/
  │    ├─ [初めてのClaude Code] → /m3/claude-code.html
  │    │    └─ [M1を使ってみる] → /m1/
  │    ├─ [AIツール比較表] → /m3/compare.html
  │    │    └─ 各ツール詳細 → /m3/tools/{tool}.html
  │    ├─ [AIツール紹介] → /m3/tools/
  │    ├─ [プロンプト集] → /m3/prompts.html
  │    ├─ [特命AI集中道場] → /m3/dojo.html → /apply.html
  │    └─ [特命AI室] → /m3/room.html → /apply.html
  │
  └─ [設計書Botを使う] → /m1/
       └─ [設計書ができたら] → /m2/
            └─ [改造で詰まったら] → /m3/
```

### クロスリンク誘導ルール

| 遷移元 | 誘導先 | 理由 |
|--------|--------|------|
| /m3/claude-code.html | /m1/ | 学んだ次に実践してもらう |
| /m1/ | /m2/ | 設計書→パック受け取りのフロー |
| /m2/ | /m3/ | 改造サポートのため |
| /m3/dojo.html | /apply.html | 道場への申し込み |
| /m3/room.html | /apply.html | 特命AI室への申し込み |
| /m3/tools/{tool}.html | /m3/compare.html | 比較文脈に戻す |
| /m3/compare.html | /m3/tools/{tool}.html | 詳細確認への遷移 |

### CTAボタン配置ルール

- 各ページに最低1つ「次アクションのCTA」を設置する
- CTAはページ末尾（フッター直前）にも再掲する
- 申し込み系CTAはすべて `/apply.html` へ集約する

---

## 4. フォルダ構成（完成形）

```
dolab-ai/
├── index.html
├── apply.html
├── 404.html
├── sitemap.xml
├── robots.txt
├── assets/
│   └── style.css
├── m1/
│   └── index.html
├── m2/
│   └── index.html
└── m3/
    ├── index.html
    ├── compare.html
    ├── prompts.html
    ├── news.html
    ├── claude-code.html
    ├── dojo.html
    ├── webinar.html
    ├── room.html
    └── tools/
        ├── index.html
        ├── chatgpt.html
        ├── gemini.html
        ├── claude.html
        ├── copilot.html
        ├── perplexity.html
        ├── midjourney.html
        ├── dalle3.html
        ├── adobe-firefly.html
        ├── canva-ai.html
        ├── elevenlabs.html
        ├── notta.html
        └── notebooklm.html
```
