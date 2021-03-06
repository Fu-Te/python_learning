# Python3入門の入門


***


# 前書き
## はじめに
みなさんは，コンピュータを制御する方法だったり，IT技術を使って何かを解決するといったことに興味を持っているだろうか．Pythonには，あなたのそんな夢を解決するための方法がたくさん用意されており，また，早く実装できることがある．そして，コミュニティがとても大きく，質問をすると解決できたりといったことがある．
また，***プログラミングにおいて，調べる力（ググる力）はとても大切**だと私は考えています．そのため，基礎については例示するが，それ以上のことは調べてもらうように構成しています．調べる力，調べ方を養っていきましょう．

本書では，最近話題のプログラミング言語Pythonの基礎の基礎の学習のお手伝いをさせていただく．Pythonを習得し，夢へと近づきましょう！

## ソースコード，環境
ソースコードは全てGithubで入手することが可能です．
Githubからファイルをダウンロードし，ぜひ実行してみてください．本書に書くプログラムもエラーなく動くことを確認しますが，環境によって動かない可能性があります．

筆者の環境は以下の通りです
OS: macOS Monterey
Python3.9.4
https://github.com/Fu-Te/python_learning

## 免責
本プログラムは全て筆者環境やクラウド環境において，動くことを確認していますが，動かない可能性があります．
本プログラムを改造等し，損害を被ったり，警察沙汰になっても筆者は責任を負いかねます．

***

## なぜPythonなのか
PythonだとAI開発を素早く行うためのライブラリがたくさん存在しており，AI開発の標準的な言語であり，また文法がとてもわかりやすいことからとても人気な言語となっている．
機械学習以外の分野，Web系やコンピュータ制御やネットワーク系もPythonで実装可能である．
さまざまな便利なツールも最終章で紹介する．

## 本書の対象とする人
プログラミングに関する知識がない人
Pythonの文法を知りたい人
これからプログラミングを頑張っていきたい人

## 本書の構成
本書では，実際に動かせるプログラムを”書き”動作させることでプログラミングへの理解進めていく形式を取る．
Pythonはインタープリタ言語と呼ばれ，１行ずつプログラムが実行されるのでとてもわかりやすく学ぶことができる．
インタープリタ言語の対となるのがコンパイラ言語(C,Rust,C++等)があるが，インタープリタ言語で動きを学んでから，コンパイラ言語の習得を目指しても遅くない．

***

# プログラミングとはどうやるのだろうか？
筆者もまだプログラミングを始めてそう長くないが私のプログラムの書き方やエラーにぶつかった時の対処法を記す．
私自身，高校生の時にプログラミングを始め，最初は何が何だか全くわからなかった．エラーが出てもグーグル先生に聞くことをせず，すぐに本を読み，基礎から学習するということを何度も繰り返し，Pythonに関する本を5冊程度読むということを繰り返した．しかし，これではいつまで経っても何も作れないままなのである．なぜなら，それらの本は基礎しか教えてくれないからである．
この本でPythonの基礎を学んだら，ぜひ何か作りたいものを定め，実装してみてほしい．実装をする途中でわからないことや，エラーに何度も出会うだろう．しかし，そのエラーを調べ，なぜできないのか，なぜできたのかを考えることによって私は成長したという実感を得ることができ，また実装する力もついてきたと思う．
せっかくインタープリタ言語を使っているので，トライアンドエラーを繰り返し成長してほしい．

***

# Pythonを使えるようにする(環境構築)
WindowsとMacosに分けて説明する．必要な部分をつまみながら環境構築をしてみてほしい．
本書では，特にPythonのバージョンを指定しないが，筆者はPython3.9.4を利用している．

## Windows
1.スタートメニューを開き，「Microsoft Store」と入力し，ストアを開く．
![](images/IMG_0007.jpg)
2.ストアが開いたら，右上の検索を選択し，「Python」と入力してください．
3.Pythonのダウンロードとインストールが完了したら，またスタートメニューを開き，「Windows PowerShell」を開いてください．それを開いたら```Python --version```と入力し，Python3がインストールされていることを確認してください．

上記の手法でできなかった場合は，ググってみてください！
参考リンクも残しておきます．
https://docs.microsoft.com/ja-jp/windows/python/beginners

## macos
macにはPythonが既に入っています．ターミナルを開き，```python --version```としてみてください．バージョンが表示されるはずです！

古いバージョンだったりしたら，新しく入れ直すことも可能です．
macosにはHomebrewという便利なツールがあります．これからプログラミングを続けていく中で，かなり便利なツールなので，入れてみても損はないと思います．気になる方は調べてみてください！
Homebrew: https://brew.sh/

## バージョン管理ツールAnaconda
Pythonにはたくさんのライブラリがあります．そのライブラリを管理したり，Pythonのバージョンごとに環境を作ることができる最強のツールであるAnacondaの導入方法を紹介します！これはMac,Win共通です！

https://www.anaconda.com/products/individual
上記のリンクからAnacondaをダウンロードし，お使いのコンピュータにインストールしてください！

次の章で説明するJupyterNotebookはAnacondaを入れることによって利用できるようになります！

***

# JupyterNotebookの使い方を学ぶ
JupyterNotebookは統合開発環境と呼ばれるものです．ブラウザ上で動き，プログラムを書いて実行するとすぐに結果が出力されるという優れもので，筆者もよく使います．
JupyterNotebookはオープンソースであり，無償利用が可能，豊富なライブラリが使える，実行結果がすぐに出るという3本柱でPythonを使う人にとっては神的なツールであります！！
**jupyternotebookの拡張子は.ipynbですが，Pythonの拡張子は.pyです**
今回はわかりやすく.ipynbを使うのですが，コンピュータを制御する時などは.py形式の方が有用です．拡張子が異なりますが，どちらも同じPythonを用いているので文法等は同じです．
今回はプログラミング言語Pythonの習得を目的としているので，わかりやすい.ipynb形式を使います

はいはい，わかったよ．んでどうやって使うんだって話ですよね．．．！
このツール，私が知る限りだと４つくらい使い方があります．．．！！
1.GoogleColaboratory
![](images/Colaboratory.png)
2.AWS SageMaker
![](images/SageMaker3.png)
3.AnacondaについてるJupyterNotebook
![](images/jupyter.png)
4.VisualStudioCodeの拡張機能を使う
![](images/jupyter2.png)

***

前のページの通り4通りですね．．．それぞれメリット，デメリットがあるので紹介しますね．
1,2は最近流行りのクラウド技術を用いたものです．どちらも無料で使うことができます．環境構築が不要で，自分のパソコンにアレ入れてーこれ入れてーとかっていっためんどくさい作業がなくなります！！
3,4は自分のパソコンに計算をさせる感じですね．いいところはローカルで実行できるってところですね．データがデカすぎてクラウドに上げられないよ，とかクラウドより高性能だし！！って人はローカルもいいですね．環境構築が鬼門になりそうですが，それも経験の一つです！
何いってるのか全然理解できん．．．って人は，調べてみてください！！

ちなみに，筆者は2,3,4を使ってます！

今回，本書では，2と3でやってみてほしいなーって感じなので，使い方について説明しますね！

***

## AWS SageMaker
こちらのツール，環境構築が必要なく利用できるので，コンピュータわからんし，何入れたらいいかわからん！AnacondaもめんどいしPython入れるのもめんどくさって人にめっちゃおすすめです！！
ただ，SageMakerって申請して次の日くらいから使えるようになるので，そこだけご了承をって感じですが．．．
https://studiolab.sagemaker.aws/
![](images/SageMaker.jpeg)
上のリンクに飛んでもらって，「Request free account」って押して，色々入力して，「Submit Request」って押してください．多分，登録したメールに確認メールきて，申請が承諾されるとアカウントが発行されるはずです．そしたら右上にあるSign inを押して，ログインしたら使えるようになります！

***

![](images/SageMaker2.png)
ログインするとこんな感じになります！
Select compute typeっていうのCPUとGPUあるんですけど，CPUの方が得意な計算とGPUの方が得意な計算っていうのがあって，場合によって使い分けます．本書で取り組むものはCPUで十分です！どれだけ使っても無料なので，どんどん使っちゃってください！
使えるようになるまでをまとめます
1.アカウント作成リクエストを送る
2.サインインする
3.GPUかCPU選ぶ
4.Start runtimeおす
5.Open projectを押す
ってな感じでサービス使えるようになりまーす．

***
### SageMaker使ってみる
![](images/SageMaker4.png)
Open project押すとこんな感じのタブが開く．筆者の環境の場合，すでにファイルがあるが，みなさんのところにはまだないと思う．
![](images/SageMaker6.png)
**Notebookのdefault:Python**ってところをクリックするとJupyterNotebook形式でコード書けます！

ちなみに，サンプルコードを実行したいなーって時は，Githubからダウンロードして，紫の＋ボタンの２つ右にあるアップロードするボタンがあるのでそこを押して，アップロードしたいファイルを選択したらサンプルコードを使えるようになります！

これでSageMakerの一通りの使い方はおしまいです！わからないことがあったら調べてみてください！


***

## AnacondaのJupyterNotebook
Anacondaに付属しているJupyterNotebookはローカル環境で動きます！
使い方は以下の通り
1.Anacondaを導入する
2.Anacondaを起動する
3.JupyterNotebookのLaunchを押す
![](images/jupyter3.jpg)
少し待つとWEBブラウザに開きます．
ここで，プログラムがあるフォルダや，これからプログラムを作りたいフォルダをクリックして
![](images/jupyter4.png)
こんな感じになる．
多分，まだファイル作ってない人は空のフォルダになっているので，画像の右上の新規ってところ押して，Python3を選択してファイル作ってください！そしたらUntitled.ipynbっていうファイルができます！
![](images/jupyter5.png)
この画像のUntitledってところクリックするとファイルの名前変えられます！

これでとりあえず設定の説明を終わりにします！

***

## JupyterNotebookの基本的な使い方
![](images/jupyter6.png)
プログラムは```print('Hello,World')```って書いてあるところに書きます！
このコードを動かすには，▷押すと動かせます．WindowsだとCtrl+Enterで，MacだとCommand+Enterで動かせるはずです！
で，新しい行を追加したい時には＋マーク押してください！

基本的なことはここまでで，後は使いながら慣れていきましょう．．．
〜〜したいけどできないのかな？とか疑問に思ったらすぐに検索してください！！
例文「JupyterNotebook，新しい行追加」みたいな感じで！

## .ipynb形式について
.ipynb形式だと，上の行の内容がしたの行にも続いています．普通，プログラムは全て完成させてから実行しますが，ipynb形式だと１行ずつでも実行でき，わかりやすいのが強みです．なので.py形式でなく.ipynb形式を用います．ここについての説明は難しいので，気になった方は
「ipynbとは」,「ipynb,py違い」みたいな感じで検索してみてください

***


# 1.Pythonの基本文法
サンプルコード名:1_python.ipynb

早速，Pythonを使ったプログラミングに入っていきましょう！！
前にも説明した通り，Pythonはインタープリタ言語で，１行ずつ実行されるのが特徴です！！
プログラミング学習で一番最初にやることといえば，「Hello,World!」を表示することですね！
```python
print('Hello,World!')
```
たったこの１行で実現できてしまう．．すごい！！
初めてなので，例を示しときます！
![](images/jupyter6.png)
こんな感じに入力して，Runってしてみてください！
プログラムを書いてて，そのプログラムがどんな処理をしているのかって他の人からわかりにくいですよね？そんな時に役に立つのが，コメントというシステムです
```python
# hello,worldを表示
print('Hello,World')
```
コメントの始めに#をつけることでコメントを記入することだってできちゃいます！
面白いのはこれからです！次に移ります！

***

# 2.変数
サンプルコード名:2_variable.ipynb

早速，変数っていうプログラムを理解する上手とても大切な概念を説明します！
## 変数ってなに？
まず変数って何ってところですよね．
変数はPythonに限らずプログラミング言語では何かしらの値を格納するために用意されるもののことです．何回も繰り返し使ったり，後から呼び出したりとかする時に使うことが多いです！
では，実際に変数を使ってみましょう！

## 変数の定義
まず，変数を定義して，使えるようにします！
```python
a=2
print(a)
```
を実行してみてください！
aって結果が出力されそうですが，2が出力されましたよね．printでaの中身を出力しています！
例えば，レジシステムを構築したいといったことがあるとしましょう．
```python
orange = 'オレンジ'
apple = 'りんご'
orange_price = 100
apple_price = 200
print(orange,orange_price)
print(apple,apple_price) 
```
を実行してみてください！orangeにはオレンジ，orange_priceには100が入っていることがわかります．
ここで大事なことがあります．**数値を定義する時には''が必要なかったが，文字列を入力する時には''が必要なことです**
文字列や数値って何？っていうのは，３章のデータ型のところで説明します！


## 変数名はどうやって決めるの？
他の人がプログラムを見た時，変数名を見てこの変数がどんな意味を持っていて，どんな役割なのか，すぐにわかることってとっても大切です．
プログラミングをする人たちの間では「自分で書いたコードでも誰が書いたかわからない」みたいなことわざがあります．つまり，いつ見ても誰が見てもわかるようにした方がより良い変数名であるといえます．
基本的に，変数名は日本語ではなく，英語で付けられることが多いですね．
ここら辺の話は，プログラミングに慣れてから追々考えればいいお話かなと個人的には思うので，ここら辺にしておきます！

***

## 変数の値を更新する
変数の値は更新することができます．
```python
orange_price = 100
print(orange_price)
orange_price = 200
print(orange_price)
```
これを実行すると100と200が順番に出力されます！プログラムは上から順に実施され，その時に一番新しい値を出力します．
## 変数を別の変数に代入する
変数に定義した内容を別の変数の中に入れることもできます！
```python
orange = 'オレンジ'
print(orange)
apple = 'りんご'
orange = apple
print(orange)
```
このコードを実行するとオレンジの後りんごが出力され，変数の中に別の変数を入れることができるということに気づくでしょう！

## 変数どうしで計算する
前に説明したレジシステムを使って説明します．
オレンジとりんご1つずつ購入し，その合計金額を求めるコードを提示します
```python
orange = 100
apple = 200
total = orange*1 + apple*1
print(total)
```
このコードを実行すると300が出力されるはずです．
追いやすく整理します
$$total = 100*1 + 200*1$$
となって計算されているのです！

また，文字同士を連結させることもできます！
```python
orange = 'オレンジ'
apple = 'りんご'
orange_apple = orange + apple
print(orange_apple)
```
この性質を利用すれば，文字を何回も出力したいときは変数名*回数といったようにすれば，指定した回数だけ文字列を出力することもできます！

## 入力を変数に保存
```python
test = input('文字を入力してください:')
print(test)
```
これを実行するとユーザに入力を求め，ユーザが入力した内容がtestに入ります．
input()はユーザに入力をさせる時に有効です．しかし，ユーザに入力をさせることは問題を発生させる可能性があることも頭に入れておく方が良いでしょう．

サンプルコードには，他にもコードを提示しているのでみてみてください！

***


# 3.データ型について
なんだいきなり，データ型って？みんなそうなるはずです！
Pythonではあまりデータ型を意識せずともプログラムを書くことができるようになっていますが，そのうち型が違いますといったエラーが出てPythonに怒られるでしょう．その日が絶対に来るので説明しておきます．

サンプルコード:3_data_type.ipynb

## 文字列
早速例を示します！
```python
name = '名前'
type(name)
```
を実行してみてください！
strと表示されるはずです！**str**はStringの略で文字列を意味します．
文字列は''か""によって挟まれています．
また，
```python
zero = '0'
type(zero)
```
これを実行してもstrになるはずです．

## 整数型
続いて整数型です．整数型は名前の通り整数を扱う時に使います
```python
a=10
type(a)
```
**int**と表示されるはずです．intはintegerの略で整数を意味します

## 浮動小数点
続いて浮動小数点です．これは小数点を含む数値を扱います
```python
a=1.1
type(a)
```
**float**と表示されるはずです．

***

## 複素数
```python
c=10j
type(c)
```
jをつけると複素数扱いになります．
**complex**と表示されるはずです！

## ブール(bool)
boolとは真か疑かを判断し，TrueかFalseを返します．
```python
flag = True
type(flag)
```
boolと表示されるはずです．真偽は第６章の条件分岐，繰り返しでよく使い，それはTrue or Falseで評価をすることが多いです．

## 型変換する
1という数字はstr型でもint型でもfloat型でも扱えます．自分でプログラムを書く時に，どの型で保存している方が便利なのかといった場面があるとしましょう．
例えば1という数字が文字列で保存されていて，int型にしたいときは
```python
one = '1'
one = int(one)
type(one)
```
このようにするとstr型からint型へ変換できます．
また，inputを用いてユーザの入力を取得したが，inputで取得した内容はstr型で手に入るので，数値にしたい時には上の例のように型変換を用いなければなりません.
intからstrの時は
```python
one = 1
one = str(one)
type(one)
```
でstr型に変更できます．
これらの型変換は，intとstrに限った話ではありません．まだまだたくさんの例があり，例示しきれないので，困った時は検索してみてください！
「python 型変換」


***

# 4.数値
サンプルコード:4_calculate.ipynb
ここではPythonでの四則演算の例を示していきます．
```python
10+3 #13　足し算
```
```python
10+(-12) #-2足し算
```
```python
10*3 #30掛け算
```
```python
10-3 #7引き算
```
```python
10/3 #3.333割り算
```
```python
10%3 #1余りを求める
```
```python
10%2 #0余りを求める
```
```python
10**3 #1000べき乗
```
この四則演算の仕組みをうまく使って条件分けをしたりします．
例えば，2の倍数を求める時は2で割った時，余りが0になる．を使います．
サンプルコード:4_compare_actuators.ipynb
また，左辺と右辺が正しいかどうかを確かめる時は
```python
10==10 #true
```
のように記述します．そうすると先ほど学んだブール型で返答が返ります．
等しくない時は!=を使います．
```python
10!=9 #true
```
また，数値の大小を比較する時は，
```python
10>9#true
```
```python
10>=9#true
```
のように表します．

これでも例示が足りない場合は
「python 四則演算」で検索！

***

# 5.文字列
サンプルコード:5_string.ipynb
みなさんはもう文字列について認知しているでしょう．
文字列同士で足し合わせることも，掛け合わせることもできることは例示しました．
次は，文字を置き換えたり，全部大文字にしたりといった操作です．
```python
firstname= '福富'
lastname= '哲平'
name = firstname+lastname
print(name)
```
文字列には，文字列を操作するためのメソッドがたくさん用意されている．
そのうちのいくつかを例示する．
文字を置き換えるときは.replace()メソッドを使います！ちなみに，メソッドについては10章で説明する予定です！
```python
name_english = name.replace('福富','Fukutomi')
print(name_english)
```
ここで勘がいい人，プログラムに慣れてきた人はあることに気づくでしょう．
nameを定義していないのになんで動いたのだろうかと．
ipynb形式では上の行で定義した変数を次の行で定義せずとも使えるようになっています．

***

2番目の文字を取得したい時は
```python
second = name[1]
print(second)
```
えっ！なんで２番目なのに1なの？って思う人が多いと思います．
このような数字は添字と呼ばれますが，コンピュータは0からカウントを始めることが多いです．
なので自分が欲しい番号は(欲しい番目-1)となります．

また，スライスという技術を使うと，何番目**から**何番目というのを指定できます
```python
slice_name = name[0:2]
print(slice_name)
```
えっ！0から2だったら3番目の数字まで出てくるんじゃない？そう思うのが普通です．
しかし，スライスの終わりの番号は，-1した数値を入れます．つまり，この例では0から1を指定して取り出しています．
スライスは他にも色々な書き方が存在します．
気になる方は「python スライス　書き方」で検索！

これ以上例示すると多くなってしまうので，文字列について詳しくなりたい人は
「pyhon 文字列操作」や「python メソッド」，「python 大文字にする」などで調べてみてください．

***

# 6.条件分岐/繰り返し
サンプルコード:6_conditional.ipynb
ここでは条件分岐や繰り返しについて学びます！
プログラミングをする上で一番大事な要素だと思っています．しっかりと理解できるようにしましょう！！
## 条件分岐
条件分岐をさせるときのキーワードはif,elif,elseの３つです．
テストの例で考えてみましょう．
```python
test=81
if test>60: #60点より高いなら
    print('合格')
else: #それ以外なら(60点以下)
    print('不合格')
```
あれ，なんかifの後スペース4こ，タブ1個分空いているなーって思いましたか？
Pythonではそれをインデントと呼び，:の後にその条件式の後に実行することを書きます．これをブロック定義と言います．どこからどこまで実行するのかを示すために使われます．他の言語だと{}でブロックを示すことが多いです．


この場合，合格と不合格どちらが出力されるでしょうか？実行してみましょう！
elifを使うと，より詳しく分類させることもできます．
```python
if test>80:
    print('優秀')
elif test>60:
    print('合格')
else:
    print('不合格')
```
これでif,else,elifの使い方を見ていきました．難しいですか？
ifはもし〜なら，elseは〜でないならのように表されます．また，プログラムは上から実行されるので，優秀に該当した場合，合格は表示されません！

また，プログラミングでは，ifの中にifを入れることもあります．
例えば，
```python
if test>60:
	print('合格')
	if test>80:
		print('優秀')
else:
	print('不合格')
```
こうすることで，合格と優秀の二つが表示されます．
この条件分岐を組み合わせることで複雑なプログラムを作成することができます．

ここでは条件分岐の一例を示しました．より詳しい使い方が知りたい方は公式ドキュメントを読むなり，「python 条件分岐」で調べるなりして，色々なコードをみて，知識を深めましょう！

***

## 繰り返し
pythonの繰り返しには
for
while
の２種類があります．とてつもなく便利です．
人間が繰り返し作業をするととてつもなく時間がかかるが，プログラミングならすぐにできます！
繰り返しこそがプログラミングをする価値とも言えるでしょう．
操作するファイルが1つなら手でやった方が早いなんてことがよくあります．プログラムを書くか手でやるかどっちが早いのか．手でやった方が早いのにプログラムを書くのはなんか違いますよね．**手段が目的**になっているのです．

簡単なwhile文を示します．
```python
i=0
while i<100: #100以下なら繰り返す
    print(i)
    i=i+1 #iに1をたす
```
ここで出てくるi=i+1はプログラミングではよく使います．また，これはi+=1といった形でも同様の動きをします．コードを変えて試してみても良いでしょう．
上のコードと同じ動きをするコードをforで書いてみます
```python
for i in range(100):
    print(i)
```
どうでしょう，動きは違いましたか？

whileは条件を満たすかどうかで，条件式がtrueの間，繰り返します．
forは指定された回数繰り返す．
といった使い分けがあります．プログラムをのケースによってどっちを使うかを使い分けるイメージです．コードをたくさん書いて，感覚を磨きましょう．
気になる方は「while for使い分け」のように検索すると良いでしょう．

***

ここで，有名なfizzbuzz問題を見てみましょう
```python
for i in range(1,101):
    if i%15==0:
        print('fizzbuzz')
    elif i%5==0:
        print('buzz')
    elif i%3==0:
        print('fizz')
    else:
        print(i)
```
15の倍数の時fizzbuzz,5の倍数の時buzz,3の倍数の時fizzを表示します．このfizzbuzz問題は，プログラミングのキモである繰り返しと条件分岐の使い方がわかっているかを問えるので，よく聞かれる問題です．

for分の便利な使い方を示します．
```python
dist=['りんご','いちご','めろん']
for i in dist:
    print(i)
```
これはまだ説明していないlistというものを使っています．forではinのあとにリストを指定することで，リストの中身を取り出すことができます．

これと同じ動作をwhileでも行えます
```python
i=0
while i<=2:
    print(dist[i])
    i=i+1
```
forとwhileどちらの方が綺麗でしょう？forですよね．このような感覚はコードを書くことで磨けると思います．

また，繰り返しにはbreakとcontinueがあります．便利です．
```python
for i in range(100):
    if i==90: #90になったらおわる
        break
    elif i%10==0: #0で割れるときは何もしない
        continue
    print(i)
```

繰り返しの説明はここら辺にしておきます．
わからないことは調べてみましょう！

***

# 7.リスト/タプル/辞書
list:リスト，配列．複数の要素を含む．[]を使って定義し，各要素の間はカンマで区切る
tuple:タプル．複数の要素を()を使って定義し，書く要素の間をカンマで区切る．中身を操作することはできない．
dictionary:辞書型，{}を使って定義，各要素をキーと組み合わせて保存する．

## リスト
```python 
dist=[1,2,3] #listを定義する
print(dist)
print(dist[0]) #listの１番目を取得
dist[0:2] #スライスを使っている
```
リストにも，リストを操作するためのメソッドがたくさん用意されています．
```python
dist.append(4) #distに４を追加する
dist
```
```python
dist.pop() #一番最後（右）にあるものを取り出す
dist
```
「python リスト」で検索するとたくさんの情報が出てきます．


## タプル
```python
tup=(1,2,3)
tup
```
タプルはリストと違い，中身を操作することができません．ユーザに触らせたくないところ，絶対に変更しないところはタプルで定義すると良いでしょう．

## 辞書
```python
dic={'name':'名前'
    ,'age':'年齢'
    }
dic
```
辞書型はデータを追加することができます
```python
dic['fist_name']='苗字'#辞書型に追加
dic
```

辞書型もたくさんの操作方法があるはずです．
「Python 辞書型　操作」で検索！

***

# 8.例外処理
Pythonには例外処理として，try/exceptがあります．
例外処理というのは，プログラムの実行の継続を妨げる異常が発生した時に，その内容に応じて実行される処理のことで，例えばintを指定しているのに文字を入力した時には，エラーが発生します．
この説明でわかりにくいと思った人は調べてみてください．

サンプルコード:8_try_except.py
tryの中ではとりあえず実行し，tryの中でエラーが発生したらexcept文に移行します．
```python
while True:
	try:
		x = int(input('数字を入力:')
		break #これがないと無限ループになります．
	except:
		print('エラーが発生,もう一度入力してください')
```
上記のコードを実行し，数字と数字以外を入力してみてください．これで例外処理の動き方について掴めたでしょうか？エラーごとにもっと細かく場合分けすることもできます．
気になる方は調べてみてください．
「Python 例外処理」

***

# 9.関数
関数と聞いて何を思い浮かべますか？二次関数，一次関数などでしょうか．
プログラミングをやっていく上で，関数というのはとても便利で，使う機会が多いため大事な概念です．
それでは説明します．

サンプルコード:9_fanction.ipynb

みなさんは学校に行く日に何をしますか？
僕の場合で考えてみます．
1.起床
2.朝ごはんを食べる
3.歯磨きをする
4.着替える
ということをします．起床すると言っても何時に起きるか，朝ごはんと言っても何を食べるかなど，それぞれにも細かい決まりがありますよね．さまざまな処理を機能として一つにまとめているものを関数と言います．

また，上で1，2，3，4でそれぞれ関数を使ったら学校に行く日いがいもその機能を使うことができますよね？
友達と遊ぶ時も1，2，3，4を実行するはずです．そうなった時使いまわせると言ったところも便利ですし，関数の中に機能をまとめておくことで，他人が自分のコードをみた時にとてもわかりやすいといった利点があります．

それでは関数の書き方についてみていきましょう．

朝ごはんを食べるを例にコードを書いてみます.
```python
def breakfast(bread_or_rice): #関数を定義する． bread_or_riceは引数と呼ばれます．
	if bread_or_rice == 0: #0か1で判別
		print('bread')
	else:
		print('rice')

while True: 
	try:
		number = int(input('パンなら0，ご飯なら1を入力:'))
		if number == 0 or number == 1:
			breakfast(number)
			break #0か1が入力されたら結果を出力し終了
		else:
			print('0か1で入力してください．')
	except:
		print('数字で入力してください')

```
これが関数の一部です．
ここではまだ関数の**戻り値**という大事な概念を話していません．

***

関数では戻り値と引数というのがとても大切です．

三角形の面積を求める関数を考えてみます．
```python
def triangle(bottom=2,height=1): #bottom=2のようにすると，引数の初期値を持たせることができます．
	return bottom*height*0.5 #戻り値はreturnの後に記述する．

triangle_area1 = triangle() #引数には初期値があるので引数を指定しなくても使える．戻り値をtriangle_area1に入れる
print(triangle_area1)

triangle_area2 = triangle(10,2)
print(triangle_area2)
```
これを実行してみてください．
引数には初期値を持たせることができ，また，戻り値がある時は，その戻り値を受け取るための変数が必要です．

***

# 10.組み込み関数
先ほど，関数の使い方，定義の仕方をみましたね．
組み込み関数とはあらかじめpythonで定義された関数のことで，私たちは何も意識をすることなく使えます．
みなさんがずっと使ってきたprintも組み込み関数の一つです．

サンプルコード:10_builtin_functions.ipynb

```python
numbers = [1,3,5,6,9,2]
max_number = max(numbers)
print(max_number)
```
```python
min_number = min(numbers)
print(min_number)
```
ここでは最大値を求めるmaxと最小値を求めるminを使ってみました．
さっき私たちが作った関数を使う時もこのように使いましたよね？
Pythonではよく使う機能は既にもう定義されていて，呼び出すことで簡単に利用することができます．

他にもさまざまな組み込み関数が用意されています．以下のURLを参考にしてみてください．
https://docs.python.org/ja/3/library/functions.html



# 11.importの使い方
importとはなんだろうか．パッケージ，ライブラリ，モジュールを自分のコードに持ってくるために使うものです．

何千行もあるコードを読みたくないですよね？先ほどまでは関数ごとに機能を分けていましたが，機能ごとに.pyファイルを作成し，機能をファイルごとに作ることもできます．今回はその説明は割愛します．興味がある方は「python ファイル分ける」などで調べてみてください．

今回は，他の人が作ったパッケージ，ライブラリをimportで呼び出して使ってみます．

日時を呼び出すdatetimeをインポートしてみます！
```python
# https://note.nkmk.me/python-datetime-usage/
import datetime 

dt_now = datetime.datetime.now()
print(dt_now)

print(type(dt_now))

print(dt_now.year)

print(dt_now.hour)datetimeのdateを呼び込み
```
importを用いて，誰かが使ったものを自分のプログラムに組み込むことで，便利な機能をすぐに実装することができます．
importを用いて呼び出せるものには，ライブラリ，パッケージ，モジュールがあります．
次の章では分野別に便利なライブラリ,パッケージを集めて列挙します．


```python
import datetime as dt
dt_now = dt.datetime.now()
```
のように，asをつけることで，名前を短くすることができる．結構使います

これでも全然説明が足りないくらいです．

追加で必要な知識がありそうだなーって時は検索して見てください．

***


# 12.便利なツール，ライブラリ，パッケージ等
ここで列挙しているものの説明は省きます．なぜならそれまでも説明していたら入門ではないように思うからです．Pythonの入門というのは，変数を定義して，繰り返し，条件分岐ができるところまでだと考えているからです．逆に言えば，それらができるようになったら，ここにあるライブラリ等をうまく使い，希望のツールを作り出すことが可能です．

名前を聞いただけではわからないと思うので，興味がある分野があれば「Python 分野名(例えばWeb)」や「Python ライブラリ名(Django)」とかで調べると，それぞれの使い方を検索することができます．
## Web
Herokuと組み合わせて使うことで簡単にサービス公開とかできます！

### Django
Djangoは大規模開発に向いてるフレームワーク
自分のポートフォリオはDjangoで作りました．
まだまだ大規模なWeb作ったことないので個人的な範囲内の利用だとFlaskでいいかなってことが多かった．

portfolio: http://www.fu-te.jp/

### Flask
Flaskは軽量フレームワーク，すぐに開発できる
稲が健康かどうかを深層学習で求めるシステム作った時に，FlaskでWeb上から使えるようにしたー．めっちゃ早く作れる．

稲健康判別: https://github.com/Fu-Te/ine_disease_diagnosis

## 科学計算
### Numpy
機械学習とか画像分類をするときの画像処理とかで使う．
行列作って〜みたいな時にめっちゃ便利だし早い．

### Scipy
プログラミング数学，科学，工学のための数値解析に便利
配列とか行列の演算に使う，時計とか高度な数学的計算が簡単にできる．

## グラフ作成
ここは結構好みが分かれるところ．Kaggle(機械学習，データサイエンス)やる人がよく使う！
８割くらいの人はmatplot使ってるかも？
個人的にはseabornが好きです．

### matplotlib
こっちがメジャーです
### seaborn
わかりやすく作れし，綺麗に作れる！僕の好みはこっち！
***
## 機械学習・深層学習
最近の流行りのコレ．
Pythonだとライブラリがいっぱいあってすぐに実装できる．

### scikit-learn
機械学習モデルで，色々な機械学習の手法が使える．
訓練データ，テストデータの分割もコレでやる！
あとは，データを標準化する時も使う．

### statsmodels
統計解析ソフトで，最小二乗法とか加重最小二乗法とかやる時に使う．

### PyTorch
ディープラーニングを実装するためのライブラリ．
FacebookのAIグループによって開発された．
自然言語処理で使われる．
define by run方式っていうのをとっていて，直感的にRNNを書くことができて，デバックが容易だったりする．

### TensorFlow
Googleが開発したやつ
ディープラーニングを実装するためのライブラリ
大規模データセットとか，パフォーマンスが高い方がいいとか，物体検出によく使うイメージ．

### Keras
最近はTensorFlowの中に組み込まれたやつ．
コードがめっちゃシンプルでモデル作成に時間がかからない！
***
## ファイル，フォルダ操作
### os
OSに依存している様々な機能が利用できる．ディレクトリ，ファイル操作ができたり，ファイルの一覧を取得したりできる．ファイル作成も可能．
osでファイル一覧を取得して，for文で1つずつ読み込んだりできたのが便利だと感じた．それにファイル名が複雑な時とか，打ち間違いとか無くなってとても良い

### Pathlib
ファイルやフォルダ操作が可能

### OpenPyXL
Excel操作ができる

### requests
htmlデータ取得とかできる．

### Selenium
動的ページのスクレイピングに向いてる

### Beautiful soup
スクレイピングがしたい時に結構使う

### Pandas
Excel，CSVデータ加工する時によく使う．Kaggleとかやる人は必修

### subprocess
Pythonのプログラムから他のアプリを実行したり，実行結果を取得するためのモジュール．
コマンドを実行したり，外部ファイルを実行したりできる

## GUI，デスクトップアプリ
Pythonでデスクトップアプリを作りたいときはここら辺が便利．

### Tkinter
シンプルな文法で作れて，起動も早い
Pythonの中で一番人気が高いGUIライブラリだと思う

### PySimpleGUI
2018年から開発が始まったらしい！
こっちもGUIを作るのに便利なライブラリ
***
## ネットワーク系
### scapy
CTFでよく使われる．幅広いプロトコルに対応したパケット操作プログラム．
パケット解析とかもできる

### socket
低水準ネットワークインターフェース．
ソケット通信を実装するときとかに使う．
サーバークライアント間の通信とか
TCP,UDP通信系

### telnetlib
Telnetプロトコルを実装しているtelnetクラスが提供される．
サーバやネットワーク機器の情報をexpectコマンドを使って取得可能

### Netmiko
ssh接続とかする時に使う
まだ使ったことがないので，使ってみたら追記
ファイル転送も可能
リモート機器に接続して，操作の補助をする
ログイン，ログアウト，モード移行，ページング設定コマンド
Cisco,Juniper,Palo Alto,Dell,Linuxに対応

### NAPALM
Arista,Cisco,Fortinet Fortios,IBM,Juniper,Mikrotic RouterOS等に対応している．
ネットワーク機器に対して何かをすると言った感じ
ARPテーブルの取得や，MACアドレステーブル，ルーティング情報，環境情報の取得，装置情報の取得等ができる

## 非同期処理
### asyncio
シングルスレッド下で動作し，試行した複数の処理は順次に処理され，IO待ち時間にぶつかると実行可能な別の処理を実行すると言う感じに，無駄なIO待ち時間を有効活用すべく，別の処理を割り当てるらしい．

***

# 13.おわりに
僕が，プログラミングを始めた時は，高校生であり，周囲にプログラマの人はいませんでした．どうやってプログラミングを学んでいけば全くわからなかった．でもプログラミングを始めて5-6年たち，プログラミング力とは，検索する力なんだろうな，と思うようになった．
エラーが出た時，調べてなんでエラーなのかを考え，解決策を考える．
ツールの使い方を自分で調べる．
本書では必要最低限の説明にとどめ，読者に自分で検索してもらうことをメインに構成してみました．ネットを使って調べて解決策を探す．それこそが現代一番大切な力なのではないかと私は考えている．
本書はプログラミングをしたことがない人を対象に作成し，プログラミングの概念を伝え，その概念を頭に入れてもらい，概念を知っていれば検索をすることができるようになる．
知らないことを調べることはできないが知っていることを調べることはできる．これを胸にプログラミングを楽しんでほしいと思う．

# 14.基礎を習得したら．．．
機械学習に興味がある人: KaggleやNishika
アルゴリズム: AtCoderやPaiza

