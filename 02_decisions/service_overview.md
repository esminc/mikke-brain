# mikke サービス概要

> **このファイルの位置づけ:** mikkeに関する意思決定・仕様の起点。各領域の詳細は参照先ファイルを確認すること。

---

## 1. mikkeとは

「今日も見っけた"いいな"を持ち寄る場所」

ポジティブなことを伝え合うことが"ごく普通"の状態を作るための、Slackチャンネル（#its-mikke）を核とした取り組み。設計思想・ターゲット・価値提供の詳細は `01_core/` を参照。

---

## 2. 自律運用の設計

mikkeが特定の誰かの頑張りに依存せず機能するための仕組みは、以下の方程式に基づいて設計されている。

> **mikkeへの投稿 = 意欲(M) × 手軽さ(A) × きっかけ(P)**

行動心理学（BJ Fogg Behavior Model）をベースとする。3要素は掛け算の関係にあり、どれか一つでもゼロになると投稿は生まれない。

| 要素 | 担う仕組み | 詳細 |
|------|-----------|------|
| **意欲(M)** | 共感リアクション文化 | [service_operations_reaction.md](service_operations_reaction.md) |
| **手軽さ(A)** | 匿名投稿機能 | [service_operations_anonymous.md](service_operations_anonymous.md) |
| **手軽さ(A)** | みっけん引用投稿 | [service_operations_quote.md](service_operations_quote.md) |
| **きっかけ(P)** | みっけんメッセージ | [service_operations_pacemaker.md](service_operations_pacemaker.md) |

---

## 3. オンボーディング

新規参加者がmikkeの文脈をすぐに把握できるよう、参加時に自動案内を行う。

| 仕組み | 詳細 |
|--------|------|
| ウェルカムメッセージ | [service_onboarding_welcome.md](service_onboarding_welcome.md) |

---

## 4. 設計原則

| 原則 | 内容 |
|------|------|
| **最小介入** | オーナーの月次負荷がほぼゼロになるよう設計する |
| **依存の分散** | 1つの仕組みが機能しなくても残りで補完できる |
| **文化への整合** | 仕組みはmikkeの「気軽さ・自由さ・強制しない」価値観を壊さないこと |
