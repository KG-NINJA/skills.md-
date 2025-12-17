# SKILL.md Generator (HTML Form)

このリポジトリは、**Codex / GPT Agent / AGENTS.md と組み合わせて使うための  
「壊れない SKILL.md を必ず生成できる HTML フォーム」**です。

SKILL.md を手書きすると起きがちな、

- YAML フロントマターの崩壊
- name / description の書き忘れ
- Markdown 構造ミスによる読み込み失敗

といった問題を防ぐことを目的としています。

---

## 目的

- **SKILL.md の構造を完全固定**
- 人間は「意味」だけ入力
- 出力はそのまま `skills/*.md` に配置可能
- Codex / GPT Agent / AGENTS.md で確実に解釈される

つまり、

> 「書式で失敗しない Skill 定義」

を実現するためのツールです。

---

## 想定ユースケース

- Codex 用 skills を量産したい
- AGENTS.md から切り替え可能な Skill を整理したい
- GPT Agent に役割を安全に渡したい
- Skill 定義を他人に共有したい（再現性重視）

---

## ファイル構成

.
├─ index.html # SKILL.md 生成フォーム
└─ README.md # この説明

yaml
Copy code

※ フォームは **単一 HTML ファイル**で完結します。

---

## 使い方

### 1. フォームを開く

- ローカルで `index.html` を開く  
- もしくは GitHub Pages に配置してブラウザから開く

### 2. 各項目を入力

| 項目 | 内容 |
|---|---|
| Skill name | skills/*.md の識別子 |
| Description | この Skill を「いつ・何のために」使うか |
| Instructions | AI にやらせたい具体的な振る舞い |

※ 書式や YAML を意識する必要はありません。

### 3. 「SKILL.md を生成」ボタンを押す

画面下部に **完成した SKILL.md** が表示されます。

### 4. コピペして配置

skills/your-skill-name.md

yaml
Copy code

として保存すれば完了です。

---

## 出力フォーマット

出力される SKILL.md は以下の構造を**必ず保証**します。

```md
---
name: your-skill-name
description: Description text here
---

# Instructions

- Instruction 1
- Instruction 2
