## 6.2 Network Theory

Let's also clear up the blockchain network we're going to run with this setup and how the compensation works for providing the piece of backend infrastructure. Its important to know the basics of how we will participate.

### 6.2.1 Proof of Stake

PoS is a consensus mechanism used in many blockchain networks to validate and add new transactions to the blockchain. Unlike Proof of Work on Bitcoin, which requires miners to solve complex mathematical problems to add new blocks to the blockchain, PoS relies on the amount of cryptocurrency a person holds and is willing to stake as collateral.

In a PoS blockchain, validators are chosen to create a new block based on their stake in the network. The more cryptocurrency a person holds, the higher their chances of being chosen as a validator. Once chosen, validators validate transactions and add them to the blockchain. For their service, validators are rewarded with transaction fees and potentially new coins.

One of the main advantages of PoS over PoW is its energy efficiency. While PoW requires massive computational resources and energy consumption, PoS achieves consensus with minimal energy use. This makes PoS a more sustainable and environmentally friendly choice for blockchain networks.

Another advantage of PoS is the security it provides. Since validators have a significant investment in the network, they are incentivized to act honestly. If a validator tries to manipulate the system or validate fraudulent transactions, they risk losing their stake, making attacks on the network costly and therefore less likely.

### 6.2.2 Network Operations

The Ethereum Virtual Machine is a crucial part of the Ethereum ecosystem and each full node running the Ethereum software has its own instance of it. This is because every full node validates every transaction and smart contract execution independently. The EVM is isolated from the network, filesystem, and other processes of the node's computer system, which makes it a sandboxed environment for smart contract execution.

When a node receives a new block, it executes all transactions in that block in its own EVM to validate the correctness of the transaction results and the final state of the block. This is a fundamental part of the Ethereum network's decentralized nature: every node independently verifies the validity of every block and every transaction.

### 6.2.3 Computation Measures

Each operation in the EVM requires a certain amount of gas, which is paid for in the chains coin. The cost of gas is a crucial part of Ethereum's incentive structure, deterring spam on the network and incentivizing miners to confirm transactions.

Since the [London Update](https://eips.ethereum.org/EIPS/eip-1559) Ethereum has a predictable fee system with two parts: a base fee and a tip. The base fee is burned and adjusts up or down depending on network congestion. This means that when the network is busy, the base fee increases, and when the network is less busy, the base fee decreases. The tip, also called priority fee, is given to the miner as an incentive to include the transaction in the block.

Gas plays a crucial role in the execution of transactions. If a transaction or smart contract operation does not have enough gas, it runs out of gas and fails, but the gas used up to that point is not returned as the computation was finished up to this point.

### 6.2.4 Tokenomics

A large portion of the transaction fee is burned, i.e., permanently removed from circulation. This burning mechanism effectively reduces the supply of Ether over time, which can exert upward pressure on the price, assuming demand remains constant or increases, making EVM PoS blockchain coins a semi-deflationary asset.

Therefore, validators only receive the block rewards and tips as fees.

### 6.2.5 Earnings & Withdrawals

When it comes to withdrawels and returns, there are certain wallet addresses to maintain: the withdrawal and the recipient address. They could be the same address, but different actions are bind to them:

- **Staking Withdrawal Address**: Staking withdrawals refer to withdrawing earned rewards or the initial staked amount (32 LYX) by validators participating in Proof-of-Stake. These withdrawals become possible after the Shapella upgrade & EIP-4895 are up and running on the according network. These staking withdrawals are automatically pushed to the withdrawal address set during the key generation process and are registered on-chain during the deposit. This address cannot be changed once the stake is deposited.
- **Recipient Fee Address**: The recipient fee address, e.g., transaction or gas fee address, differs from the staking withdrawal. The recipient fee address is associated with the validator when they perform validation duties, such as proposing and attesting to blocks. The recipient fee address is set during the start of the validator client on the node and can be changed upon restart. To set or modify, you need your node's wallet password after importing the validator keys. The fees are paid by users who initiate transactions and smart contract executions on the EVM network. Validators collect the fees as an incentive for their work in maintaining the blockchain.

In conclusion, staking withdrawals refer to withdrawing rewards and staked amounts connected to the consensus mechanism. On the other end, the recipient fee address is where validators receive transaction fees for their validation work itself.

> Typically everything is included in the APY for staking rewards. But as expected, there are fluctuations for various factors such as network usage, the number of validators, and consensus changes.