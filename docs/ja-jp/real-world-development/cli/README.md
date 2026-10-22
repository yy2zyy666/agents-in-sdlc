---
slug: ja-jp/real-world-development/cli
title: "GitHub Copilot CLI"
description: "Copilot CLI のモード、カスタマイズ、MCP ツール、pull request の自動化を学びながら、Tailspin Toys の 2 つの変更を実装、検証、提供します。"
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

**[GitHub Copilot CLI][about-copilot-cli]** は、エージェント型コーディング アシスタントの GitHub Copilot をターミナルで利用できるようにします。コードベースを探索し、コードを生成し、コマンドを実行し、外部ツールに接続できます。すべてコマンド ラインから行えるため、グラフィカル エディターに切り替えずに作業を続けられます。

このワークショップでは、Tailspin Toys を使った一連のワークフローを進めます。

1. GitHub Codespaces でプロジェクトを準備し、Copilot CLI をインストールして基本を確認します。
2. 星評価を表示する小さな変更を加え、ブラウザーで確認して、最初の pull request (PR) を手動でマージします。
3. フィルターの issue から始め、Plan モードで方針を決め、Autopilot モードで実装し、Interactive モードでレビューします。
4. リポジトリの指示を更新し、フィルターの作業に適用します。
5. 既存の `quality-checks` skill をカスタマイズして、プロジェクトのチェックに使います。
6. Playwright Model Context Protocol (MCP) サーバーを追加して、ブラウザーでフィルターの動作を確認します。
7. quality assurance (QA) カスタム エージェントを作成し、要件、カバレッジ、検証の証拠をレビューします。
8. フィルターの変更全体を確認し、フィルター PR に Agent Merge を使います。
9. コンテキスト、モデル、共有、任意のクラウド委任に役立つスラッシュ コマンドを確認します。

ワークショップに集中できるよう、PR は 2 つ作成します。1 つ目は星評価、2 つ目は指示と skill の更新、QA プロファイル、テストを含むフィルターの変更です。フィルターと品質のワークフローでは同じ会話とブランチを使うため、各ツールを試しながら作業を積み重ねられます。

## レッスン

| レッスン | トピック | 説明 |
| ------ | ----- | ----------- |
| [0. 前提条件][ex0] | セットアップ | リポジトリと Codespace を作成します |
| [1. Copilot CLI のインストール][ex1] | インストール | Copilot CLI をインストールして認証し、基本を確認します |
| [2. 星評価の追加: 小さな改善][ex2] | 最初の変更 | 既存の評価と null の場合の表示を追加し、最初の PR をマージします |
| [3. エージェント モード: Plan と Autopilot][ex3] | エージェント モード | issue から機能を計画し、Autopilot で実装して Interactive モードでレビューします |
| [4. カスタム指示で Copilot をガイドする][ex4] | コンテキスト | 指示を確認、更新し、フィルターに適用します |
| [5. quality-checks skill のカスタマイズと使用][ex5] | 繰り返し可能なチェック | 既存の skill を確認し、レポート形式を変更して実行します |
| [6. Playwright MCP による機能の検証][ex6] | ブラウザーでの確認 | CLI で MCP を構成し、フィルターの動作を調べます |
| [7. QA エージェントの作成と使用][ex7] | 要件とカバレッジ | 専門プロファイルを作成して選択し、最終検証の証拠を収集します |
| [8. 機能 PR の作成とマージ][ex8] | レビューとマージ | 変更全体を確認し、PR を作成して Agent Merge を使います |
| [9. GitHub Copilot CLI のスラッシュ コマンド][ex9] | CLI 機能 | コンテキスト、モデル、共有、任意のクラウド エージェントへの委任を確認します |
| [10. まとめと次のステップ][ex10] | まとめ | ワークフロー、再利用可能なカスタマイズ、その他のリソースを確認します |
| [オプション: Foundry の導入][foundry] | ホスト型エージェント | モデルを準備し、カタログに基づくエージェントをデプロイして、Web サイトに接続します |

## 前提条件

このワークショップに参加する前に、次を準備してください。

- [ ] **Copilot Student、Pro、Pro+、Business、Enterprise** のいずれかの有効なプランがある GitHub アカウント
- [ ] リポジトリと Codespace を作成する権限
- [ ] ターミナルまたはコマンド ライン操作の基本的な知識

> [!TIP]
> 有料プランがありませんか。認証済みの学生は [GitHub Education][student-plan] を通じて GitHub Copilot を無料で利用できます。**Copilot Student** プランには、このワークショップで使用する agent、MCP、code review、Copilot CLI の機能が含まれています。

> [!NOTE]
> Copilot Business または Copilot Enterprise を使用している場合は、管理者が Copilot CLI を有効にしていることを確認してください。

## はじめる

**[前提条件から始める →][ex0]**

[about-copilot-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[student-plan]: https://github.com/education/students
[ex0]: 0-prerequisites/
[ex1]: 1-install-copilot-cli/
[ex2]: 2-add-star-rating/
[ex3]: 3-agent-modes/
[ex4]: 4-custom-instructions/
[ex5]: 5-agent-skills/
[ex6]: 6-mcp-playwright/
[ex7]: 7-qa-agent/
[ex8]: 8-create-pull-request/
[ex9]: 9-cli-power-tools/
[ex10]: 10-review/
[foundry]: 8-foundry-agent/
