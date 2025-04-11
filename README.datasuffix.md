# How to use transaction data suffix in Contract

## By using Contract constructor
```typescript
import { Contract } from "@ethersproject/contracts";
import ethers from "ethers";


const signer = ... // ethers Signer object to signing transaction data
const data = '0x....' // fixed suffix data to send on transaction
const contract = new Contract(contractAddress, abi, signer, data)
// every contract call from contract object will append `data` into transaction data

contract.setSuffixData(null); // you can set suffixData after changing contract
```
