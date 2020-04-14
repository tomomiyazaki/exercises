# Minicondaのインストール
- ダウンロード & 実行
https://docs.conda.io/en/latest/miniconda.html

- 環境変数の設定
```
$ vi .bashrc
$ export PATH="/Users/tomo/local/miniconda3/bin:$PATH"
```


# Conda環境を作成する
```
$ conda create -n souzou python=3.7.2
$ source activate souzou
$ conda install numpy matplotlib==3.0.3 ipython scikit-image 
```


