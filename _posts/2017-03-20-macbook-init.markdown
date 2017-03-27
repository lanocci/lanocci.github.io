---
layout: post
title:  'MacBook Pro 13" Late 2016 購入後にやったこと'
date:   2017-03-20 06:56:38 +0900
categories: jekyll update
---
# MacBook Pro 13" Late 2016 購入後にやったこと

## [Homebrew](http://qiita.com/b4b4r07/items/6efebc2f3d1cbbd393fc)

## Better Touch Tool

## Emacs

- howm のインストールがうまくいかない。 -> うまくいった
- `~/.emacs.d/` ディレクトリの下に`conf`ディレクトリを作成しないとassertion failedエラーが発生するので注意

## marked2

[emacs + marked2 で markdown](http://qiita.com/gooichi/items/2b185dbdf24166a15ca4)
-> これだけだとコマンドがみつからないので、[この](http://moonstruckdrops.github.io/blog/2013/03/24/markdown-mode/)通りパスを通す設定を入れる


[これ]((http://yasuyk.github.io/blog/2013/01/16/emacs-marked/))でもOK

```
(defun markdown-preview-file ()
  "run Marked on the current file and revert the buffer"
  (interactive)
  (shell-command
   (format "open -a /Applications/Marked.app %s"
       (shell-quote-argument (buffer-file-name))))
)
(global-set-key "\C-cm" 'markdown-preview-file)
```

-> Ctrl + c , mでmarked2起動

## ~/.bash_profile

- emacsのバージョンをCocoa emacsと揃える
  - `alias emacs="/Applications/Emacs.app/Contents/MacOS/Emacs -nw"`
- ターミナルのプロンプトを変更するために以下を追加 [参考](http://qiita.com/iwazer/items/5f57a80b8aac0f4e9839)
  - `export PS1='\W $ '`

## [githubの設定](http://qiita.com/shizuma/items/2b2f873a0034839e47ce)
