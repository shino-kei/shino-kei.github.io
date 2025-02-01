---
created: 2024/11/27
modified: 2024/11/27
tags:
  - obsidian
  - Commander
---

## 概要

Obsidianを使う際に、daily noteのタブを一番左においてピン留めするようにしているが、毎回操作するのが面倒なので簡略化したいと思った

結論としては、[Commander](https://github.com/phibr0/obsidian-Commander)と[pane-relief](https://github.com/pjeby/pane-relief)のプラグインで実現できたので、しばらく試してみる

![[img-デイリーノートを開いたら常に左端にピン留めされるようにしたい.png]]

## 手順

### ①プラグインのインストール

obsidianの設定メニューから、community pluginsを開いて、[Commander](https://github.com/phibr0/obsidian-Commander)と[pane-relief](https://github.com/pjeby/pane-relief)をインストールする

### ② マクロの登録

Commanderの設定から、マクロを登録する

Add Macroボタンを押して、下記の３コマンドを登録する（ここでは、`Open Pinned Daily Note`という名前をつけた）

![[2024-11-27_macro_open_pinned_daily_note.png]]

### ③リボンにコマンドを登録する

Commanderの設定メニューから先ほど作成したマクロを実行するリボンを追加する

![[2024-11-27_add_macro_commands_to_ribbon.png]]

すると、リボンメニューの中にマクロとして登録したコマンドが表示されているので、以降はこのボタンを押すだけでまとめて処理を実行できる

![[img-デイリーノートを開いたら常に左端にピン留めされるようにしたい.png]]
