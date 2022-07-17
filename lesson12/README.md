## myserver.js
~~~javascript

const http = require('http');
const fs = require('fs');
const ejs = require('ejs');
const qs = require('querystring');
let template = fs.readFileSync(__dirname + '/forum.ejs','utf-8');
let posts = [];

const server = http.createServer((req,res)=>{
  let data = ejs.render(template,{
    title:'hello ejs',
    content:'<strong>big hello ejs.</strong>'
  });

  res.setHeader('Content-Type','text/html');
  res.statusCode = 200;
  res.end(data);

 
});

const hostname = '127.0.0.1';
const port =3000;

server.listen(port,hostname,()=>{
  console.log(`server running at http://${hostname}:${port}`);
});