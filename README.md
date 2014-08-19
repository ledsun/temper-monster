# このプロジェクトは何か？

温度センサーの監視情報をモニタリングするWebアプリケーションシステムです。

- 外出中の部屋の温度を外出先から確認
- MQTTを使ったセンサー監視システムのサンプル実装

## システム構成
- Raspberry Pi
    - 温度センサー
        - USBRH-FG
    - Raspbian
    - MQTT publisher
        - golang
- Node.js サーバー
    - MQTT Server
        - 転送はしない
        - レコードをMongoDBに貯める
    - Web UI
        - Vue.jsを使う
        - グラフ表示
- MongoDB

## デプロイ先
Herokuを想定

## 開発環境
- Raspberry PiのシミュレータとしてVagrantを使用
- クライアントはgoをARM向けにクロスコンパイルして配置
- サーバーはMac OS X 上で直接実装
