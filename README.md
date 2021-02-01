### A:GitHub上にリモートリポジトリを用意する

1. ブラウザで[GitHub](https://github.com/)にアクセスし、右上の+マークを押して「New repository」を選択する。

![リモートリポジトリを作成1](img/1-a.jpg)

2. Repository name（リポジトリ名）を入力する。今回は「Practice」にした。必要ならばDescription（説明文）も入力する。その下のラジオボタンはPublicを選択し、Create repositoryをクリックする。

|選択肢|内容
|--|--
|Public|誰もが閲覧可能な公開リポジトリを作成する
|Private|許可した人しか見られない非公開リポジトリを作成する

![リモートリポジトリを作成2](img/1-b.jpg)

3. Git Bashを起動し、任意の場所にPracticeディレクトリを作成し移動する。git initでローカルリポジトリを作成し、git remote addでリモートリポジトリの設定を行う。リモートリポジトリのURLは、Codeタブ内のQuick setupで確認できる。

```
$ mkdir Practice
$ cd Practice
$ git init
$ git remote add origin <リモートリポジトリのURL>
```

![リモートリポジトリを作成3](img/1-c.jpg)
![リモートリポジトリを作成4](img/1-d.jpg)

4. Practiceディレクトリ内でindex.htmlを作成し、以下の内容で保存した。

![リモートリポジトリを作成5](img/1-f.jpg)

5. git addコマンドでindex.htmlをコミット対象に設定する。その後、git commitコマンドでコミットする。このとき、-mオプションでコミットメッセージが設定できる。

```
$ git add index.html
$ git commit -m "create index.html"
```

6. git pushコマンドでプッシュを行う。

```
$ git push origin master 
```

![リモートリポジトリを作成6](img/1-h.jpg)

7. リモートリポジトリにindex.htmlが存在することを確認する。

![リモートリポジトリを作成7](img/1-i.jpg)
![リモートリポジトリを作成8](img/1-j.jpg)

### A:Bをコラボレーターとして招待する

1. Settingタブに切り替え、左側のメニューからManage accessをクリックする。次にInvite a collaboraterをクリックする。

![コラボレーターの招待1](img/1-k.jpg)

2. 招待したい人(B)のユーザー名を入力すると、該当するユーザーが表示されるのでクリックする。その後、緑色のボタンをクリックする。

![コラボレーターの招待2](img/1-l.jpg)

3.招待したユーザー(B)にメールが届くので、正体を受けてもらうと正式にコラボレーターになる。

![コラボレーターの招待3](img2/01.jpg)
![コラボレーターの招待4](img2/02.jpg)
![コラボレーターの招待4](img2/03.png)

### A:Bのプルリクエストをマージする

1. Pull requestsタブを選択し、開きたいプルリクエストをクリックすると、選んだプルリクエストが表示される。

![プルリクエスト1](img/3-b.jpg)
![プルリクエスト2](img/3-c.jpg)

2. Commitsタブや、Files changedタブで変更点を確認する。 

![プルリクエスト4](img/3-e.jpg)
![プルリクエスト3](img/3-d.jpg)

3. 問題がない場合は、Merge pull requestをクリックし、コミットメッセージを入力してConfirm mergeをクリックする。

![プルリクエスト2](img/3-h.jpg)
![プルリクエスト5](img/3-f.jpg)

4. これで、マージコミットが追加された。

![プルリクエスト6](img/3-g.jpg)

### Aの作業

1. git pullコマンドで、ローカルリポジトリにリモートリポジトリのデータを取り込む。

```
$ git pull origin master
```

![git pull](img/4-1.jpg)

2. index.htmlに変更を加える。ここでは、13行目にdivタグを追加した。

![index.htmlに追記する](img/4-2.jpg)

3. git addコマンドでindex.htmlをコミット対象に設定する。次に、git commitコマンドでコミットする。そして、git pushコマンドでプッシュする。

```
$ git add index.html
$ git commit -m "update index.html"
$ git push origin master
```

![pushする](img/4-3.jpg)

