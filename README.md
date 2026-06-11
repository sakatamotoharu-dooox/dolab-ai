# Do Lab AI

中小企業向けAI活用メンバーシッププラットフォーム。  
外注も高額SaaSも不要。業務改善AIを自分で作り・動かし・改造できる人を育てます。

**公開URL**: https://sakatamotoharu-dooox.github.io/dolab-ai/

---

## URL設計

| URL | ページ | 対応タスク |
|-----|--------|-----------|
| `/` | ダッシュボード（トップ） | UI-02 |
| `/m3/` | M3 学ぶ トップ | UI-01 |
| `/m3/claude-code.html` | 初めてのClaude Code | M3-C01 |
| `/m3/compare.html` | AIツール比較表 | M3-C02 |
| `/m3/prompts.html` | プロンプト集 | M3-C03 |
| `/m3/tools.html` | AIツール紹介 | M3-C04 |
| `/m3/news.html` | AI最新ニュース | M3-C05 |
| `/m3/dojo.html` | 特命AI集中道場案内 | M3-C08 |
| `/m3/webinar.html` | AIウェビナー案内 | M3-C08 |
| `/m1/` | M1 設計書Bot | UI-03 |
| `/m2/` | M2 AIパック | UI-04 |

---

## フォルダ構成

```
dolab-ai/
├── index.html          # トップ（ダッシュボード）
├── assets/
│   └── style.css       # 共通スタイル（GP-06）
├── m1/
│   └── index.html      # M1 設計書Bot
├── m2/
│   └── index.html      # M2 AIパック
└── m3/
    ├── index.html      # M3 トップ
    ├── claude-code.html
    ├── compare.html
    ├── prompts.html
    ├── tools.html
    ├── news.html
    ├── dojo.html
    └── webinar.html
```

---

## デプロイ方法

HTMLファイルを編集後、pushするだけで自動公開されます。

```bash
git add .
git commit -m "update: ページ名"
git push
```

GitHub Pages の反映には最大5分かかる場合があります。

---

## 開発ガイド

ページの追加・更新手順（環境構築・ファイル構成・ローカル確認・デプロイ・コーディング規約）は、開発ガイドにまとめています。

- 📄 [DEVELOPMENT.md](DEVELOPMENT.md)（Markdown版）
- 🖥 [docs/development-guide.html](docs/development-guide.html)（ブラウザ閲覧用の整形版）
