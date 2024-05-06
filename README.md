# Module 10 - Asynchronous Programming - Broadcast Chat
> **Soros Febriano** || **2206083445**

## Experiment 2.1: Original code, and how it run
![alt text](images/server.png)
![alt text](images/client1.png)
![alt text](images/client2.png)
![alt text](images/client3.png)
When the clients are ran with `cargo run --bin client` and connected to an active server by running `cargo run --bin server`, the messages sent by a client will be broadcasted across all of the connected clients

## Experiment 2.2: Modifying port
![alt text](images/server_1.png)
![alt text](images/client1_1.png)
![alt text](images/client2_1.png)
![alt text](images/client3_1.png)
After modifying the port to 8080 at the `client.rs` at line 10:
`ClientBuilder::from_uri(Uri::from_static("ws://127.0.0.1:8080"))` and
`server.rs` at line 48 `let listener = TcpListener::bind("127.0.0.1:8080").await?;`, both components still run smoothly as expected.