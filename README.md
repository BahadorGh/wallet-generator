# wallet-generator
Easily generate wallet with ethers package, bsc ( and other similar networks)

## Instruction:
### Prepare the project:
- `mkdir walletGenerator && cd walletGenerator`
- `npm init -y`
- `npm install ethers`
- create new js file and insert codes as below:

```
var ethers = require("ethers");
var crypto = require("crypto");
````

```
var id = crypto.randomBytes(32).toString('hex'); // generating 32bytes random string 
var privateKey = '0x' + id; // 0x is used to make private key in hexadecimal

console.log("PrivateKey(don't share this with anyone!): ", privateKey);

var wallet = new ethers.Wallet(privateKey);
console.log("Wallet address:", wallet.address);
```

After generating wallet you will have public and private key of your newly generated wallet.
To check your wallet, you can test assets in it from explorer:
- charge your wallet from a faucet like: https://testnet.binance.org/faucet-smart (for binance smart chain testnet faucet)
- then check your balance from explorer as here : https://testnet.bscscan.com/address/{YourWalletAddress}
