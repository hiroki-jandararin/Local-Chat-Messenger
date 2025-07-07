# 📨 Local Chat Messenger

Local Chat Messenger は、UNIXドメインソケット（Datagram）を用いた、**ローカル環境専用のチャット風通信アプリ**です。クライアントは「名前」または「住所」のいずれかを選択し、サーバがランダムな偽データ（Fakerによる）を返すシンプルな仕組みになっています。

## 📦 機能概要

- UNIXドメインソケット（DGRAM）によるクライアント・サーバ通信
- Fakerライブラリによってランダムな名前・住所を生成
- 入力が無効な場合には適切なバリデーションメッセージを返却
- 完全ローカルで動作し、インターネット接続不要

## 🏗️ 使用技術

- Python 3
- Faker ライブラリ
- UNIXドメインソケット (AF_UNIX, SOCK_DGRAM)
- WSL2 / Linux 互換環境推奨

## 🔧 セットアップ方法

```bash
# 仮想環境の作成（任意）
python3 -m venv .venv
source .venv/bin/activate

# Fakerのインストール
pip install Faker
```

---

## 🚀 実行方法

### 1. サーバを起動

```bash
python3 server.py
```
---

### 2. クライアントを起動（別のターミナル）

```bash
python3 server.py
```
### 入力例：
```bash
表示したいデータの数字を選択してください。1. 名前, 2. 住所 :
```

## 🗂️ ファイル構成

```bash
localMessenger/
├── client.py       # クライアントコード（入力と受信処理）
├── server.py       # サーバコード（受信と応答処理）
├── README.md       # このファイル
└── .venv/          # 仮想環境（.gitignore 推奨）
```


