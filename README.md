# EX01 Developing a Simple Webserver
## Date: 15-03-2024
## AIM:
To develop a simple webserver to serve html pages.
## DESIGN STEPS:
### Step 1: 
HTML content creation.
### Step 2:
Design of webserver workflow.
### Step 3:
Implementation using Python code.
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver.
## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content="""
<html>
<title>Top Software Industries</title>
<body>
<table border="2" cellspacing="10" cellpadding="6">
<caption>Top 5 Revenue Generating Software Companies</caption>
<tr>
<th>5.no</th>
<th>Company</th>
<th>Revenue</th>
</tr>
<tr>
<th>1</td>
<th>Microsoft</td>
<th>65 Billion</td>
</tr>
<tr>
<th>2</th>
<th>oracle</th>
<th>29.6 Billion</th>
</tr>
<tr>
<th>3</th>
<th>IBM</th>
<th>29.1 Billion</th>
</tr>
<tr>
kth>4</th>
<th>SAP</th>
<th>6.4 Billion</th>
</tr>
<tr>
<th>5</th>
<th>Symantec</th>
<th>5.6 Billion</th>
</tr>
</body>
</html>
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        printf("request received")
        self. send_response(200)
        self.send_header(" content-type',"'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address=(' ',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:
![313163640-71e47b3e-f08b-4606-b750-7fbd0b756131](https://github.com/Dhanusha17/simplewebserver/assets/151549957/9132a559-1cf8-4c26-bf83-cfbf9ffe593c)
![313163737-d2a0ac3c-0e80-4170-b4ca-5f46b146e9ab](https://github.com/Dhanusha17/simplewebserver/assets/151549957/c9901867-1392-48ce-9e8c-48faf6e9b07c)
## RESULT:
The program for implementing simple webserver is executed successfully.
