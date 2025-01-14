##Ex:01 Developing a Simple Webserver
## DATE:07-10-2023
## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation
### Step 2:
Design of webserver workflow
### Step 3:
Implementation using Python code
### Step 4:
Serving the HTML pages.
### Step 5:
Testing the webserver

## PROGRAM:
```
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Top 5 Revenue generating software Companies<h1>
<UL TYPE=“circle”>
<LI> zoho </LI>		
<LI> apple </LI>
<LI> infosys </LI>
<LI> accenture </LI>
<LI> microsoft </LI>
</UL>
</body>
</html>

"""

class myhandler(BaseHTTPRequestHandler):

    def do_GET(self):

        print("request received")

        self.send_response(200)

        self.send_header('content-type', 'text/html; charset=utf-8')

        self.end_headers()

        self.wfile.write(content.encode())

server_address = ('',8000)

httpd = HTTPServer(server_address,myhandler)

print("my webserver is running...")

httpd.serve_forever()

```

## OUTPUT:

![image](https://github.com/jaisurya143/simplewebserver/assets/121999338/7c1d9734-fbd7-40e0-ad46-a3823b87b927)

![image](https://github.com/jaisurya143/simplewebserver/assets/121999338/d8aea9cc-7974-46af-8fec-476a666fc90b)



## RESULT:
The program for implementing simple webserver is executed successfully.
