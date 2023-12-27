
# 第三回課題
## 1.サンプルアプリケーションのデプロイ  
![デプロイ](img/lecture03-1.png)
## 2.APサーバー
name:Puma version:5.6.5  
```bin/cloud9_dev```
## 3.DBサーバー  
name:MySQL version:8.0.35  
```mysql -u root -p```  
停止  
```sudo service mysqld stop```  
再開  
```sudo service mysqld start```  
## 4.Rails構成管理ツール
**bundler**  
bundlerとはgemのバージョンやgemの依存関係を管理するツール。あるgemを使うために別のあるgemを使う必要がるといった関係を依存関係という。bundlerは依存関係が解決されたgemを一括でインストールしてくれ、複数人（台）のPCで作業する際も同じバージョンのgemを一括でインストールすることができる。
## 5.感想
各コードの意味や、yarnなどの言葉の意味を調べながら進めたため約10日間という長時間かかってしまったが、ある程度の理解を持って進めることができた。しかし、正直なところ、全く同じサンプルアプリケーションを自分一人でデプロイできるかというと全くの自信はなく、場数を踏んで、コードや言葉、調べ方などの理解を深めて行く必要があると感じた。

## MySQL
ログイン：mysql -u root -p
Which mysql →コマンドがどこにあるかを表示  
My cnf→MySQLで読み込まれる設定ファイルのこと。
My cnfの場所はLinuxの場合は/etc/my cnfにあることが多い  
Which my conf→設定ファイルがどこにあるかを表示
/etc -------プログラムの起動、終了や再起動などのコントロール機能やプログラム本体などが保存されている
Mysql停止　sudo service mysqld stop
Mysql再起動　sudo service mysqld start

## Ruby
rvm　→　ruby version manager:複数のRuby実行環境の管理を簡単にするスクリプトツール  
gemとは
ライブラリなどのパッケージ
指定したバージョンをインストール：rvm install "version"

## yml  
Ymlとは設定ファイルの形式に使われることの多い言語、ソフトウェアやアプリケーションの設定情報を記述する際によく使われる。
cp config/database.yml.sample config/database.ymlとは
Railsにおけるデーターベースとの接続におけるコード化したもの。ちなみに、sampleファイルは実際に使わず、それをコピーしたファイルを別に用意し、そちらを使用する。　　

## socket  
ネットワークとの接続口のこと。
Database.ymlのsocketとはソケットファイルのパスを示す

## bin setup
Rails配下にあるbin/setupファイルの中身を実行するコマンド。
Bin/setupはRailsが用意している開発環境のセットアップようのスクリプトファイル

## catコマンド
ファイルの中身を確認したいときに使用するLinuxコマンド

## yarn
Javascriptをサーバーサイドで動かすための実行エンジンであるNode.js上で動作するパッケージマネージャー。
パッケージマネージャーとは、各ソフトウェアのインストールや更新などの操作、また他のソフトウェアとの依存関係を管理するためのツール。
Yarnのインストール:npm install --global yarn
Yarnのバージョン変更： yarn set version バージョン
※Cloud9を再起動するとyarnがなくなっている

## 起きていること		
Bin/setup →　yarnがインストールされていないとエラー　→　インストールしたところ解決
Bin/setup →　mysqlがエラー　→　パスワードの有効期限切れと判明 →　パスワード変更　→　detabase.ymlのパスワードも変更する　→　エラー解決できず

![犬](20231227-1334_ec676204ee36533204e01db450e0265e.png)
