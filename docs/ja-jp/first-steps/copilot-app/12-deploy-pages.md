---
title: "レッスン 12 - GitHub Pages でサイトをデプロイする"
description: "GitHub Copilot app で Pages ワークフローを構成して pull request をレビューし、公開された Space Quiz を確認します。"
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Space Quiz を GitHub Pages にデプロイして、公開サイトとして利用できるようにします。Copilot はワークフローを準備してデプロイを案内できますが、変更をレビューし、サイトが公開されたことを確認するのはユーザーの責任です。

このレッスンでは、次のことを行います。

- Copilot に GitHub Pages のデプロイを構成するよう依頼します。
- マージする前にワークフローと pull request をレビューします。
- デプロイの進行状況を確認し、公開されたサイトを検証します。

## シナリオ

Space Quiz はすでに GitHub リポジトリにありますが、まだ簡単に試せる方法がありません。1 ファイルのサイトを GitHub Pages で公開すると、サーバーやランタイム依存関係を追加せずに公開 URL から利用できます。

## Copilot にサイトのデプロイを依頼する

`space-quiz` の Copilot app セッションで、次のプロンプトを送信します。

```plaintext
このリポジトリで GitHub Pages を有効にしてください。必要であれば Web サイトをビルドし、GitHub Pages にデプロイする GitHub Actions ワークフローを作成してください。README がまだない場合は、アプリとローカルでの実行方法を説明する README を追加してください。これらの変更を含む pull request を作成し、必須のチェックに合格したらマージしてください。デプロイが成功するまで監視し、ライブ Web サイトの最終 URL を報告してください。Pages の有効化やマージの権限がない場合は、何を承認または実行する必要があるか正確に教えてください。サイトが公開されるまでは成功と報告しないでください。
```

![3 段階の図: space-quiz の pull request がマージされた状態、Build website・Upload artifact・Deploy to Pages のステップが成功した GitHub Actions Deploy website の実行、yourname.github.io/space-quiz/ で公開された Space Quiz。](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> このプロンプトは、エージェントに pull request の作成とマージ、およびリポジトリの Pages 設定の変更を依頼します。続行する前に、diff、デプロイ権限、GitHub の承認要求を確認してください。

## ワークフローをレビューしてデプロイを確認する

1. README がリポジトリに存在しない場合にのみ追加されたことを確認します。
2. ワークフローのビルドとデプロイの手順を含め、pull request の変更をレビューします。
3. 必須の pull request チェックに合格した後にのみマージします。
4. GitHub Actions のデプロイ実行が成功するまで確認します。
5. 報告された URL を開き、Space Quiz が表示されることを確認します。

エージェントが Pages を有効化したり pull request をマージしたりできない場合は、提示された具体的な手順に従ってください。デプロイが成功し、公開サイトが読み込まれるまで、タスクを完了したものとして扱わないでください。

## まとめと次のステップ

Space Quiz が公開サイトとして利用できるようになりました。エージェントの報告だけに頼らず、デプロイを確認できました。続けて[レッスン 13: 振り返りと次のステップ][next-lesson]に進みます。

[next-lesson]: ../13-review/
