# TRIPLE-ECHO

**TRIPLE-ECHO** は、リスニングとタイピング（ディクテーション）を組み合わせた、高度な英語反復学習システムです。
ブラウザさえあれば、CSV形式の問題集を読み込んで即座に学習を開始できます。

![TRIPLE-ECHO Version 2](https://img.shields.io/badge/Version-2.0-e95c8b?style=for-the-badge)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-f1c40f?style=for-the-badge&logo=javascript&logoColor=black)
![CSS](https://img.shields.io/badge/Aesthetics-Rich-00d2ff?style=for-the-badge)

## 🚀 主な機能

-   **多様な学習モード**:
    -   **通常モード**: 穴埋め、選択問題、和訳、誤文訂正など多様な形式に対応。
    -   **再生モード (Listening Mode)**: 和訳を隠し、英文を自動リピート再生。聞き流しやシャドーイングに最適。
    -   **ディクテーション・モード (Dictation Mode)**: 英文を隠し、聴こえた音をタイピングして再現。
-   **高度な音声設定**:
    -   **アメリカ英語 (en-US) 固定**: ブラウザが持つ高品質な音声エンジンを利用。
    -   **ランダムボイス設定**: 再生のたびに異なる声質（男性・女性等）を選択可能（飽き防止と多様な話者への対応）。
    -   **スピードトレーニング**: 0.1倍速から1.0倍速まで徐々に速度を上げる「段階的再生」機能。
-   **スマートな正誤判定**:
    -   大文字小文字の区別や句読点（ピリオド、カンマ等）の有無を無視した柔軟なマッチング。
-   **進捗管理**:
    -   `localStorage` を利用した「間違えた問題」の記録と復習機能。
-   **CSVによる柔軟な問題作成**:
    -   独自のCSVファイルを読み込むことで、あらゆる教材をアプリ化可能。

## 🛠️ 技術スタック

-   **Frontend**: HTML5, CSS3 (Modern Vanilla CSS), JavaScript (Vanilla ES6+)
-   **Audio API**: Web Speech API (speechSynthesis)
-   **Storage**: Browser LocalStorage

## 📖 使い方

1.  `index.html` をブラウザで開きます。
2.  「1a. 問題csvファイルを選択」から、学習したい教材のCSVを選択します。
3.  「出題数」や「学習モード」を設定します。
4.  「出題開始」ボタンを押して学習をスタート！

### CSVファイルの形式

以下のヘッダーを持つCSVファイルを準備してください：
`"item_id","unit_category","difficulty_level","format_type","question_text","correct_answer","explanation","full_sentence","tags"`

| カラム名 | 説明 | 備考 |
| :--- | :--- | :--- |
| item_id | 問題固有のID | 例: INF-001 |
| unit_category | 単元名 | 例: 不定詞, 接続詞 |
| difficulty_level | 難易度 | 数値またはラベル |
| format_type | 出題形式 | 穴埋め, 選択問題, 誤文訂正, etc. |
| question_text | 問題文 | 穴埋めは `( )` を含める |
| correct_answer | 正解 | 選択問題は `/` 区切りで選択肢を記述可能 |
| explanation | 解説文 | 解答後に表示されます |
| full_sentence | 完成した英文 | 音声再生に使われます |
| tags | 検索用タグ | カンマ区切りで複数指定可能 |

## 📦 インストール / デプロイ

特別なサーバー設定は不要です。ファイルをクローンまたはダウンロードし、`index.html` をブラウザで開くだけで動作します。
GitHub Pages などでのホスティングも容易です。

---

Developed with ❤️ for better English learning.
