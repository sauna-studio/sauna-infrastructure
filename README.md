# sauna-infrastructure
Sauna Studio infrastructure


## Scope

Terraform / Google Cloud Run / Cloud SQL PostgreSQL 18 / OpenTelemetry / Dockerの基盤コード。

## Architecture

業務データの正本はSauna APIとPostgreSQL。認証情報をTerraform state・plan・ログ・リポジトリに公開しない。

## Verification

実装後はterraform fmt -check -recursive / init -backend=false / validateを実行する。apply・本番デプロイ・課金リソース・広いIAM付与は明示承認まで実行しない。

初期PRは開発基盤のみを追加します。CIはRepository policy検査を実行し、業務機能の実装や動作検証はまだ含みません。

[AGENTS.md](AGENTS.md) と [CONTRIBUTING.md](CONTRIBUTING.md) に従い、Issueの依存関係を満たしてから独立Review Agentを並行起動して実装します。共通規則適用元: [sauna-studio/.github@075c6695309d](https://github.com/sauna-studio/.github/tree/075c6695309d28baad2dc1391d7d3821b81142cc)。
