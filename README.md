# ifLink NEXT — 共創DX人材育成OS

異業種をつなぎ、IF-THEN モジュールで未来を共創するプラットフォームのデモ実装。
**Premium Edition v2.3 — GitHub Pages Ready**

![hero](assets/images/hero.jpg)

## ✨ 主な機能

- 🏠 **HOME / ダッシュボード** — KPI ステータス・推奨テーマ・最新ニュース
- 📇 **カードホルダー** — IF / THEN / ASSET / MENTOR をカテゴリ・キーワード絞り込み
- 📝 **モジュール登録** — 自社の強みを IF / THEN / ASSET としてカード化
- ⚡ **共創ビルダー** — IF×THEN×ASSET×MENTOR を組み合わせて PoC 提案を即時生成
  - **ドラッグ&ドロップ対応** (PC + タッチ)
  - **過去マッチング DB** から類似ソリューションをアニメーション表示
- 🛒 **マーケットプレイス** — モジュール売買・Amazon Pay 連携想定
- 👔 **メンターページ** — 事業開発 / 知財 / 製造の専門家ネットワーク
- 🌐 **共創共有 / コミュニティ** — プロジェクト共有・SNS連携・スコアリング
- 📊 **分析・レポート** — KPI / 業界別ドーナツ / 折れ線 / ヒートマップ
- 💎 **プレミアム機能** — IPガード / クローズドルーム / メンターアバター ほか

## 🌐 多言語対応

右上の言語スイッチで **日本語 / English / 中文** を切替できます。

## 🤖 AI API 連携 (OpenAI / Gemini)

右上「AI: OFF」をクリックして API キーを設定すると、共創ビルダーが**実 AI による PoC 提案**を生成します。

- 対応プロバイダー: OpenAI (`gpt-4o-mini` / `gpt-4o`), Google Gemini (`gemini-1.5-flash`)
- API キーは **ブラウザの LocalStorage にのみ保存**、外部送信なし

## 💾 LocalStorage 永続化

以下の状態がブラウザに保存され、リロード後も復元されます:

- 選択中言語 / EX POINT / スロット投入状態 / サウンドON-OFF
- フィルター・ハンドタブ位置
- ユーザー登録カスタムカード
- API 設定

## 📁 ファイル構成

```
.
├── index.html           # メインアプリ (112KB)
├── assets/
│   └── images/          # 画像アセット 21点 + ロゴ (合計 1.65MB)
│       ├── logo.svg
│       ├── hero.jpg
│       ├── dashboard.jpg
│       ├── if-001.jpg ... if-004.jpg
│       ├── th-001.jpg ... th-004.jpg
│       ├── as-001.jpg ... as-004.jpg
│       └── mentor-1.jpg ... mentor-3.jpg
├── .nojekyll            # Jekyll処理を無効化
├── .gitignore
└── README.md
```

## 🚀 GitHub Pages 公開手順

### 1. リポジトリ作成

```bash
git init
git add .
git commit -m "Initial commit: ifLink NEXT v2.3"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

### 2. GitHub Pages 有効化

1. リポジトリの **Settings** → **Pages**
2. **Source**: `Deploy from a branch`
3. **Branch**: `main` / `(root)` → **Save**

数分後に `https://<your-username>.github.io/<repo-name>/` で公開されます。

### 3. 動作確認

- ヒーロー画像・カード画像が正しく表示されること
- 言語スイッチで JA / EN / 中 切替動作
- 共創ビルダーでドラッグ&ドロップ操作
- API 設定モーダルで AI 連携設定保存

## 🛠 ローカルプレビュー

ファイルを直接ブラウザで開いても動作しますが、推奨はローカル HTTP サーバー経由です。

```bash
# Python 3
python3 -m http.server 8000
# → http://localhost:8000/

# Node.js
npx serve .
```

## 📐 技術仕様

- **単一HTML / 単一JS / 単一CSS** (フレームワーク不使用)
- レスポンシブ対応 (1100px / 820px / 560px)
- グラスモーフィズム × シルバーブルーメタリック デザイン
- HTML5 Drag&Drop API + 独自 Touch ハンドラ
- WebAudio API (操作SE)
- LocalStorage / Fetch API
- 外部依存: なし

## 🎨 デザインシステム

| 要素 | 値 |
|---|---|
| プライマリ | `#0d7df0` (Blue) |
| アクセント | `#13d6ff` (Cyan) |
| ベース | シルバー × ブルーメタリック グラデ |
| フォント | Hiragino Sans / Yu Gothic UI / Meiryo |
| 角丸 | 12px / 18px / 24px |
| グロー | `0 0 22px rgba(0,174,255,.55)` |

## 📝 ライセンス

このデモは内部レビュー / 提案用途を想定しています。商用利用前にライセンスを確認してください。

---

**© 2026 ifLink NEXT — IF-THEN Innovation OS**
