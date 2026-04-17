# codex-config

## 日本語

Codex やコーディングエージェントに適用する作業ルールをまとめた設定用リポジトリです。実装前の要件確認、進捗ログ、ドキュメント更新、競合時の優先順位、ネットワーク権限の扱いなどを `AGENTS.md` に定義しています。

### 構成

- `AGENTS.md`: エージェント向けの必須作業ルール

### 使い方

`AGENTS.md` を、エージェントの作業ルールを統一したいリポジトリにコピーまたは移植して使います。

### 含まれる方針

- 要件ファイルを source of truth として扱う
- `workflow.md` と `progress.md` を維持する
- 競合時の優先順位を明確にする
- 実装単位ごとに commit する
- ネットワークや install の失敗時は権限付き再実行を確認する
- サブエージェント利用時は範囲と結果を記録する

### 注意

このリポジトリは設定・ドキュメント用です。アプリケーションコードやビルド手順は含みません。

## English

This repository stores reusable operating rules for Codex and coding agents.

### Structure

- `AGENTS.md`: mandatory instructions for coding agents

### Usage

Copy or adapt `AGENTS.md` into repositories where agent behavior needs to be standardized.

### Covered Policies

- Treat requirement files as the source of truth
- Maintain `workflow.md` and `progress.md`
- Define conflict priority
- Commit meaningful units of work
- Retry network/install failures with escalation when needed
- Record sub-agent scope and outcomes

### Notes

This repository is configuration/documentation only. It does not include application code or a build step.
