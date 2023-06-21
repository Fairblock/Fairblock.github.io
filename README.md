



# Fairblock.github.io

<img width="512" alt="Screen Shot 2023-06-20 at 1 57 08 AM" src="https://github.com/Fairblock/FairBlock.github.io/assets/34263018/f92e8ad9-0e0b-4a19-8f08-0a2dd210e163">

While decentralized applications are rapidly gaining popularity, lack of “pre-execution privacy” has limited many on-chain applications including private governance/voting, sealed-bid auctions, or caused major obstacles to DeFi applications from a user-centric point-of-view specifically with front-running strategies.

 

Alongside the huge financial loss which goes out of the pockets of retail users and protocols, bad MEV (not good MEV e.g. arbitrage) has many other negative effects such as consensus instability (especially sabotaging a smaller Cosmos chain for an MEV opportunity in another chain), UX complexity (failure of transactions, slippage, and lost opportunities), waste of blockspace, and network congestion.

 

Based on extensive academic research, Fairblock is building infrastructure that can enable “pre-execution privacy” for applications such as front-running protection, private voting/governance, censorship-resistant rollup sequencers, and randomness generation oracles. Fairblock leverages distributed identity-based encryption which is a novel, secure, and efficient pairing-based scheme that can be exploited cleverly to enable pre-execution privacy. The highly simplified flow our approach will have is as follows:

(a) Users encrypt transactions using a master public key (remains the same) and ID of the block in which the transaction should be executed (happens seamlessly in the user browser) and send them to the destination chain directly (not Fairblock).

(b) Consensus validators or a sequencer of the destination chain finalize the ordering and inclusion of encrypted transactions

(c) Fairblock validators share their shares of the block key (block key is a single key to decrypt all transactions encrypted to a combination of the validators’ shared public key and an ID corresponding to block height or other conditions).

(d) A single private key (block key) will be automatically generated using an honest majority of private keys on FairyRing (Fairblock decentralized network of private key generators)

d) The generated block key will be used to decrypt all of the previously encrypted transactions and execution follows the inclusion and ordering in step b (before execution of plaintext transactions in the next block).

 

It is easy to see that this mechanism solves many forms of exploits/front-running attacks (bad MEV) and protects the contents of the transaction before execution to enable other applications such as sealed-bid auctions and private governance i.e. the validators must finalize a block of encrypted transactions and fix their order, no party can see the information in them, and hence it is much harder for them to influence the outcome. 

 

Fairblock can be used for front-running protection, private limit orders, private voting/governance, sealed-bid auctions, randomness generation and censorship-resistant sequencers in the Cosmos and soon in the Ethereum ecosystem, modular ecosystem (Celestia), Layer 2s (Optimism, Scroll, Eclipse), and cross-chain infrastructures and applications (Axelar, Squid) to protect the contents of the transactions before execution. Our goal/value is empowering users and protocols with the optional freedom of encrypting their transactions in order to protect them against various forms of malicious strategies and enable decentralized applications which are not previously possible.
