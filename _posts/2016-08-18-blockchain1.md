---
layout: post
title: "Blockchain - Part1"
subtitle: "A beginner's guide"
date: 2016-08-18 23:45:13 -0400
background: '/img/posts/blockchain-part1.jpg'
---


There is a lot of buzz around blockchain these days. As I was reading in a blog, blockchain has now become a “solution” looking for a problem. The enthusiasm to implement blockchain is real. Considerable effort is being spend on creating proof of concept for various use cases. Before going into the application and use cases, lets understand the basics first.

## What is blockchain?

Blockchain is a distributed ledger (DL) where the transaction information is stored in blocks at multiple nodes and added to a chain to prior transaction (or blocks). In a centralized database structure, there is a central trusted party, which authenticates and stores information of all the transaction. Each of the nodes write to or read from the server. But in the DL, there is no central party. All the transactions are saved at all the nodes and authenticated by all the nodes. While centralized database is a server-client setup, the DL is a peer-to-peer network.

## How does a block get added to a blockchain?

Suppose a transaction takes place between 2 parties. Each node will individually create a block for this transaction. The node will take information of the 2 parties involved in the transaction, the transaction details, the “hash” to the previous block to create a new block. A new “hash” is created for this new block. A block gets added to the chain only if the “hash” created by all the nodes match. If the “hash” of one of the nodes doesn’t match, it gets corrected by way of “consensus”.

## Public Vs Permissioned blockchains

Public blockchains are those in which every node can read and write to the public ledger, that is a node doesn’t need any special permission to write to the ledger. The most widely implemented example of the public blockchain is Bitcoin. Since any node can write into a public ledger, the public blockchain has more complex logic (such as proof of work, longest chain rule, etc) to keep illegitimate blocks out of the ledger. In comparison, the permissioned or private ledger is one in which only a limited number of authorized nodes can write to the ledger. In the world of finance, one would expect to see more applications of permissioned than public blockchains due to the need for regulations compliance and risks involved.

 In the next post, I would talk more about the application of blockchain and some use cases.

 If you have any comments or queries, please leave a comment.