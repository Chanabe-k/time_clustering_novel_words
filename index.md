## About
本ページは、NLP2021に投稿した「オンラインコミュニティにおける単語頻度の通時的変化を利用した新語リストの獲得」という論文において掲載した時系列クラスタリングの全体像を載せたものです。
詳しくはNLP2021予稿集（Comming Soon）をご覧ください。

## 概要
日本語において、近年世間に大きく広まった新語のリストを獲得するために、株式会社ドワンゴ様から提供されている「ニコニコ動画コメント等データセット([https://www.nii.ac.jp/dsc/idr/nico/nico-user.html])」および東北大学乾研究室にてクローリングされたTwitterデータを利用し、Pythonの tslearn ライブラリ （[https://tslearn.readthedocs.io/en/latest/index.html]） を用いて単語のクラスタリングを行いました。
なお、単語の分割にはMeCabのNEologd ([https://github.com/neologd/mecab-ipadic-neologd/blob/master/README.ja.md]) を用いています。


クラスタリングされた時系列データの見方は以下の通りです。
![グラフ例](fig/sample_1.png =250x)
上からクラスタナンバー + クラスタに属した単語数、グラフ、クラスタに属した単語となっています。

グラフは横軸が各年（2013~2018年）、縦軸が各年における単語頻度（各単語の頻度を、各年における総単語数で正規化したもの）となっています。


描画されているグラフにオンマウスすると、その線に対応する単語を確認することができます。
![こんなこともできます](fig/sample_2.png 250x)

htmlの作成にはtaucharts ([https://github.com/TargetProcess/tauCharts]) というJavascriptライブラリを用いています。

また、この時系列クラスタリングの可視化において、同研究室の松田耕史氏に大きな協力をいただいております。記して感謝いたします。

## 時系列クラスタリングの結果

### ニコニコ動画コメント等データセット()
[クラスタリング結果](https://chanabe-k.github.io/time_clustering_novel_words/twitter_clustering.html)

### Twitter 
[クラスタリング結果](https://chanabe-k.github.io/time_clustering_novel_words/nico_clustering.html)

#### Contact
- 阿部香央莉 (Kaori Abe)
- 東北大学乾研究室, D1
- E-mail: abe-k[at]ecei.tohoku.ac.jp
