# try-aws-eks

AWS EKS を試してみる。  
EKS on Fargate で nginx サーバを起動してみる。  

## ツールインストール

eksctl, kubectl をインストール。  
Homebrew で eksctl を入れれば kubectl も一緒に入る。  

```sh
brew tap weaveworks/tap
brew install weaveworks/tap/eksctl
```

## クラスタ作成

クラスタを作成。  
10〜20分くらいかかる。  

```sh
eksctl create cluster -f cluster.yml
```

## クラスタ削除

後始末。  
10〜20分くらいかかる。  

```sh
eksctl delete cluster -f cluster.yml -w
```
