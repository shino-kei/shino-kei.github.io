---
created: 2024/10/27
modified: 2024/11/27
tags:
  - obsidian
  - quartz
---

## 必要な環境

- Obsidian
- Git
- nodejs
- npm

## フォルダ構成

- Obsidian Vault: ノートを書き溜める場所
	- publish: Github Pagesで公開するためのフォルダ
	- その他プライベートなフォルダ
- Quartz: ブログ管理用のリポジトリ

参考：[Obsidian + Quartz + Github Page を使ってサイト公開｜devlive](https://note.com/devlive/n/n3250edc2ee8f)

## 方針

- obsidianでページの編集を行う
- vault内に`publish`という名前のフォルダを作成し、公開したいノートはこの中に置く
- Quartz4でGitHub Pagesへのファイル変換を行う
- `publish`フォルダとQuartz4の作業フォルダは別々に管理する（submoduleにはしない）
	- `publish`フォルダへのシンボリックリンクをQuartz4の`contents`フォルダに作成

## 現状の懸念点

- 複数マシンで編集したくなったときどうする？
	- [livesync](https://github.com/vrtmrz/obsidian-livesync)でデバイス間のファイルは同期
	- 念のため別途Gitでバックアップを保存しておく

---

以下検討メモ

- htmlをそのまま書くのは大変なので、mdから変換したい
- octopressというものが有名っぽい？
	- [完全に無料なGithubブログを始める方法 - slow living in the sky](https://atmarksharp.v01.jp/posts/github-static-site-generators.html)
	- [Octopress をインストールして GitHub Pages で公開する - Qiita](https://qiita.com/key-amb/items/33c4823c78e50f8f2a04)
- obsidianに慣れてるから、Quartzが相性良いかも？
	- [Welcome to Quartz 4](https://quartz.jzhao.xyz/)
	- [Obsidian + Quartz + Github Page を使ってサイト公開｜devlive](https://note.com/devlive/n/n3250edc2ee8f)
	- [Quartz4で無料でObsidian Publishを代替する](https://masaki39.github.io/Quartz4%E3%81%A7%E7%84%A1%E6%96%99%E3%81%A7Obsidian-Publish%E3%82%92%E4%BB%A3%E6%9B%BF%E3%81%99%E3%82%8B)
		- publishというフォルダをobsidianリポジトリの中に作成し、Quartzの作業フォルダにシンボリックリンクを貼るという方法が提案されている
		- obsidianのvault内にサブモジュールを作る案もあるが、submoduleを上手く運用できた試しが無いので、シンボリックリンク方式にしておく
- やってみた。良い感じかも
	- [index](https://shino-kei.github.io)

![[img-技術ブログをgithubpagesに移行する.png]]
