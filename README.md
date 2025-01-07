# Japanese-MIR-Book
音楽情報処理日本語リソース集。Collection of Music Information Retrieval Resources in Japanese.

# 環境準備

Python仮想環境下で、以下のコマンドを実行することでブックのビルド環境を構築します。

```
pip install -r book/requirements.txt
```

# JupyterBookのビルド
以下のコマンドでブックをビルドします。

```
jupyter-book build book/
```

ビルドを実行すると、`book/_build/`の下に静的サイトのデータが生成されます。

```
book
 └──_build
    └── html
       ├── _images
       ├── _static
       ├── index.html
       ├── intro.html
       ...
```

`book/_build/html/index.html`をブラウザで開くことで、ビルドされたブックの内容を閲覧できます。