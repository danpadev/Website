# Blocks (mermaid)

The network is initialized from a single node and a **genesis block**. This is the very first block in the blockchain which defines the initial structure of the network.

```mermaid
graph TD
    node(Node) --> genesis-block(Genesis<br>Block)
    style genesis-block fill:#ddd,stroke:#000,stroke-width:4px
```


The genesis block consists of the minimum amount of information required to initialize a new network including:

* All account information from alpha
* The node registration of the source node
* The initial schedule consisting a single node (the source node)

| Genesis Block      |
|--------------------|
| All Alpha Accounts <table><tr><td>✓ -----</td></tr><tr><td>✓ -----</td></tr><tr><td>✓ -----</td></tr></table> |
| Node Registration <== Node |
| Schedule <table><tr><td>1. Node A</td></tr><tr><td>2. Node B</td></tr><tr><td>...</td></tr></table>          |

Blocks are data structures that represent a description of change to the network. These originate from signed requests and may include:

* a transfer of coins between accounts
* the registration of a username
* a new node being added to the network
* etc...

```mermaid
graph TD
    genesis-block("Genesis Block<br>repesents the initial<br>structure of the network") --> block0(block 0)
    block0(block 0) --> block1("block 1<br>(change to account balances)")
    block1("block 1<br>(change to account balances)") --> block2(block 2)
    block2(block 2) --> block3(block 3)
    block3(block 3) --> block4(block 4)
    block4(block 4) --> block5("block 5<br>(change to PV schedule)")
    block5("block 5<br>(change to PV schedule)") --> block6(block 6) 
    
    style genesis-block fill:#ddd,stroke:#000,stroke-width:4px
    style block0 fill:#0dd,stroke:#000
    style block1 fill:#07e,stroke:#000
    style block3 fill:#07e,stroke:#000
    style block4 fill:#07e,stroke:#000
    style block5 fill:#0dd,stroke:#000
    style block6 fill:#07e,stroke:#000
```


> ⓘ Note
> For details on all the different block types, see the [Block Types](https://www.thenewboston.com/guide/block-types) section of the documentation.
