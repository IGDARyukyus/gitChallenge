# IGDA Ryukyus Git Challenge

## 目的

Gitコマンドを覚えるためのリポジトリです。
好きにPullRequestを飛ばしてもらってOKです。

# 手順

- このリポジトリをForkしましょう
- ForkしたリポジトリをPCにCloneしましょう
- Cloneしたものをmasterからブランチを切りましょう
- Readmeの作業メンバーに自分の名前を記述します
- commitして自分のリモート先のリポジトリにpushします
- github上でpullRequestを作ります
- レビューが通ればマージします

# 作業ディレクトリを最新にする

- masterブランチに移動
- .git/configを以下の例のように修正

```diff
[core]
  ...(色々記述してある)
[remote "origin"]
  url = git@github.com:kazumalab/gitChallenge.git
  fetch = +refs/heads/*:refs/remotes/origin/*
+ [remote "igda"]
+   url = git@github.com:IGDARyukyus/gitChallenge.git
+   fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
  ...(色々記述してある)

```

- masterでpullして最新にします

```sh
$ git pull igda master
```

- すでにbranchを作って作業している場合はbranch側も更新します

```sh
$git checkout <your-branch>
$git rebase master

# コンフリクトがある場合
# branch名が<2knk3k>みたいに番号ブランチになる
# コンフリクト修正後

$git add <confilict file>
$git rebase --continue
```

- 最後にフォークしたremote(github)先へPushします

```sh
$ git push origin master
```

# 作業した人

[@kazumalab](https://github.com/kazumalab)

