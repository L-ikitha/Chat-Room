# 📡 Chat Room

A basic **multi-client chat room** implemented in C++ using **sockets** and **multithreading**. This project allows multiple clients to connect to a server and exchange messages in real-time.

---

## 🧠 Overview

* 🖥️ **Server** handles connection requests
* 💬 **Clients** connect and chat with each other
* 🚀 Uses **TCP sockets**
* 🧵 Supports multiple clients using **threads**

---

## 📌 Features

✅ Accepts multiple client connections
✅ Broadcasts messages to all connected clients
✅ Server continuously listens for new clients
✅ Clients can send and receive messages simultaneously

---

## 🗂️ Folder Structure

```
Simple-Chat-Room/
├── Server/
│   ├── Server.cpp
│   └── main.cpp
├── Client/
│   ├── Client.cpp
│   └── main.cpp
└── README.md
```

---

## ▶️ How To Build & Run

### ⚙️ Requirements

You’ll need:

✔ C++ compiler (g++, clang++, MSVC)
✔ C++17 standard support
✔ Windows / Linux / macOS terminal

---

### 🖥️ On **Windows (MinGW-w64 or MSYS2)**

Install g++ (via MSYS2 or MinGW). Then compile:

```bash
g++ -std=c++17 Server/Server.cpp Server/main.cpp -lws2_32 -o chat_server
g++ -std=c++17 Client/Client.cpp Client/main.cpp -lws2_32 -o chat_client
```

Run server:

```bash
.\chat_server.exe
```

Run client (in new terminal):

```bash
.\chat_client.exe
```

---

### 🐧 On **Linux / macOS**

```bash
g++ -std=c++17 Server/Server.cpp Server/main.cpp -pthread -o chat_server
g++ -std=c++17 Client/Client.cpp Client/main.cpp -pthread -o chat_client
```

Run:

```bash
./chat_server
./chat_client
```

---

## 💡 How It Works

1. **Server** starts and waits for connections
2. **Client** connects with server address & port
3. Server assigns each client to a **thread**
4. Clients send messages → server broadcasts to all
5. Chat continues until closed

---

