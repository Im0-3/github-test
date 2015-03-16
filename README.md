# github-testttt
git練習用のリポジトリ

## ３段階のファイル状態について
### 作業ディレクトリ
変更を加えた作業中のファイル群  
作業ディレクトリからステージングエリアへ登録する場合  
```
git add
```

### ステージングエリア
次のcommitに含めるファイル群
作業内容を確定させGitディレクトリへ登録する場合  
```
git commit
```

### Gitディレクトリ
変更が確定したファイル群

## ブランチについて
* 同時にプロジェクトを進める際にはブランチを作って、同時に開発を行う  
* 修正を繰り返して、最後にブランチをマージ（合体）する  
* Gitはブランチの作成が高速、マージが簡単  
* Gitはブランチを作成する際、ブランチ名をコミットと関連づける
* マージする際は共通の親コミットまで遡り、現在のファイルと比較してマージを行う


## ファイルをステージングエリアへ移動する
コマンドラインでファイルの状態を確認するには
```
git status
```

ファイルをステージングエリアに移動するには
```
git add filepattern
```

filepatternにはファイル名やディレクトリ名が入る  
(例)

* css/ （cssディレクトリ内のファイル）  
* *.js （jsファイル全て）

ステージングエリアにファイルを移動してから
```
git status
```
を実行すると以下のように表示される

```
On branch master
Your branch is up-to-date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

	modified:   README.md
```

## コミット
以下を実行
```
git commit -m "メッセージを入力"
```

コミットが成功したら、以下を実行して履歴を確認してみる
```
git log
```

## PushしてGithubに反映する
変更した内容をGithubリポジトリに反映させるにはgit pushを実行する
```
git push <リモート名> <ブランチ名>
```

pushする際はリモート名・ブランチ名を指定する
通常clone元はorigin、デフォルトのブランチははmaster
```
git push origin master
```

## .gitignoreについて
.gitignoreというファイルをプロジェクトのトップのディレクトリに保存すると、バージョン管理しないようにできる。
