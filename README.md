# Wordファイルを自動で表記統一するスクリプト

## Pythonのバージョン確認

Python本体（もしくはAnaconda）のインストールが必要です。

`python -V` を実行して、バージョンが 3.x 以上であることを確認してください（特にmacOS）。

- macOSでバージョンが 2.x 以下の場合
    - Homebrew などで新しいバージョン（3.9など）をインストールしてください
        - [macOS環境のPython: Python環境構築ガイド - python.jp](https://www.python.jp/install/macos/index.html)
    - `python` のかわりに `python3` コマンドを利用してください
- Windowsの場合
    - インストールされていない場合は下記参照
        - [Windows 環境のPython: Python環境構築ガイド - python.jp](https://www.python.jp/install/windows/index.html)

## インストール

- 次のパッケージが必要です
    - `pandas`
    - `notebook` (Jupyter Notebook)
    - `python-docx`

### 通常のPythonの場合（Anaconda以外）

```
$ python -m pip install --upgrade pip
$ python -m pip install pandas
$ python -m pip install notebook
$ python -m pip install python-docx
```

### Anacondaの場合

`pandas` と `notebook` はすでにインストールされているはずです。

```
$ conda install -c conda-forge python-docx
```

## 使い方

- 原稿を `before.docx` という名前で作成
- `unification.csv` を編集して好きなルールを作成
- 原稿と表記統一ルールを本スクリプトと同じディレクトリに移動
- Jupyter Notebookを起動する
    - `$ jupyter notebook`
- `w_unification.ipynb` を開く
- 「after.docx」という名前の表記統一済みファイルが自動でできる

