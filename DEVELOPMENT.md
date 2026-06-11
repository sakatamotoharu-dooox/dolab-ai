# Do Lab AI 開発ガイド（ページの開発・更新手順）

Do Lab AI サイト（GitHub Pages）のページを**追加・更新する手順**をまとめた開発手順書です。
特に M3「学ぶ」の Cowork 系ページ（`m3/cowork.html` など）の制作を想定していますが、他ページも同じ流れで対応できます。

- **公開URL**: https://sakatamotoharu-dooox.github.io/dolab-ai/
- **リポジトリ**: `sakatamotoharu-dooox/dolab-ai`
- **想定読者**: 制作担当（専門的な開発経験がなくても追える粒度で記載）

---

## 1. 開発環境のセットアップ手順

### 必要なもの
- **Git**（バージョン管理）
- **テキストエディタ**（VS Code 推奨）
- **ブラウザ**（Google Chrome 推奨 ※PDF生成にも使用）
- **GitHubアカウント**（リポジトリへのアクセス権限。SSH鍵の登録を推奨）

### 手順

リポジトリを手元に複製し、最新の `main` に更新します。

▼ 実行コマンド

```bash
# 1. リポジトリをクローン（SSH）
git clone git@github.com:sakatamotoharu-dooox/dolab-ai.git
cd dolab-ai

# 2. 最新の main に更新（2回目以降）
git switch main
git pull
```

> ※ SSHが使えない場合はHTTPSクローンでも可：`git clone https://github.com/sakatamotoharu-dooox/dolab-ai.git`
> ※ ビルドツール・npm等は不要です（素のHTML/CSSサイトのため）。

---

## 2. ファイル構成・編集対象ファイル

```
dolab-ai/
├── index.html            # トップ（ダッシュボード）
├── assets/
│   └── style.css         # 共通デザインシステム ★全ページに影響
├── m1/index.html         # M1 設計書Bot（テーマ色: コーラル --m1）
├── m2/index.html         # M2 AIパック（テーマ色: オレンジ --m2）
└── m3/                   # M3 学ぶ（テーマ色: パープル --m3）
    ├── index.html        # M3トップ（カード一覧）★ページ追加時はここにカードを足す
    ├── claude-code.html
    ├── cowork.html          # Cowork 基本的な使い方
    ├── cowork-features.html # Cowork 機能と活用事例
    ├── tools/              # AIツール紹介ページ群（ChatGPT/Claude など）
    │   ├── index.html        # AIツール紹介トップ（一覧）
    │   └── chatgpt.html       # 例：ChatGPT 紹介
    └── （compare.html / prompts.html など）
```

### 編集対象の早見表
| やりたいこと | 編集するファイル |
|---|---|
| 新しいページを追加 | `m3/`（など該当ディレクトリ）に新規 `.html` を作成 |
| 一覧（M3トップ）に載せる | `m3/index.html` に `card c-m3` のカードを1つ追加 |
| AIツール紹介ページを追加 | `m3/tools/` に新規 `.html`、`m3/tools/index.html`（一覧）にも追記 |
| 既存ページの文言・見た目（そのページのみ） | 対象ページの `<style>` ブロック |
| サイト全体の共通デザイン | `assets/style.css` ★影響範囲が大きいので慎重に |

### URL設計・配置の方針
- ページは原則 **`/m3/xxx.html` のフラット配置**（README の URL 設計に準拠）。
- AIツール紹介ページは **`/m3/tools/` 配下**にまとめる（例：`/m3/tools/chatgpt.html`）。
- Cowork セクションの詳しいページ構成・URL設計・サイトマップ位置・導線は、設計ドキュメント **[docs/cowork-section-design.md](docs/cowork-section-design.md)** を参照（Issue #123）。

---

## 3. ローカル確認方法

公開前に、必ず手元のブラウザで表示を確認します。

- **方法A（手軽）**: 対象の `.html` をダブルクリック、またはブラウザにドラッグ＆ドロップ（`file://` で開く）
- **方法B（推奨）**: 簡易サーバを立てて確認（相対パス・リンクが本番に近い形で動く）
  ```bash
  python3 -m http.server 8000
  # → ブラウザで http://localhost:8000/m3/cowork.html を開く
  ```

### 確認ポイント
- ヘッダー／フッターが共通の見た目になっているか
- ページ内・ページ間のリンクが切れていないか
- スマホ幅（ウィンドウを狭める）でレイアウトが崩れないか（レスポンシブ）

---

## 4. デプロイ手順（push → GitHub Pages）

`main` ブランチへの変更が GitHub Pages で**自動公開**されます（反映に最大5分）。
**ブランチを切ってPR経由でマージする**運用を推奨します。次の 1〜7 の順で進めます。

1. **作業ブランチを作成する**
   例：`add-m3-xxx`
2. **ページを編集し、ローカルで表示を確認する**
   第3章の方法で確認する
3. **変更をコミットする**
   何を変えたか短くメッセージを書く
4. **GitHubへ push する**
5. **GitHub上でPRを作成する**
   `Compare & pull request`。対応Issueがあれば本文に `Closes #番号`（マージ時に自動クローズ）
6. **レビュー後にマージする**
   マージすると `main` に反映される
7. **数分後、公開URLで確認する**
   例：`https://sakatamotoharu-dooox.github.io/dolab-ai/m3/xxx.html`

▼ 実際のコマンド（ステップ 1〜4 のターミナル操作）

```bash
# 1. 作業ブランチを作成
git switch -c add-m3-xxx

# 2. 編集 → ローカルで表示確認（第3章）

# 3. 変更をコミット
git add m3/xxx.html m3/index.html
git commit -m "m3: ○○ページを追加"

# 4. GitHubへ push
git push -u origin add-m3-xxx
```

※ ステップ 5〜7（PR作成・マージ・公開確認）は GitHub の画面上での操作です。
※ `gh` コマンドが無い環境では、PRの作成だけブラウザで行います（push までは Git で完結）。

### （任意）PDF版を作る
配布用PDFが必要な場合、Google Chrome のヘッドレス機能で生成できます。
```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" \
  --headless --no-pdf-header-footer \
  --print-to-pdf="m3/xxx.pdf" \
  "file://$(pwd)/m3/xxx.html"
```
各ページには印刷用の `@media print` を用意しておくと、きれいなPDFになります。

---

## 5. コーディング規約・命名ルール

### ファイル・配置
- ファイル名は **半角英小文字＋ハイフン**（例：`cowork-features.html`）。日本語・スペースは不可。
- 配置先：学ぶ系は `m3/`、設計書Botは `m1/`、AIパックは `m2/`。
- 1ページ＝**1つのHTMLファイル**で作成する。

▼ 実行イメージ：正しい場所・名前でファイルを作る

```bash
# 学ぶ系のページは m3/ 配下に、半角英小文字＋ハイフンで作成
$ cd m3
$ touch cowork-features.html
→ m3/cowork-features.html を作成しました
```

### ブランチ・PR
- ブランチ名は内容がわかる英小文字＋ハイフン（例：`add-m3-cowork-features`）。
- コミットメッセージは日本語OK。「何を・どうしたか」を簡潔に書く。
- 1つのPR＝1つのまとまった変更。

▼ 実行イメージ：ブランチ作成 → コミット → push

```bash
# ① 内容がわかる名前でブランチを作成
$ git switch -c add-m3-cowork-features

# ② 変更をコミット（何を・どうしたか）
$ git add m3/cowork-features.html
$ git commit -m "m3: Cowork機能ページを追加"

# ③ push（このあと GitHub で PR を作成）
$ git push -u origin add-m3-cowork-features
```

---

## 付録：Issue対応の基本フロー

1. **Issueを確認** → 必要なら公式・事例などを追加調査
2. **ブランチ作成** → ページ作成/更新 → **ローカル確認**
3. **PR作成**（本文に `Closes #番号`）→ レビュー → **マージ** → 公開確認

> ※ 複数のPRが同じ `m3/index.html` を編集する場合、後からマージする方で**競合**が出ることがあります。1つマージするごとに最新 `main` に合わせて調整してください。

---

**作成**: Do Lab AI 開発ガイド ｜ 株式会社 Dooox
