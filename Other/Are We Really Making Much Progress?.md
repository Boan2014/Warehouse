# Are We Really Making Much Progress? - A Worrying Analysis of Recent Neural Recommendation Approaches(RecSys'19) 

## [論文](https://arxiv.org/abs/1907.06902)

## Author
+ Maurizio Ferrari Dacrema. Politecnico di Milano, Italy
+ Paolo Cremonesi. Politecnico di Milano, Italy
+ Dietmar Jannach. University of Klagenfurt, Austria

## Why I choose this parper
+ 同じ疑問を持ったことや似たようなケースをあったことがあるからです。

## Motivation

1.深層学習をベースとした推薦モデルは推薦分野の主流となっていたが、再現性低さや弱いベースラインの応用などについてはまだ重視されていません。

2.全ての論文が自分は"state-of-the-art"であるが、それは本当に推薦分野進捗現状を表せるかに対す疑問を持っていて、それを明らかにしたい。

## Goal

>1. Reproducibility : To what extent is recent research in the area reproducible (with reasonable effort)?

>2. Progress : To what extent are recent algorithms actually leading to better performance results when compared to relatively simple, but well-tuned, baseline methods?

## Approach

### 論文集め

+ タスク： Top-N
+ 会議： KDD, SIGIR, WWW, RecSys
+ 時間：2015~2018
+ 条件：
    1. 深層学習を応用しました。
    2. 評価はPrecision、Recall、MAPなどのランキング指標を使用した。

### Reproducibility

>• A working version of the source code is available or the code
only has to be modified in minimal ways to work correctly.

>• At least one dataset used in the original paper is available. A
further requirement here is that either the originally-used
train-test splits are publicly available or that they can be
reconstructed based on the information in the paper.

>*In case these artifacts were not already publicly provided, we contacted all authors of the papers and waited 30 days for a response.

<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/Table%201.png" width=auto height=auto >

### 評価手法
+ すべてのメソッドに対して同じデータセット、同じ評価手順と同じ環境内で評価します。

+ **それぞれの元の論文で使用されていた同じ評価手順とデータセットを使ってもと論文の結果を再現する。
**

>For all reproduced algorithms considered in the individual experiments, we used the optimal hyper-parameters that were reported by the authors in the original papers for each dataset. 

### Baseline
+ #### TopPopular
+ #### ItemKNN
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/ItemKNN.png" width=auto height=auto >

+ #### UserKNN

+ #### ItemKNN-CBF
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/ItemKNN-CBF.png" width=auto height=auto >

+ #### ItemKNN-CFCBF

+ #### P3α

+ #### RP3α

>For all baseline algorithms and datasets, we determined the optimal parameters via Bayesian search using the implementa- tion of Scikit-Optimize6. We explored 35 cases for each algorithm, where the first 5 were used for the initial random points. We con- sidered neighborhood sizes k from 5 to 800; the shrink term h was between 0 and 1000; and α and β took real values between 0 and 2.

### 結果
+ #### Collaborative Memory Networks (CMN)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/CMN.png" width=auto height=auto >

+ #### Metapath based Context for RECommendation (MCRec)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/MCRec.png" width=auto height=auto >

+ #### Collaborative Variational Autoencoder (CVAE)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/CVAE.png" width=auto height=auto >

+ #### Collaborative Deep Learning (CDL)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/CDL.png" width=auto height=auto >

+ #### Neural Collaborative Filtering (NCF)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/NCF.png" width=auto height=auto >

+ #### Spectral Collaborative Filtering (SpectralCF)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/SpectralCF_1.png" width=auto height=auto >
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/SpectralCF_2.png" width=auto height=auto >

+ #### Variational Autoencoders for Collaborative Filtering (Mult-VAE)
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/Mult-VAE_1.png" width=auto height=auto >
<img src="https://raw.githubusercontent.com/Boan2014/Warehouse/master/Other/Mult-VAE_2.png" width=auto height=auto >

## DISCUSSION
+ 不適切なベースラインの選択と最適化の欠如
+ 異なるデータセット、評価プロトコル、測定基準、およびベースラインの使用。
+ 精度値に対する過度の追求

## 考察
+ 精度と多様性のトレードオフ
+ 説明性への繋がり
+ DLの強み

## Next
+ Jöran Beel and Stefan Langer. 2015. A Comparison of Offline Evaluations, Online Evaluations, and User Studies in the Context of Research-Paper Recommender Systems. In Proceedings TPDL ’15. 153–168.

+ Paolo Cremonesi, Franca Garzotto, and Roberto Turrin. 2012. Investigating the Persuasion Potential of Recommender Systems from a Quality Perspective: An Empirical Study. Transactions on Interactive Intelligent Systems 2, 2 (2012), 1–41.

+ Florent Garcin, Boi Faltings, Olivier Donatsch, Ayar Alazzawi, Christophe Brut- tin, and Amr Huber. 2014. Offline and Online Evaluation of News Recommender Systems at Swissinfo.Ch. In Proceedings RecSys ’14. 169–176.

+ Andrii Maksai, Florent Garcin, and Boi Faltings. 2015. Predicting Online Performance of News Recommender Systems Through Richer Evaluation Metrics. In Proceedings RecSys ’15. 179–186.

+ Marco Rossetti, Fabio Stella, and Markus Zanker. 2016. Contrasting Offline and Online Results when Evaluating Recommendation Algorithms. In Proceedings RecSys ’16. 31–34.
