# Aptos Wallet Client Api

### Initialize WalletClient

```
const NODE_URL = "https://fullnode.devnet.aptoslabs.com/v1";
const FAUCET_URL = "https://faucet.devnet.aptoslabs.com";

const walletClient = new WalletClient(NODE_URL, FAUCET_URL);
```

### Cteate New Account

```
  let { account, seed } = await walletClient.createNewAccount();
```

### Check Balance

```
  let balance = await walletClient.balance(addr1);
```

### Send Token

```
 let txnHash = await walletClient.transfer(fromAccount, toAddress, sendAmount);
```

### Import Account

```
 let account = await walletClient.getAccountFromMnemonic(seed);
```

### Account Transactions

```
 let txns = await walletClient.getAllTransactions(address, coin);
```
