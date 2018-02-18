ect-bootstrap-express
=====================

[Express](http://expressjs.com/ja/)のテンプレートエンジンに
[ECT](https://ectjs.com/)を使用して、
[Bootstrap v4.0](http://getbootstrap.com/)の
[Starter template](http://getbootstrap.com/docs/4.0/examples/starter-template/)の状態からサクッと始めるための雛形です。

## 使っているパッケージ

```
npm install --save ect
npm install --save bootstrap
npm install --save jquery
npm install --save popper.js
```

## app.js の修正箇所

```
var ECT = require('ect');
var ectRenderer = ECT({ watch: true, root: __dirname + '/views', ext : '.ect' });

// app.set('view engine', 'jade');
app.set('view engine', 'ect');
app.engine('ect', ectRenderer.render);
```

## ECT とは

[Pug](https://pugjs.org/)(Jade) と [EJS](http://ejs.co/) の良いトコ取りをしつつ爆速と評判のテンプレートエンジンです。  
EJSみたいに `<%= @title %>` てな感じで変数を埋め込んだりでき、  
Pugみたいに`extend` やら `block` やら `include` が使えます。
