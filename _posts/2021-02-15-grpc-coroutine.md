---
layout: post
title: "GRPC and C++ coroutine"
---

# Why
Recently, I am learning GRPC and C++ coroutine. I was thinking why not combining them togeter, and writing some GRPC toy programs using C++ coroutine. Hence the series of posts you will see in the nearly future. This is the first post of them.

# Hello World!
GRPC is google's RPC (remote procedure call) framework utilizing google's protobuf for serializing messages between two remote procedure stubs. Our first toy program is the "Hello World!" program distributed with every GRPC package.

The process is simple. The client sends a request message containing a name to the sever by calling a remote procedure on the server. Upon receiving the request, the server runs the procedure using the message as the argument and return a reply containing "Hello [name]" to the client. If the name containing in the message is "World!", then we have the famous "Hello World!".

## GRPC Code without Coroutine

