



# Fairblock.github.io

<img width="512" alt="Screen Shot 2023-06-20 at 1 57 08 AM" src="https://github.com/Fairblock/FairBlock.github.io/assets/34263018/f92e8ad9-0e0b-4a19-8f08-0a2dd210e163">

Fairblock is building a chain-agnostic framework that makes it easy for developers to implement privacy-preserving transactions at critical paths. We think of cryptographic schemes as different tools in a toolbox, and there is no one-size-fits-all solution when building privacy into applications. Leveraging advanced cryptographic schemes including identity-based encryption (IBE), witness encryption (WE), and fully homomorphic encryption (FHE), Fairblock is building blockchain infrastructure for programmable privacy and conditional decryption. These technologies help protect the content of transactions from bots, competitors, and other adversaries. 

This can be useful for a wide range of privacy-preserving use cases including encrypted on-chain intents (limit orders, stop-loss orders, programmable trading), bad-MEV prevention, private governance, censorship-resistant shared sequencing, on-chain gaming, on-chain legal contracts, randomness generation oracles, and any scenario where asymmetric information limits the use of a decentralized application.

Fairblock consists of:

- The Fairblock SDK -  A framework that developers can use as part of the building blocks of their applications and networks to take advantage of the privacy-preserving services offered by the Fairblock Network.
- FairyRing - A Cosmos SDK appchain mainly responsible for decentralized generation of private keys for decryption of transactions generated across the apps and networks that have integrated Fairblock, triggered upon specific conditions.

The highly simplified flow of our approach is as follows:

a. From the frontend of an app that has integrated Fairblock, a user encrypts a transaction(s) using a master public key and declares the transaction’s “condition(s) for decryption.” Example of “conditions” are the execution of a transaction at a specific time in the future, when certain market conditions are reached, or at the conclusion of a voting period. The encrypted transaction(s) is submitted on-chain on the network where the application resides.
 
b. The validators or sequencers of the underlying network include the encrypted transaction(s) in a block.

c. Once the condition(s) for decryption are met, validators of the FairyRing submit private key shares. The key shares are aggregated to form a private key matching the master public key associated with the encrypted transaction(s) and the condition of decryption.

d. The aggregated private key is used to decrypt the encrypted transaction(s), which are thereafter executed by the validators of the network upon which the app resides.

Using this approach, Fairblock provides developers with the freedom to choose when, where, and how to implement encrypted transactions into decentralized applications. This can be useful to protect users from various forms of malicious strategies from adversaries, promoting fairness across the crypto ecosystem.
