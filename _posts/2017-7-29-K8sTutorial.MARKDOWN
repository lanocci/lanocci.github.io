---
layout: post 
title:  "k8s公式チュートリアルで詰まったところ"
date:   2017-07-29 23:00:00 -0600
categories: kubernetes tech note
---
# Kubernetes 公式チュートリアルをローカル環境で進める上で詰まったこと
interactive tutorialということでオンラインでコマンドラインツールを試すこともできるが、あえてローカルでやったときに詰まったところをメモ

## Module 2

### Step 2/3

- `kubectl run`するところでdockerhubからイメージを取ってくるが、dockerhubのurlが古いためか取ってこれない。
- 掲載されているコマンドの代わりに以下のコマンドを実行するとうまくいく
- `kubectl run kubernetes-bootcamp --image=jocatalin/kubernetes-bootcamp:v1 --port=8080`
- urlの`docker.io/`を削っただ201~け
