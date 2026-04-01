# claude-in-ppt-consulting

**Consulting-style instructions & skills for Claude in PPT**  
MBBスタイルのコンサルライクな資料を Claude in PPT で作成するための Instructions とスキル集です。

> ⚠️ This is an unofficial prompt set, not affiliated with or endorsed by Anthropic.

---

## 概要 / Overview

外資系コンサルのスライドを参考に、以下の方針で資料作成を行う Instructions とスキルを提供します。

- シンプル・プロフェッショナルなデザイン（黒・白・グレー基調）
- 論理的なスライド構成（章番号・目次・メッセージライン）
- スライドマスタを尊重したフォント・レイアウト管理
- ネイティブオブジェクト優先（アイコン・矢印・表）

## ファイル構成 / Files

```
claude-in-ppt-consulting/
├── README.md
├── LICENSE
├── instructions.md         # Instructions欄に貼り付けるプロンプト
├── template.potx           # スライドマスタ入りテンプレート
└── skills/
    ├── update-toc/
    │   └── SKILL.md        # /update-toc : 目次スライドを自動生成・更新
    └── apply-layout/
        └── SKILL.md        # /apply-layout : レイアウト自動適用
```
## 動作環境 / Requirements

| | 推奨 | 最低限 |
|---|---|---|
| プラン | Claude Max（Opus） | Claude Pro |
| モデル | claude-opus-4 | claude-sonnet-4 |

> スライド生成・スキル実行はトークン消費が大きいため、
> Claude Pro 以上を推奨します。Max プランの Opus モデルが最も安定します。

## 使い方 / Usage

### 1. テンプレートを開く

`template.potx` をダブルクリックして新規 PowerPoint ファイルを作成します。  
既存のスライドマスタを使う場合はこの手順をスキップしてください。

### 2. Instructions を設定する

1. Claude in PPT を開く
2. Instructions 欄（設定アイコン → Instructions）を開く
3. `prompt.md` の内容をすべてコピーして貼り付ける

![Instructions の設定方法（スクリーンショット準備中）]()

### 3. スキルを追加する（任意）

1. `skills/update-toc/` フォルダをまるごと claude.ai にアップロードする
2. 同様に `skills/apply-layout/` もアップロードする
3. スライドを選択した状態でコマンドを入力する

| コマンド | 内容 |
|---|---|
| `/update-toc` | 目次スライドを自動生成・更新する |
| `/apply-layout` | 選択中のスライドをスライドマスタに従いリデザインする |

### 4. スライドを作成する

Instructions を設定した状態で、Claude in PPT に自然言語で指示するだけです。

```
例：
「競合分析のスライドを作って。3社比較で、評価軸は価格・品質・サポートの3つ。」
```

## 既知の制限・WIP

- [ ] サンプルスクリーンショットの追加
- [ ] 英語版 Instructions の提供
- [ ] スキルの追加（図解自動生成など）

Instructions・スキルともに改善中です。フィードバックは [Issues](../../issues) からお気軽にどうぞ。

## ライセンス / License

MIT License © 2026 iCON Inc. (株式会社iCON)

本リポジトリのプロンプト・スキルファイルに適用されます。  
Claude in PPT および Claude は Anthropic の製品です。本リポジトリは Anthropic とは無関係です。
