# Are We Really Making Much Progress? - A Worrying Analysis of Recent Neural Recommendation Approaches
## Author
+ Maurizio Ferrari Dacrema. Politecnico di Milano, Italy
+ Paolo Cremonesi. Politecnico di Milano, Italy
+ Dietmar Jannach. University of Klagenfurt, Austria

## Why I choose this parper

## Motivation

1.深層学習をベースとした推薦モデルは推薦分野の主流となっていたが、再現性低さや弱いベースラインの応用などについてはまだ重視されていません。
2.各論文では”state-of-art" が溢れ満ちたが、それは本当に推薦分野進捗現状を表せるかの疑問。

## Goal

>1. Reproducibility : To what extent is recent research in the area reproducible (with reasonable effort)?

>2. Progress : To what extent are recent algorithms actually leading to better performance results when compared to relatively simple, but well-tuned, baseline methods?
```
## Approach

###　論文集め
+ タスク： Top-N
+ 会議： KDD, SIGIR, WWW, RecSys
+ 時間：2015~2018
+ 条件：
    1. 深層学習を応用しました。
    2. 評価はPrecision、Recall、MAPなどのランキング指標を使用した。

### Reproducibility

>• A working version of the source code is available or the code
only has to be modified in minimal ways to work correctly.3

>• At least one dataset used in the original paper is available. A
further requirement here is that either the originally-used
train-test splits are publicly available or that they can be
reconstructed based on the information in the paper.

>*In case these artifacts were not already publicly provided, we contacted all authors of the papers and waited 30 days for a response.

<img src=""https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/Table%201.png">



## Next
