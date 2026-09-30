# 逆引き音楽情報処理ガイド

音楽情報処理研究・開発者のためのお役立ちサイト「逆引き音楽情報処理ガイド」プロジェクトです。

このサイトは、音楽情報処理に関する基本手法・実装テクニック・最近のトピックなどの話題を掘り下げ、 研究・開発に従事する方に役立つ日本語資料をまとめています。

Discordサーバー「**音楽情報処理コミュニティ**」によるプロジェクトです。ぜひサーバーにご参加ください！

<a href="https://discord.gg/RJRS8pmpwT">
        <img src="https://img.shields.io/discord/1319190512523280414?style=social&logo=discord&label=音楽情報処理コミュニティ"
            alt="音楽情報処理コミュニティ">
</a>

要望や修正提案はIssuesからお願いします。

# 環境準備

Python仮想環境下で、以下のコマンドを実行することでサイトのビルド環境を構築します。

```
pip install -r book/requirements.txt
```

Jupyter Book 2の実行にはNode.js（18、20、22以降）が必要です。

# JupyterBookのビルド
ローカル環境でサイトの内容を確認するには、以下のコマンドを実行しJupyterBookをビルドしてください。

```
cd book
jupyter book build --html
```

編集中に開発サーバーで確認する場合は、`book/`で`jupyter book start`を実行します。

ビルドを実行すると、`book/_build/html/`の下に静的サイトのデータが生成されます。

Jupyter Book 2の出力は絶対パスとJavaScriptで動作するため、`index.html`を直接開いても表示されません。HTTPサーバー経由で閲覧してください。

```
cd book
python -m http.server 8000 -d _build/html
```

ブラウザで`http://localhost:8000/`を開くと、ビルドされたブックの内容を閲覧できます。