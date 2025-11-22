# minihandson_zerto_to_snow

Snowflakeを使用したTasty Bytesデータ分析プロジェクト

## 概要
POS、顧客ロイヤルティ、トラックレビューデータを取り込み、ビジネス分析を支援するデータパイプラインです。

## 構成
- **setup.sql**: データベース、スキーマ、ロール、権限設定
- **api_integration.sql**: GitHubAPI統合設定
- **notebook/**: Jupyter形式のデータ処理パイプライン
- **streamlit/**: 顧客分析ダッシュボード

## 主な機能
- マルチレイヤーアーキテクチャ (Raw / Harmonized / Analytics / Semantic)
- データパイプラインの構築
- Streamlitダッシュボードで顧客ロイヤルティ可視化

## データスキーマ
### Raw層
- **raw_pos**: POS取引データ (トラック、メニュー、注文情報)
- **raw_customer**: 顧客ロイヤルティプログラムデータ
- **raw_support**: トラックレビューと顧客ボイスデータ

### Harmonized層
正規化され結合されたビジネス用ビュー

### Analytics層
分析・可視化向けの最終ビュー

### Semantic層
Cortex Analyst用のセマンティックモデル

## セットアップ
1. `setup.sql`を実行してインフラストラクチャを構築
2. `api_integration.sql`でGitHub統合を設定
3. Notebookでデータパイプラインを実行
4. Streamlitダッシュボードで分析結果を可視化

## ダッシュボード機能
Streamlit アプリケーションは以下を提供：
- 国・売上範囲によるフィルタリング
- 顧客分布と売上分析
- 売上トップ顧客ランキング
- 訪問店舗数ランキング
- 詳細顧客データテーブル