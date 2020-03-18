# Gitチートシート

## （基本）変更をpushするまでの流れ

変更されているファイルを確認する

```
git status
```

リモートリポジトリの変更を取り込む

```
git pull origin ブランチ名
```

全てのファイルをインデックスする

```
git add .
```

コミットする

```
git commit -m "コミットメッセージ"
```

（masterに）プッシュする

```
git push origin master
```

## （基本）その他の操作

クローンする

```
git clone リポジトリ名
```

初期化（これでgitが使えるようになる）

```
git init
```

ブランチの作成

```
git branch ブランチ名
```


ブランチ名の変更

```
git branch -m ブランチ名
```


ブランチの削除

```
git branch -d ブランチ名
```


ブランチの削除（強制）

```
git branch -D ブランチ名
```

ブランチの切り替え

```
git checkout ブランチ名
```

ブランチを作成し切り替える

```
git checkout -b ブランチ名
```

ファイルの差分を見る

```
git diff ファイル名
```

現在のブランチと指定ブランチごとの差分を見る

```
git branch ブランチ名
```

マージする

```
git merge ブランチ名
```

## 使えると便利なコマンド

変更内容を前コミットに追加
またはコミットメッセージを編集

```
git commit --amend
```

メッセージ編集なしでコミット追加

```
git commit --amend --no-edit
```

ステージとの差分を表示

```
git diff --staged
```

スタッシュする（変更内容を別の場所に一時的に保存）

```
git stash
```

スタッシュ解除する

```
git stash pop
```


ログを確認する

```
git log
```

コミットの詳細を確認する

```
git show コミットID
```

## 間違えた時のリカバリー

バージョン管理対象から外したい
```
git rm --cached ファイル名
```

`git add`を間違えた

```
git reset HEAD .
```

`git commit`を間違えた（変更ファイルはとっておきたい）

```
git reset --soft HEAD^
```

`git commit`を間違えた（変更ファイルも消したい）

```
git reset --hard HEAD^
```

## 新人に使わせたくないコマンド

強制プッシュ

```
git push -f origin ブランチ名
```

ブランチ指定なしpull

```
git pull
```
