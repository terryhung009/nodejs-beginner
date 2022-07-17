## myserver.js
~~~javascript

const http = require('http');
const fs = require('fs');
const ejs = require('ejs');
const qs = require('querystring');
let template = fs.readFileSync(__dirname + '/forum.ejs','utf-8');
let posts = [];

const server = http.createServer((req,res)=>{
  if(req.method ==='POST' ){
    //表單提交
    req.data= "";
    req.on("readable",function(){
      //表單數據收集
    })
  }

 
});

const hostname = '127.0.0.1';
const port =3000;

server.listen(port,hostname,()=>{
  console.log(`server running at http://${hostname}:${port}`);
});