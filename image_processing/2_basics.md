# Pythonの起動
`$ python` or`$ ipython`


# [Pythonの練習](https://docs.python.org/ja/3/tutorial/introduction.html#numbers)
まず，計算してみましょう．
```
>>> 2 + 2
4
>>> 50 - 5*6
20
>>> (50 - 5*6) / 4
5.0
>>> 8 / 5  # division always returns a floating point number
1.6
>>> 17 / 3  # classic division returns a float
5.666666666666667
>>>
>>> 17 // 3  # floor division discards the fractional part
5
>>> 17 % 3  # the % operator returns the remainder of the division
2
>>> 5 * 3 + 2  # result * divisor + remainder
17
>>> width = 20
>>> height = 5 * 9
>>> width * height
900
```
演算子 / と // はどのような計算をしているでしょうか？


次に，リスト型を使ってみます．リスト (list) は、コンマ区切りの値 (要素) の並びを角括弧で囲んだものとして書き表されます．
```
>>> squares = [1, 4, 9, 16, 25]
>>> squares
[1, 4, 9, 16, 25]
```

リストの要素にアクセスしてみます．
```
>>> squares[0]  # indexing returns the item
1
>>> squares[-1]
25
>>> squares[-3:]  # slicing returns a new list
[9, 16, 25]
```


基本的な文法を見ます．

if文
```
x = int( input('Your value: ') )
if x > 3:
  print('Big')
elif x==3:
  print('Medium')
else:
  print('Small')
```

while文
```
c=0
while(True):
  c += 1
  print(c)
  if c==5:
    break

```

for文
```
for i in range(10):
    print(i)

```



# [Numpyの練習](https://github.com/rougier/numpy-100)
Pythonの数値計算ライブラリであるNumpyを練習します．Numpyを用いて，行列やベクトルなどを効率的に処理できます．

1. ライブラリの読み込み．`import numpy as np`
2. ベクトルの作成 `X = np.zeros(5)`
3. 二次元べエクトルの作成 `X = np.zeros( (3,4) )`．手動で設定する`X = np.array([ [1,2,3], [4,5,6] ])`
4. 行列のサイズを取得する `X.shape`



# 画像の読み込みと表示
画像の表示にはPythonの描画ライブラリである，[Matplotlib](https://matplotlib.org/index.html)を用いいます．
```
import matplotlib.pyplot as plt  # ライブラリの読み込み
plt.ion()  # インタラクティブモードON
```

画像の読み込みは，scikit-imageを用います．
```
from skimage import io # 入出力ライブラリの読み込み
im = io.imread('./imgs/cat.jpg')  # 画像ファイルの読み込み
plt.imshow(im)  # 表示
```


# 練習問題
1. 画素値が赤，青，緑となる画像（縦1画素，横3画素）を作成，表示し，保存せよ．
2. 次の画像を作成せよ．縦100画素，幅300画素，幅0-99画素は赤．100-199は青，200-299画素は青．
```
img = np.zeros( (5,5), 'uint8')  # 5*5画像の初期化
io.imsave('test.png', img )  # 画像の保存
```
