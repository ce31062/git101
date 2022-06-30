# リモートリポジトリ(GitHub)にpushする基本操作を学ぶ

## 作業ツリーの内容をリモートリポジトリに送る
1.作業ツリーの内容をリポジトリまでの中間領域にコピーする（ステージする)
既にプロジェクトのファイルやディレクトリが作業ツリーにあるなら、作業ツリーのトップで以下のコマンドを実行。<br>
プロジェクトの全てのファイルとディレクトリをGitの管理下に置くことができる。<br>
※管理したくないファイルやディレクトリも含まれるので注意
```
git add .
```
2.ステージの内容をリポジトリにコミットする<br>
-mオプションによって、コメントメッセージを簡単に設定することができる。<br>
```
git commit -m "Add test.txt"
```
3.ローカルリポジトリでコミットした内容をリモートリポジトリに送る。(プッシュする)<br>
```
git push origin master
```
## リモートの更新を取得してローカルブランチに反映する
1.リモートリポジトリにあるコミットをローカルリポジトリに取得する<br>
```
git fetch origin master
```
2.リモート追跡ブランチ(origin/master)をローカルブランチ(master)に早送りマージする<br>
まず、masterをチェックアウトする。<br>
```
git checkout master
```
リモート追跡ブランチを早送りマージする。<br>
```
git merge--ff-only origin/master
```
