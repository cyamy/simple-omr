# simple-omr
 テスト採点を自動化するために製作しました．

## 使用方法
1. 必要ライブラリのインストール
```
% pip install pandas
% pip install numpy
% pip install python-opencv
```

2. 実行
```
% python3 omr.py   

seet count = 1
```

3. 結果表示
```
% column -t -s "," result.csv   

grade  class  number  Q1  Q2  Q3  Q4  Q5  Q6  Q7  Q8  Q9  Q10  Q11  Q12      Q13      Q14  Q15 
0      2      17      34  4   5   8   4   9   3   7   5   6    10   no data  overlap  5    6    
(略)
```
（端末上では結果が一列ズレて表示されますが，表計算ソフトでは問題なく表示されます）

## 注意点
* A4レイアウトを用いて解析します．
    * scandata直下にスキャンしたデータをpng形式で保存してください．

* マークシートレイアウトを変更した際は，プログラムの修正が必要です．

* スキャナによってはうまく動作しない可能性があります．
    * 自身の環境で読み取ったマーカを用いてください．
    * 識別閾値を変更することで，対処できるかもしれません．

* 印刷機を使用する際，大きく傾くとうまく読み取れない可能性があります．

## ToDo
* デスクトップアプリ化
* 全てマークシート問題では，定期考査に不向きな教科ばかり
    * 代替手段の検討
