# react
learn-react

# todo
- React + Redux の開発環境構築

# references
- 開発環境：https://qiita.com/ma2saka/items/ad8d1f129f52fba5e5ae
- 開発環境：https://qiita.com/wwalpha/items/55f7d52950edff1bdb17
- 開発環境：https://qiita.com/yutasuzuki/items/83d2bfdfa58341a1e99e
- チュートリアル：https://laboradian.com/tried-react-redux-tutorial/
- TODOアプリ：https://webbibouroku.com/Blog/Article/react-redux-todo

# react | 接続情報
- app : 192.168.33.10:80

# memo - 環境構築 (後ほどevernoteに移行) https://www.evernote.com/l/ANcL5bjoFchBi6UgYkCwgzrwlvO3B9wJGWQ
- nodeのインストール
https://サーバー構築と設定.com/?p=3272

$ sudo yum install https://rpm.nodesource.com/pub_11.x/el/7/x86_64/nodesource-release-el7-1.noarch.rpm

$ sudo yum info nodejs

$ sudo yum install nodejs

$ node --version
v11.7.0

$ npm --version
6.5.0

$ echo 'console.log("Hello, World!");' > hello.js

$ node hello.js
Hello, World!

$ vim hello.js
===================
var http = require('http');

http.createServer(
  function (req, res) {
    res.writeHead(200, {"Content-Type": "text/plain"});
    res.write('Node.js server is running!');
    res.end();
  }
).listen(8080);
===================

$ node hello.js
192.168.33.10:8080

# ReactでTODOアプリを作ってみる
- url:https://webbibouroku.com/Blog/Article/react-redux-todo
- install
$ sudo npm install -g create-react-app

$ create-react-app react-redux-todo

$ cd react-redux-todo
$ npm install --save redux react-redux redux-logger

[ReactにReduxを組み込む]が終わったら一旦下記コマンドを実行して、動作を画面を確認
$ cd /vagrant_data/react-redux-todo/
(vagrantの中)
$ npm start
http://192.168.33.10:3000

# 自動起動
- https://qiita.com/takenobi/items/797be00dd0b592f484ef
- https://www.sejuku.net/blog/81363
$ cd react-redux-todo

$ vim server.js
  const express = require('express');
  const app = express();
  const path = require('path');
  app.use(express.static(path.join(__dirname, 'build')));
  const port = process.env.PORT || 3000;
  const server = app.listen(port, function () {
      console.log('server start');
  });

$ sudo npm install --save express

# 手動起動
$ node server.js

$ sudo npm install -g forever

$ forever start server.js

$ forever stop server.js

# TODOアプリ完了後、webpackを設定
- https://wp-kyoto.net/learn-webpack-again/
