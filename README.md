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

memo:[Storeの作成]から作業再開
