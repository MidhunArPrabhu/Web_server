# Developing a Simple Webserver

# AIM:

NAME: MIDHUN AZHAHU RAJA P
REFERENCE NO : 22008311
# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content ="""
<html>
<head>
</head>
<body>
<h1>MIDZ SIMPLE WEBSERVER</h1>
<h2>NAME:MIDHUN AZHAHU RAJA P</h2>
<h3>REFERENCE NO: 22008311</h3>
<h4>LIST OF FRAMEWORKS : </h4>
<u1>
<li>DJANGO<img src="https://studygyaan.com/wp-content/uploads/2021/12/CicamXxN_400x400-1.jpg" style="width: 150px;height: 150px"></li>
<li>FLASK<img src="https://miro.medium.com/max/800/1*Q5EUk28Xc3iCDoMSkrd1_w.png" style="width: 150px;height: 150Px"></li>
<li>RUBY ON RAILS<img src="https://rubyonrails.org/assets/images/opengraph.png" style="width: 150px;height: 150px"></li>


</body>
</html>"""


class HelloHandler(BaseHTTPRequestHandler):  
     def do_GET(self):
          self.send_response(200)
          self.send_header("content-type","text/html;charset=utf-8")
          self.end_headers()
          self.wfile.write(content.encode())

server_address = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve_forever()
```
# OUTPUT:

![MIDZ_DI](midz_simpweb.png)

# RESULT:
The program is executed succesfully
