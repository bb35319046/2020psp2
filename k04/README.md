# 課題4 レポート

bb35319046 松本峻汰
## 課題

[../sample/heights.csv]は標本全体（男性と女性合わせた14人）のデータをまとめたものである．
一方，[../sample/IDs.csv]は標本14人の学籍番号（身長データと同じ順番）である．
学籍番号を尋ねて，その学籍番号のデータがリストにあれば，学籍番号，身長，性別のデータを表示し，リストになければ，「No data」と表示せよ．

この二つのファイルを読み取り，学籍番号，身長，性別の3つをメンバーとする構造体の配列で管理するとよい．

## ソースコードの説明
l5~l9:構造体の配列を宣言。

l46~l48 & l60~l61:ファイル内の性別、身長、IDの値を宣言したgender,heights,IDに代入。

l72~l88:入力したIDとファイルから格納したIDを比較して、存在すれば身長と性別を表示する。また、比較したときにIDが違うごとに変数nodata（初期値0）に1ずつ足していく。

l90~l94:上記の通りにしていくと、nodataは13または14になる。14になるということは、入力したIDがファイルから格納したIDが一度も一致しなかったということになるので"No data"と表示する。

## 入出力結果

例えば，ID 45313125のデータを調べたいとき，

```
input the filename sample heights:../sample/heights.csv
input the filename of sample ID:../sample/IDs.csv     
which ID`s data do you want?: 45313125
ID :45313125
gender :Female
heights :152.40
```

例えば，ID 45313124のデータを調べたいとき，

```
input the filename sample heights:../sample/heights.csv
input the filename of sample ID:../sample/IDs.csv     
which ID`s data do you want?: 45313124
-------
NO data
-------
```

## 修正履歴
[comment #20200630]
- 修正の指示、アドバイス等は特にありません。引き続き先生に提出をお願いします。

[comment #20200716 sonoda]
- 課題4の完了を確認しました．
