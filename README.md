# scribd

Scribd REST API binding for Node.JS.

### Installing

GIT

    $ git clone https://github.com/firejune/scribd.git

NPM

    $ npm install scribd

### Usage

    var Scribd = require('scribd');

    var Scribd_api_key = "ENTER-YOUR-API-KEY-HERE"
      , Scribd_secret = "ENTER-YOUR-API-SECRET-HERE"; 

    var scribd = new Scribd(Scribd_api_key, Scribd_secret);
    
    
    // callback, file, docType, access, revId
    scribd.upload(function(err, res) {
      console.log('scribd.upload', err, res);
    }, './aaa.docx');
    
    // callback, url, docType, access, revId
    scribd.uploadFromUrl(function(err, res) {
      console.log('scribd.uploadFromUrl', err, res);
    }, 'url');
    
    // callback, docId
    scribd.remove(function(err, res) {
      console.log('scribd.remove', err, res);
    }, 'docId');
    
    
    // callback, query, numResults, numStart, scope
    scribd.search(function(err, res) {
      console.log('\nscribd.search', err, res);
    }, 'Node.JS', 1);
    
    // callback
    scribd.getList(function(err, res) {
      console.log('\nscribd.getList', err, res);
    });
    
    
    // callback, docId
    scribd.getConversionStatus(function(err, res) {
      console.log('\nscribd.getConversionStatus', err, res);
    }, docId);
    
    // callback, docId
    scribd.getSettings(function(err, res) {
      console.log('\nscribd.getSettings', err, res);
    }, docId);
    
    // callback, docId, title, description, access, license, showAds, tags
    scribd.changeSettings(function(err, res) {
      console.log('\nscribd.changeSettings', err, res);
    }, 'docId', 'title');
    
    
    // callback, username, password
    scribd.login(function(err, res) {
      console.log('\nscribd.login', err, res);
    }, 'username', 'password');
    
    // callback, username, password, email, name
    scribd.signup(function(err, res) {
      console.log('scribd.signup', err, res);
    }, 'username', 'password', 'email', 'name');

Have fun!

### License

MIT <3
