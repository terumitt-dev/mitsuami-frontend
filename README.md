# mitsuami-frontend

ミツアミ（Mitsuami）は、出自の違う3つのAIが合議して答える、球体の話しかけガジェットです。
名前は「三つ編み」から取りました。3本を編んで1本にするように、3つの意見をそれぞれの形のまま編み合わせて、1つの答えにします。

このリポジトリは、ミツアミの画面です。質問を送り、3つのユニットの賛否と、多数決の結論を表示します。

## 現在の状態

Vite と React の雛形だけがあります。表示されるのは Vite の初期画面で、ミツアミの画面はこれから作ります。

## 技術

- Node.js 26
- React 19 / TypeScript / Vite

## 起動

Docker が必要です。

```sh
docker compose up --build
```

起動したら http://localhost:5173 を開きます。

## 関連リポジトリ

| リポジトリ | 役割 |
|---|---|
| [mitsuami-backend](https://github.com/terumitt-dev/mitsuami-backend) | 司令塔。3つのユニットに質問を送り、多数決で結論を返す（Rails） |
| [mitsuami-frontend](https://github.com/terumitt-dev/mitsuami-frontend) | 画面。質問を送り、賛否と結論を表示する（React） |
| [mitsuami-unit-python](https://github.com/terumitt-dev/mitsuami-unit-python) | ユニット「科学者」（Python、FastAPI、PyTorch） |
| [mitsuami-unit-go](https://github.com/terumitt-dev/mitsuami-unit-go) | ユニット「母」（Go、net/http、llama.cpp） |
| [mitsuami-unit-rust](https://github.com/terumitt-dev/mitsuami-unit-rust) | ユニット「女」（Rust、axum、ONNX Runtime） |
| mitsuami-personas（非公開） | 人格の定義、学習データ、追加学習と変換のスクリプト |
