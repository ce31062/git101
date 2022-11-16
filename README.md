# GitHubの実用的な基本操作を学ぶ (git101)
<img src="https://user-images.githubusercontent.com/74296872/202144653-5a875fd1-c2db-47d4-83b1-796039b66f58.png" width="800">

## 作業ツリーの内容をリモートリポジトリに送る
1.作業ツリーの内容をリポジトリまでの中間領域にコピーする（ステージする)<br>
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
