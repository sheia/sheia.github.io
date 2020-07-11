---
layout: post
title: "Blockchain - Part2"
subtitle: "When to use blockchain?"
date: 2016-08-26 23:45:13 -0400
background: '/img/posts/blockchain-part2.jpg'
---


The first step in solving a business problem is defining requirements. Then one defines a design that best solves the business problem. With the hype around blockchain and over-eagerness to get on the blockchain bandwagon, corporates are taking the reverse approach – they are searching for use cases to implement blockchain in their organisations. 

But was blockchain really required in the use case? If there are few or no real benefit in using blockchain, it would be wiser to use an already existing and well established databases which has years of research and development behind them rather than use blockchain, which is still in its very nascent stage.

## So when should one choose blockchain?

- When there is a need for a shared database – where multiple users read and write to a database but there is only one unique value of the database at any given point in time.

- When the users do not want to have a central intermediary. The reason for a need for disintermediation could be to reduce cost as there are additional protocols and checks to put in place to ensure the integrity of the central party to make sure the intermediary is not tampering with the data, which if done could be difficult to detect and prove. Or the reason could be to improve security as a distributed ledger with multiple copies of the database is harder to tamper with than the central ledger.

- When the confidentiality of the data is not critical. In a centralised database, there can be a restriction on who accesses which data. But with blockchain, all the parties can see all the transactions even though the data would be encrypted. But this condition is evolving now as solutions such as R3 Corda is rethinking the need to share and validate all the transactions with everyone, rather restricting them to parties involved in the transaction.

Having described the conditions  let’s now look at one example of a blockchain implementation.

## An use case - Financial agreement between 2 banks

Suppose there is a transaction between 2 banks, BankA and BankB. BankA sends the details of the transaction to BankB and saves a local copy. BankB receives and processes the message and saves a local copy too. Though the message would be in a industry standardised format, there is no guarantee that BankB has interpreted the message correctly. Hence, the need for costly reconciliation between the banks, followed by rework arising from mismatch in data. 

Blockchain can help here by providing a shared database which the banks can use as a shared ledger. Each bank will know that this is the same information that is read by the other bank also. Due to the immutability of blockchain, the banks and the regulators can be confident about the validity of the data and its history and the same can be used for regulatory reporting as well.

You may refer to my earlier article in this link for the basics of blockchain.

Please leave a comment in case of any thoughts or queries.