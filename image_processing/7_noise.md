# ノイズ除去
ディジタル画像には、本来の画像に何らかの形でノイズが付加されていることが多い。ノイズを目立たなくするために、ノイズ除去を行う。ノイズ除去は、画像では輝度値が急激には変化しないことを利用し、周辺の画素の情報を利用することで行う。

![](./etc/noise_1.jpg)

平滑化フィルタは、周辺の画素の輝度値の平均を新しい輝度値とするものである。すなわち、次のようなフィルタを適用する。

|1/9|1/9|1/9|
|:-:|:-:|:-:|
|1/9|1/9|1/9|
|1/9|1/9|1/9|

また、メディアンフィルタは、周辺の画素の輝度値の中央値を新しい輝度値とするものである。すなわち、例えばある画素の周辺の画素値が以下のようであった場合、

|12|18|13|
|:-:|:-:|:-:|
|19|255|17|
|15|12|14|

画素値を小さい順に並べると、12  12  13  14  15  17  18  19  255 となる。中央の値をとって、15を新しい画素値とする。

# 課題

課題で使用する画像は，`./imgs_7/noise`にあります．

1. 平均化フィルタをノイズ画像に適用し，結果を表示せよ．フィルタのサイズは（３，３）とする．
2. メディアンフィルタをノイズ画像に適用し，結果を表示せよ．フィルタのサイズは（３，３）とする．
3. 平均化とメディアンフィルタのサイズを（５，５）にせよ．（３，３）と（５，５）の結果を比較せよ．
4. 平均化とメディアンフィルタのサイズを（N，N）にせよ．（３，３）と（N，N）の結果を比較せよ．