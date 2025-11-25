# minihandson_zerto_to_snow

Snowflakeを使用したTasty Bytesデータ分析プロジェクト

## 概要
POS、顧客ロイヤルティ、トラックレビューデータを取り込み、ビジネス分析を支援するSnowflakeのハンズオンプロジェクトです。
データパイプラインの構築からBI・AI活用まで、Snowflakeの主要機能を体験できます。

## ハンズオンコンテンツ

### 1. データパイプライン (`notebook/1_Simple_Data_Pipeline.ipynb`)
半構造化データ、Dynamic Table、Taskを使用したデータパイプラインの構築を学びます。

**学習内容：**
- 半構造化データ（JSON）の取り込みと処理
- Dynamic Tableによる自動データ更新
- Taskを使ったスケジューリングとパイプライン自動化

### 2. データコラボレーション (`notebook/2_Data_Share.ipynb`)
データシェアリング機能とMarketPlaceを活用したデータ共有を体験します。

**学習内容：**
- データシェアリングによる組織間データ連携
- Snowflake MarketPlaceからのデータ取得
- セキュアなデータコラボレーション

### 3. BI＆AI (`streamlit/3_streamlit_dashboard.py`)
StreamlitダッシュボードとSnowflake Intelligenceを使った分析とAI活用を実践します。

**学習内容：**
- Streamlitによるインタラクティブダッシュボード開発
- Snowflake Intelligenceを活用したデータ分析
- 顧客ロイヤルティの可視化とインサイト抽出

## プロジェクト構成
- **setup.sql**: データベース、スキーマ、ロール、権限設定
- **api_integration.sql**: GitHubAPI統合設定
- **notebook/**: ハンズオン用Jupyter Notebookファイル
  - `1_Simple_Data_Pipeline.ipynb`: データパイプライン構築
  - `2_Data_Share.ipynb`: データコラボレーション
- **streamlit/**: BI＆AIダッシュボード
  - `3_streamlit_dashboard.py`: Streamlitアプリケーション
- **Cortex_AI/**: Cortex Analyst用セマンティックモデル

## データアーキテクチャ
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

## セットアップ手順
1. `setup.sql`を実行してSnowflakeインフラストラクチャを構築
2. `api_integration.sql`でGitHub統合を設定
3. ハンズオン1: `notebook/1_Simple_Data_Pipeline.ipynb`でデータパイプラインを構築
4. ハンズオン2: `notebook/2_Data_Share.ipynb`でデータ共有を体験
5. ハンズオン3: `streamlit/3_streamlit_dashboard.py`でダッシュボードを作成・分析

## ダッシュボード機能
Streamlit アプリケーションは以下を提供：
- 国・売上範囲によるフィルタリング
- 顧客分布と売上分析
- 売上トップ顧客ランキング
- 訪問店舗数ランキング
- 詳細顧客データテーブル
- Snowflake Intelligence統合
