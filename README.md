# work_env

## 概要
北大Bioinfo研究会での解析用レポジトリです。

## 初期設定

1. dockerをインストールする。
2. `docker pull kokeh/dev_slim:0.1.2`を実行する。
3. gitをインストールする。
4. `https://github.com/kohta-hatanaka/work_env.git`を好きな場所(ホームディレクトリとか)で実行する。  
`git clone git@github.com:kohta-hatanaka/work_env.git`でも可。

## 使い方
下記のコマンドを実行して、docker contaierを起動する。  
`docker run -it -v (work_env/wdのパス):/home/user kokeh/dev_slim:0.1.2`

基本的にprojフォルダ内でプロジェクトを作って動かす。  
各プロジェクトフォルダ内で  
・Pythonの初期化：`uv init`  
・Rの初期化：Rを2回実行する。(1回目はSave workspace image? [y/n/c]:→n、2回目はそのまま使える。)  
をすると使えるようになるので初期化して使用する事。  

jupyterの起動などは今後追加していく予定。  

注：メモリの消費が激しくなるため、vscodeを利用する際はホスト側(WSLを使っているときはwindows側)からのみ接続する事を推奨。
将来的にはdocker内でjupyter起動→ホスト側からサーバーに接続する形で実行する事を目標。