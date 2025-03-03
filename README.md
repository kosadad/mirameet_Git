

# mirameet_Git
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**目次**

- 【Chapter 1】VisualStudioCodeでGit操作
- 【Chapter 2】コンフリクトの対処法について

<!-- END doctoc generated TOC please keep comment here to allow auto update -->


***
# 【Chapter 1】VisualStudioCodeでGit操作 


### ⑴クローンする
1.<>CodeタブのCodeからURLをコピーする。
![スクリーンショット 2021-07-13 135828](https://user-images.githubusercontent.com/60914189/125394037-f73d4080-e3e3-11eb-9292-67ba978ae302.png)


今回はC:\User\ユーザーネームにクローンします。
<br>他の場所にクローンしたい方は”cd 任意のパス”で移動してからクローンしてください。



```
$ git clone コピーしたURL
```
![image](https://user-images.githubusercontent.com/60914189/125255343-488ef680-e336-11eb-8b05-8878a72219a4.png)
下記のような結果が返ってきたらクローンされています。
![image](https://user-images.githubusercontent.com/60914189/125255384-517fc800-e336-11eb-9c35-79ac33a27a54.png)


### ⑵ブランチを作成する
任意のブランチ名（今回はfeature1)を入力してCreate branch:octo-branchを押下する


![スクリーンショット 2021-07-13 141356](https://user-images.githubusercontent.com/60914189/125394410-9c581900-e3e4-11eb-9040-1cdda0f71544.png)


ブランチがfeature1になっていることを確認してindex.htmlの中身を書き換える
![スクリーンショット 2021-07-12 173359](https://user-images.githubusercontent.com/60914189/125256520-7a548d00-e337-11eb-9d05-3dee75ef5a03.png)

Visualstudiocodeを起動し、OpenFolderを押下


![スクリーンショット 2021-07-12 173603](https://user-images.githubusercontent.com/60914189/125257010-f3ec7b00-e337-11eb-9884-0818a82ee859.png)


### ⑶クローンしてきたプロジェクトをVscodeで開く
先ほどクローンした場所まで移動

“mirameet_Git”を押下し、”フォルダー”に反映されたことを確認したら”フォルダーの選択”を押下
![スクリーンショット 2021-07-12 174254](https://user-images.githubusercontent.com/60914189/125257696-a1f82500-e338-11eb-8aaf-3a61f80c3297.png)




### ⑷Gitの基本設定をする
TerminalタブからNewterminalを押下し、VScodeのターミナルに下記コマンドを入力する。
```
git config –-global user.name “ユーザー名”
git config –-global user.email ”メールアドレス”
```
![スクリーンショット 2021-07-13 141729](https://user-images.githubusercontent.com/60914189/125394723-14264380-e3e5-11eb-93c3-90daf8665c02.png)

“git init”と入力し、クローンしてきたリポジトリを初期化する
![スクリーンショット 2021-07-13 141915](https://user-images.githubusercontent.com/60914189/125394885-5780b200-e3e5-11eb-9779-4a7f47298eeb.png)

### ⑸文言を書き換える
index.htmlを開き14行目の「【Git入門】　Gitの使い方を理解しよう」を
<br>「【Git入門】　文言を書き換えてみよう」に変える
![スクリーンショット 2021-07-13 142040](https://user-images.githubusercontent.com/60914189/125395022-8e56c800-e3e5-11eb-8612-ecb74536a574.png)

### ⑹変更を保存する
書き変えたらCtrl+Sで保存する。未保存の場合は変更したファイル名に”●”がつく
![スクリーンショット 2021-07-13 142148](https://user-images.githubusercontent.com/60914189/125395105-b0e8e100-e3e5-11eb-996b-e0433bea0542.png)


### ⑺ステージングを行う
1.VSCodeでステージングを行うので左側のソース管理アイコンをクリックしてGitメニューを開く
![スクリーンショット 2021-07-13 142237](https://user-images.githubusercontent.com/60914189/125395171-cb22bf00-e3e5-11eb-8b67-ce3abfeb558d.png)

2.ソース管理アイコンを押したら、ファイル右にある「＋」を押下する
![スクリーンショット 2021-07-13 142333](https://user-images.githubusercontent.com/60914189/125395275-ed1c4180-e3e5-11eb-8f1f-25ab58f0a164.png)

3.Staged Changesに書き換えたファイルが入る。ここで変更点を確認出来る。
![スクリーンショット 2021-07-13 142427](https://user-images.githubusercontent.com/60914189/125395365-10df8780-e3e6-11eb-9cf8-4b6833614ebc.png)

4.ステージングを行うとStaged Changesが表示されなくなる
![スクリーンショット 2021-07-13 142523](https://user-images.githubusercontent.com/60914189/125395460-2fde1980-e3e6-11eb-9151-9745a495ac83.png)

### ⑻コミットを行う
Messageにコメントを記入し、メニュー上部にある“✓”アイコンを押す。
<br>“✓”はコミットアイコン
![スクリーンショット 2021-07-13 143219](https://user-images.githubusercontent.com/60914189/125396168-286b4000-e3e7-11eb-8203-82dc50dcd36c.png)

### ⑼ローカルリポジトリとGitHubのリポジトリを紐づけを行う
1.コミットしたいリポジトリのURLをコピーする（一番最初にコピーしたのと同じURL）
![スクリーンショット 2021-07-13 143219](https://user-images.githubusercontent.com/60914189/125396278-4c2e8600-e3e7-11eb-9e35-6795f3690817.png)

2.現在のローカルリポジトリにリモートのリポジトリを追加する(下記コマンドを使用)
```
git remote add origin https://github.com/hinanotea/mirameet_Git.git
```
![スクリーンショット 2021-07-13 143738](https://user-images.githubusercontent.com/60914189/125396770-f1495e80-e3e7-11eb-90a5-44b3bffa58f5.png)

リモートリポジトリの名前と場所を表示し、実際にリモートリポジトリに紐づいたのか確認する
```
git remote –v
```
”fatal: remote origin already exists”というエラーが出たら下記コマンドを
<br>実行し一度originを削除してから再度登録
```
git remote rm origin
```
### ⑽ブランチの作成と移動
Git branchを入力し現在のブランチを確認する。defaultのブランチのみ（mainまたはmaster)だったら新規でブランチを作成する。

![スクリーンショット 2021-07-13 143918](https://user-images.githubusercontent.com/60914189/125396877-205fd000-e3e8-11eb-8095-e233c662285d.png)

今回はfeature1というブランチを作成し、feature1に移動する。
下記コマンドでブランチを作成。
```
git branch feature1
```

ブランチを移動するコマンド
```
git checkout feature1![image](https://user-images.githubusercontent.com/60914189/125397003-4d13e780-e3e8-11eb-9e17-f9b086ff23a1.png)
```
git branchと入力した際に緑色の文字になっているのが現在指定しているブランチ


### ⑾feature1ブランチにプッシュ
下記コマンドを使用し、feature1ブランチに対するプッシュ操作を行う
```
git push –u origin feature1
```
![スクリーンショット 2021-07-13 144323](https://user-images.githubusercontent.com/60914189/125397303-b693f600-e3e8-11eb-891b-e24193f50dae.png)

### ⑿変更内容がGitHubに反映されたかの確認をする
index.htmlの中身と最終更新日時を確認する。反映されていない場合はF5キーで更新し再度確認する。

![スクリーンショット 2021-07-13 144714](https://user-images.githubusercontent.com/60914189/125397688-3ae67900-e3e9-11eb-9e56-c2b3d19d5e89.png)


画面上部に”feature1 had recent pushes 1 minute ago”のようなメッセージが表示されるのでCompare&pull requestを押下

### ⒀プルリクエストを作成する
![スクリーンショット 2021-07-13 144802](https://user-images.githubusercontent.com/60914189/125397772-5baece80-e3e9-11eb-91f4-6f60ba53dd86.png)

### ⒁変更内容の確認
変更内容の確認を見てみましょう。

![スクリーンショット 2021-07-13 144951](https://user-images.githubusercontent.com/60914189/125397940-99abf280-e3e9-11eb-8fea-3148941244b4.png)

### ⒂ソースコードの確認（レビュアー側の操作）
「Pull requests」タブを開き、「Files changed」からソースコードを確認する。
![スクリーンショット 2021-07-13 145119](https://user-images.githubusercontent.com/60914189/125398074-ceb84500-e3e9-11eb-9ef1-b1de8e26c547.png)


### ⒃コメントを記載（レビュアー側の操作）
コメントしたい箇所にカーソルをあてると青い”＋”アイコンが出てきて
<br>コメントが記載出来るようになるので必要に応じてコメントを記載する

![スクリーンショット 2021-07-13 145245](https://user-images.githubusercontent.com/60914189/125398261-0de69600-e3ea-11eb-9d81-0cc5c9a4950b.png)

記載したら”Start a review”を押下する

### ⒄マージする（レビュアー側の操作）
内容に問題がなければ、「Conversation」の「Merge pull request」をクリックしてレビューを完了する。
![スクリーンショット 2021-07-13 145418](https://user-images.githubusercontent.com/60914189/125398399-3a9aad80-e3ea-11eb-992b-234151de16ba.png)


### ⒅プルする（レビュアー側の操作）
マージした内容（ここでは login.html ）をローカルリポジトリの master に取得し、最新化する必要がある。
<br>この場合、 プル（pull） という操作を行うことで、リモートトリポジトリから変更内容を取得することができる

![スクリーンショット 2021-07-13 152519](https://user-images.githubusercontent.com/60914189/125401792-96673580-e3ee-11eb-9fd1-9f61cd2c2177.png)


デフォルトブランチに切り替える
```
git checkout master
```
プルする
```
git pull
```
### ⒆ディレクトリ内の確認をする（レビュアー側の操作）
lsコマンドを実行すると、index.html を確認することができる。
![スクリーンショット 2021-07-13 152632](https://user-images.githubusercontent.com/60914189/125401911-bb5ba880-e3ee-11eb-85ab-f79405a03cb7.png)



### ⒇全作業の変更履歴を確認をする（レビュアー側の操作）
git log コマンドを入力することで、これまでの全作業の変更履歴を確認もできる
![スクリーンショット 2021-07-13 152802](https://user-images.githubusercontent.com/60914189/125402064-ee9e3780-e3ee-11eb-8b0b-44fc36fcd97c.png)

### 修正箇所の確認をする（レビュアー側の操作）
Masterブランチでのindex.htmlで先ほど書き換えた場所が確認出来る。
![スクリーンショット 2021-07-13 153002](https://user-images.githubusercontent.com/60914189/125402315-3a50e100-e3ef-11eb-9a7d-03027cdc7d90.png)



# 【Chapter 2】コンフリクトの対処法

### ⑴新規でブランチを作成
1.  VisualStudioCodeのブランチが表示されているところをクリックし、ブランチ作成
![スクリーンショット 2021-07-12 153032](https://user-images.githubusercontent.com/60914189/125241195-1ecdd380-e326-11eb-8cb0-1b67b4ce66ac.png)


ブランチ名は下記を入力
```
feature2
```
2. ブランチ名がfeature2になったのを確認しましたら再度index.htmlに修正を加えます。
![スクリーンショット 2021-07-12 154901](https://user-images.githubusercontent.com/60914189/125243198-baf8da00-e328-11eb-9ddb-20dcf51affc1.png)

### ⑵index.htmlを修正
1.ブランチ名がfeature2になっているのを確認。再度index.htmlに修正を加えます。

2.以下のソースをindex.htmlの31行目以降に挿入します。
挿入後上書き保存を行いローカルの修正を確認しましょう。
```
<h1>【Git入門】 コンフリクトを理解しよう</h1>
```
![スクリーンショット 2021-07-12 154425](https://user-images.githubusercontent.com/60914189/125242781-170f2e80-e328-11eb-9715-54c4ad45b955.png)

### ⑶コンフリクトを起こしてみる
1.ここでコンフリクトを発生させるためにindex.htmlをGitHub上で直接編集したいと思います。
<br>GitHubを開き、index.htmlをクリックして下さい。

![スクリーンショット 2021-07-12 155402](https://user-images.githubusercontent.com/60914189/125243758-79b4fa00-e329-11eb-8fd9-d94548675985.png)


2.index.htmlが表示されましたら右上のペンのマークの”Edit this file”をクリックし編集できるようにします。
![スクリーンショット 2021-07-12 160724](https://user-images.githubusercontent.com/60914189/125245307-6145df00-e32b-11eb-9d05-840f8716644b.png)

3.先ほどと同じ32行目に以下の文言を追加します。
```
<h1>【Git入門】 コンフリクトは注意が必要です。</h1>
```
![スクリーンショット 2021-07-12 160928](https://user-images.githubusercontent.com/60914189/125245491-981bf500-e32b-11eb-8935-7094f250cd2c.png)

4.Commit changesをクリックし修正をコミットします。
![image](https://user-images.githubusercontent.com/60914189/125245636-c568a300-e32b-11eb-9fa2-2d500df566d1.png)

5.Commit changesをクリックし修正をコミットします。


![スクリーンショット 2021-07-12 160928](https://user-images.githubusercontent.com/60914189/125245809-f8129b80-e32b-11eb-826c-730a0720ffb7.png)
これでmasterブランチのソースには32行目に文言が入った状態になりました。

6.Vscodeに戻り、先ほどの修正をpullしてみましょう。

ソースを保存した状態で左側メニューの＋マークをクリックし
修正をステージにあげます。
![スクリーンショット 2021-07-12 161928](https://user-images.githubusercontent.com/60914189/125246769-2e9ce600-e32d-11eb-9ebd-86639f825240.png)

7.ステージにあげた修正をコミットします。 

✓マークをクリックし「文書を追加」と入力しEnterキーを押します。
![スクリーンショット 2021-07-12 162156](https://user-images.githubusercontent.com/60914189/125246883-4c6a4b00-e32d-11eb-8ce7-d1d98a71a8e9.png)

8.Pushを行う
…マークを押しメニューを出しその中のプッシュを選択します。
<br>ブランチの公開が確認されるのでOKボタンをクリックします。
![image](https://user-images.githubusercontent.com/60914189/125247038-79b6f900-e32d-11eb-8a8e-0664920d3797.png)


![image](https://user-images.githubusercontent.com/60914189/125247055-7cb1e980-e32d-11eb-9c81-fba1fad454f5.png)


### ⑷コンフリクトの対処について
1.GitHubに戻りプルリクエストを作成していきます。
Compare & pull requestキーをクリックします。
![image](https://user-images.githubusercontent.com/60914189/125247414-e205da80-e32d-11eb-8722-82b5c3c725df.png)

2.Create pull requestキーをクリックします。
![image](https://user-images.githubusercontent.com/60914189/125247477-f3e77d80-e32d-11eb-981b-312a6c5c65a9.png)

3.コンフリクト解消
Pullリクエストが作成されましたが先ほどと違いコンフリクトが発生しております。
<br>このままでは修正を反映できませんので、コンフリクトの解消を行いましょう。
![スクリーンショット 2021-07-12 162831](https://user-images.githubusercontent.com/60914189/125247749-3d37cd00-e32e-11eb-9556-1628a0fc5c09.png)
赤枠部分で上がfeature2、下がmasterでの状態を表示しています。
<br>今回はfeature2の内容で反映していきたいと思いますので33行目だけを残すように修正します。

![スクリーンショット 2021-07-12 162934](https://user-images.githubusercontent.com/60914189/125247903-68222100-e32e-11eb-9c02-b843e598ccb7.png)

修正後にMark as resolvedを押下し修正を反映します。
コミットが出来るようになりますので
Commmit mergeでコミットします。



![image](https://user-images.githubusercontent.com/60914189/125247933-6f492f00-e32e-11eb-9952-f55652bbdff7.png)

![image](https://user-images.githubusercontent.com/60914189/125247966-7a03c400-e32e-11eb-8259-82a53471aef9.png)

コンフリクトが解消したので、再度プルリクエストを作成します。
<br>Merge pullrequestをクリックします。


![image](https://user-images.githubusercontent.com/60914189/125247985-825bff00-e32e-11eb-97a1-b51b5416eaa4.png)





プルリクエストが正常に作成できました

