# api-setup-practice

## 概要

COACHTECH 教材 Tutorial 11-1「API開発環境の構築と疎通確認」で作成した成果物です。

API 開発環境を構築し、 /api/hello エンドポイントを介して JSON レスポンスを返す REST API の疎通確認を実施したアプリケーションです。

## 使用技術

- PHP 8.2
- Laravel 10.x
- REST API（JSONレスポンス）
- Postman（動作確認）

## 学んだこと

- routes/api.php を使用した API ルーティングの設定方法と、自動付与される /api プレフィックスの仕組み
- response()->json() ヘルパー関数を使用した構造化 JSON レスポンスの返却方法
- Postmanを使用した API リクエスト送信とレスポンス確認

## 動作確認

- sail up -d で環境の起動
- sail artisan migrate:fresh --seed でデータベースを初期化
- Postmanで GET http://localhost/api/hello にアクセス
- ステータスコード 200 OK と共に、以下の JSON レスポンスが返却されることを確認
  json
  {
  "message": "Hello, API!"
  }
