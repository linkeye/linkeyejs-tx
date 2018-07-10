# linkeyejs-tx 

# install
`npm install linkeyejs-tx`

# usage

```javascript
const LinkeyeTx = require('linkeyejs-tx')
const privateKey = Buffer.from('e331b6d69882b4cb4ea581d88e0b604039a3de5967688d3dcffdd2270c0fd109', 'hex')

const txParams = {
  nonce: '0x00',
  gasPrice: '0x09184e72a000', 
  gasLimit: '0x2710',
  to: '0x0000000000000000000000000000000000000000', 
  value: '0x00', 
  subId:'0x00000000000000000000000000000000',
  data: '0x7f7465737432000000000000000000000000000000000000000000000000000000600057',
  chainId: 3
}

const tx = new LinkeyeTx(txParams)
tx.sign(privateKey)
const serializedTx = tx.serialize()
```

**Note:** this package expects ECMAScript 6 (ES6) as a minimum environment. From browsers lacking ES6 support, please use a shim (like [es6-shim](https://github.com/paulmillr/es6-shim)) before including any of the builds from this repo.
