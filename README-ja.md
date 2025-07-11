# tyohyo

帳票出力を行うシステムと統合し協働するためのPDF開発プラットフォーム

# Overview

- pdf-compiler
    - Input: PDF Scheme
    - Output: Raw PDF
    - Features:
        - pdf-generatorのプリプロセッサー
        - DynamicDataの差し込み以外のコンパイルを全て行う(such as handlebars.jsのプリコンパイル)
        - pdfのページサイズの設定
        - 複数ページのレンダリングを可能にする
- pdf-ui
    - Input: Human Operation
    - Output: PDF Scheme
    - Features:
        - GUIを使い、PDF Schemeを簡単に生成することができる
- pdf-generator
    - Input: Raw PDF & Dynamic Data
    - Output: PDF
    - Features:
        - 動的にデータを差し込む
- PDF Scheme
    - PDF Meta Info
    - Page(サイズ、ルートコンテナ)
    - コンテナ
        - LayoutRule
            - Stackベース
            - 絶対値ベース
            - etc
        - ChildItems
            - 線
            - 図形
            - テキスト
            - テーブル
            - 画像
            - コンテナ
            - etc
