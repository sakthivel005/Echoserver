# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
## CLIENT:
```
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```


## SERVER:
```import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")
```

## OUTPUT:
## Client output:

![Screenshot 2023-08-31 084722](https://github.com/sakthivel005/Echoserver/assets/120550359/e5ec546c-df7d-4ae5-9d99-e9a64afc12ef)


## Server output:

![Screenshot 2023-08-31 084749](https://github.com/sakthivel005/Echoserver/assets/120550359/6e1807df-664a-4cfb-8d20-f83982a1916d)



## RESULT:
The program is executed successfully
