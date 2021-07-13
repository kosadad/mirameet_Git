# mirameet_Git  Git超入門



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

![スクリーンショット 2021-07-12 173359](https://user-images.githubusercontent.com/60914189/125256520-7a548d00-e337-11eb-9d05-3dee75ef5a03.png)

ブランチがfeature1になっていることを確認してindex.htmlの中身を書き換える
Visualstudiocodeを起動し、OpenFolderを押下
![スクリーンショット 2021-07-12 173603](https://user-images.githubusercontent.com/60914189/125257010-f3ec7b00-e337-11eb-9884-0818a82ee859.png)


### ⑶クローンしてきたプロジェクトをVscodeで開く
先ほどクローンした場所まで移動

“mirameet_Git”を押下し、”フォルダー”に反映されたことを確認したら”フォルダーの選択”を押下
![スクリーンショット 2021-07-12 174254](https://user-images.githubusercontent.com/60914189/125257696-a1f82500-e338-11eb-8aaf-3a61f80c3297.png)




### ⑷Gitの基本設定をする

### ⑸文言を書き換える

### ⑹変更を保存する

### ⑺ステージングを行う


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

"はい"をクリック

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

