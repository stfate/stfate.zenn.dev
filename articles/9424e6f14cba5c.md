---
title: "Python 3.11でnumbaのインストールに失敗する問題"
emoji: "🌊"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [Python]
published: true
---

Python 3.11でnumbaのインストールに失敗する問題
======

# 問題

Python 3.11系で`pip install numba`したときにインストールに失敗する．
![](/images/20230421PipNumbaInstallError.png)


# 原因

numbaの安定版(0.56.4)がPython3.11に対応していないのが原因っぽい．
[numba/numba Python 3.11 #8304](https://github.com/numba/numba/issues/8304)


# 対処法

Python 3.11に対応しているRC版を入れる．

```bash
pip install --pre numba
```

![](/images/20230421PipNumbaInstalled.png)

これでようやく3.11系に移行できる……
