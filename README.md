# SBOM-BC

## 環境構築

### 0. リリースの最新化
```bash
sudo apt update
sudo apt upgrade
sudo apt install -y build-essential libgmp3-dev
```

### 1. Gethのインストール
#### Go-langをインストール

```bash
# 最新版を公式よりダウンロード
wget https://go.dev/dl/go1.24.2.linux-amd64.tar.gz

# 展開
tar -C /usr/local/ -xvf go1.24.2.linux-amd64.tar.gz
```

#### パスの設定
~/.bashrc へ以下の内容を追加
```
export PATH=$PATH:/usr/local/go/bin
```

#### 編集の反映
```bash
source ~/.bashrc
```

#### 動作確認
```bash
go version
```

#### Gethのインストール
必要なパッケージのインストール
```bash
sudo apt update
sudo apt install -y build-essential git curl
```

```bash
# ソースコードのクローン
git clone https://github.com/ethereum/go-ethereum.git
cd go-ethereum

# ビルド
make geth

# バイナリをシステムに導入
sudo cp build/bin/geth /usr/local/bin/
```

#### 動作確認
```bash
# geth version
Geth
Version: 1.15.8-unstable
Git Commit: 21b035eb29f6489ffee66d8ee2451873bc96dd2d
Git Commit Date: 20250407
Architecture: amd64
Go Version: go1.24.2
Operating System: linux
GOPATH=
GOROOT=
```

