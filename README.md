# BlockchainPrinciplesAndPractices
The fundamental data structures and algorithms used to build a typical Blockchain and build up a working example. First, learn how to store single transactions in a block. Second, discover how to store multiple transactions in a block using Merkle trees. Next, learn how to make the Blockchain tamper-proof using mining and proof-of-work. Finally, learn how nodes on a Blockchain maintain consensus. By the end, have the knowledge and tools necessary to build own Blockchain.

# Notes
## Storing Transactions in Blocks
Block Header (IBlock interface)

```
int BlockNumber { get; }
DateTime CreatedDate { get; set; }
string BlockHash { get; }
string PreviousBlockHash { get; set; }
IBlock NextBlock { get; set; }
```

### Run project BlockWithSingleTransaction
Install C# extensions

Open project with Visual Studio Code.

```
code .
```

Use Debug .NET Core. Set up breakpoints and start debugging. Check result on debug console.

### BlockWithMultipleTransaction Project
Use Merkle Tree to hash all trasactions.

Add ```List<ITransaction> Transaction { get; }``` to ```IBlock``` interface.

ITransaction interface
```
string ClaimNumber { get; set; }
decimal SettlementAmount { get; set; }
DateTime SettlementDate { get; set; }
string CarRegistration { get; set; }
int Mileage { get; set; }
ClaimType ClaimType { get; set; }
```

#### Merkle Tree
Check Merkle folder.

