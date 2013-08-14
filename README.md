以下のスクリプトの使用は、[mecab-0.996](http://mecab.googlecode.com/svn/trunk/mecab/doc/index.html) と [unidic-mecab_kana-accent-2.1.2_src.zip](http://download.unidic.org/) がインストールされていることを前提としています。
また、MeCab と Unidic の設定は変更せず、デフォルトの状態にしておいてください。
***
### kana-conv.awk
=======
日本語のテキストファイルをカナ表記に変換するスクリプトです。
ヨミはMeCabの解析結果に基づいており、必ずしも正確なものではありません。

### n-gram.awk
=======
テキストの表記のままのN-gramを採取するスクリプトです。
このスクリプトは MeCab も Unidic も必要としません。

### yoko.awk
=======
テキストファイルから、文字・書字形・語彙素を単位としてN-gramを採取するスクリプトです。
複数のファイルの入力に対応しており、マージ機能も備えています。

### sachiko.awk
=======
基本的な機能は yoko.awk と変わりませんが、MeCab と Unidic の環境を整えるのが難しい場合に使用します。
国立国語研究所が提供している「茶豆」による形態素解析済みのデータを、処理することができます。

### yumi.awk
=======
複数のテキストファイルの中で、一致する文字列ごとに出現回数をカウントするスクリプトです。
yoko.awk 、sachiko.awk と同様のマージ機能を備えています。
