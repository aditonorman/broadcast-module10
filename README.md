### Tutorial 2.1: Broadcast Chat — Results and Explanation

In this tutorial, I implemented a WebSocket-based broadcast chat system in Rust using `tokio` and `tokio-websockets`. I wrote two binaries: one for the server and one for the client. The server listens on TCP port 2000 and uses a broadcast channel to forward incoming messages to all connected clients.

To test the setup, I ran the server and then launched three separate client instances in different terminals. Each client connected successfully and was able to send and receive messages. When I typed a message in one client, it was broadcast and displayed in all clients, including the sender.

This confirmed that the server correctly receives and rebroadcasts messages using asynchronous tasks. The WebSocket streams handled input and output concurrently, and the broadcast channel ensured all clients received every message.

Here’s what I saw from one of the clients:
![img.png](img.png)![img_1.png](img_1.png)![img_2.png](img_2.png)![img_3.png](img_3.png)