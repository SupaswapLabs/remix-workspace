REMIX DEFAULT WORKSPACE

Remix default workspace is present when:
i. Remix loads for the very first time 
ii. A new workspace is created with 'Default' template
iii. There are no files existing in the File Explorer

This workspace contains 3 directories:

1. 'contracts': Holds three contracts with increasing levels of complexity.
2. 'scripts': Contains four typescript files to deploy a contract. It is explained below.
3. 'tests': Contains one Solidity test file for 'Ballot' contract & one JS test file for 'Storage' contract.

SCRIPTS

The 'scripts' folder has four typescript files which help to deploy the 'Storage' contract using 'web3.js' and 'ethers.js' libraries.

For the deployment of any other contract, just update the contract's name from 'Storage' to the desired contract and provide constructor arguments accordingly 
in the file `deploy_with_ethers.ts` or  `deploy_with_web3.ts`

In the 'tests' folder there is a script containing Mocha-Chai unit tests for 'Storage' contract.

To run a script, right click on file name in the file explorer and click 'Run'. Remember, Solidity file must already be compiled.
Output from script will appear in remix terminal.

Please note, require/import is supported in a limited manner for Remix supported modules.
For now, modules supported by Remix are ethers, web3, swarmgw, chai, multihashes, remix and hardhat only for hardhat.ethers object/plugin.
For unsupported modules, an error like this will be thrown: '<module_name> module require is not supported by Remix IDE' will be shown.

**Transaction Details:**
- Pair Contract: https://testnetscan.scschain.com/tx/0x544679fb2672023cfc8e4d43bc8cdd9431895ee46ff558fc4411370a10156564
- ERC-20 Contract: https://testnetscan.scschain.com/tx/0x10324969d7d1c1b48215e03f09c714e825210761e6c742aeb2f53bab35a3b11b
- Factory Contract: https://testnetscan.scschain.com/tx/0xa4226b18f40c392d0b5a5c071c4af33474c4dff16e84760ca119dc5402583cd2
- Create Pair: https://testnetscan.scschain.com/tx/0x4b51d85e5b453d819a49581738f8000b3c9960bbfe7276f87bbee537fd1db520 => 0x49EaE6000a0a39ED98CE92fa81f2efF2f70f95F8
- Contract Creator Address: 0xB26444db4062440543919361d7A19db1495F5785
- SetFeeTo: 0xB26444db4062440543919361d7A19db1495F5785
- tokenA: 0xac5da1e4cda892a2e4506072fe14c8e42f2760bb
- tokenB: 0x2bda8f0ae0e7c584c77dd5c74c486fe717692c30
- Pair Transaction: https://testnetscan.scschain.com/tx/0xfd0cc54c9b99de5fae9ecdab2a7ab0658884ed8880402908332b0f3713bd951c
  
**resources:**
- https://superexchain.github.io/smart-contract/deployment/remix.html
- https://testnetscan.scschain.com/api-docs

**Logs:**


[block:3178713 txIndex:0]from: 0xB26...F5785to: UniswapV2Factory.(constructor)value: 0 weidata: 0x608...f5785logs: 0hash: 0x25f...0fa6c
status	true Transaction mined and execution succeed
transaction hash	0x544679fb2672023cfc8e4d43bc8cdd9431895ee46ff558fc4411370a10156564
block hash	0x25f0cbac39e7e12b0c890f8040de148d72732f441f21a19203c57422c300fa6c
block number	3178713
contract address	0xa723C7bC9D8b7d55a9ea6db66c47b5bf27c63A39
from	0xB26444db4062440543919361d7A19db1495F5785
to	UniswapV2Factory.(constructor)
gas	4139002 gas
transaction cost	4139002 gas 
input	0x608...f5785
decoded input	{
	"address _feeToSetter": "0x0000000000000000000000000000000000000000"
}
decoded output	 - 
logs	[]
val	0 wei
call to UniswapV2Factory.allPairs
call to UniswapV2Factory.allPairs errored: Returned error: {"jsonrpc":"2.0","error":"invalid opcode: INVALID","id":7370203893933050}
transact to UniswapV2Factory.createPair pending ... 

[block:3178790 txIndex:0]from: 0xB26...F5785to: UniswapV2Factory.createPair(address,address) 0xa72...63A39value: 0 weidata: 0xc9c...92c30logs: 1hash: 0x406...fe894
status	true Transaction mined and execution succeed
transaction hash	0x4b51d85e5b453d819a49581738f8000b3c9960bbfe7276f87bbee537fd1db520
block hash	0x4062654fbd13210af09a05c6267e0d92b7c9e2455f2b61ab8a559da6ceffe894
block number	3178790
from	0xB26444db4062440543919361d7A19db1495F5785
to	UniswapV2Factory.createPair(address,address) 0xa723C7bC9D8b7d55a9ea6db66c47b5bf27c63A39
gas	3258859 gas
transaction cost	3258859 gas 
input	0xc9c...92c30
decoded input	{
	"address tokenA": "0xA4dED08cA94057a49EB6CB98d2BEEa2857a1ba45",
	"address tokenB": "0x2bDa8F0AE0E7C584c77dD5C74c486Fe717692c30"
}
decoded output	 - 
logs	[
	{
		"from": "0xa723C7bC9D8b7d55a9ea6db66c47b5bf27c63A39",
		"topic": "0x0d3648bd0f6ba80134a33ba9275ac585d9d315f0ad8355cddefde31afa28d0e9",
		"event": "PairCreated",
		"args": {
			"0": "0x2bDa8F0AE0E7C584c77dD5C74c486Fe717692c30",
			"1": "0xA4dED08cA94057a49EB6CB98d2BEEa2857a1ba45",
			"2": "0x49EaE6000a0a39ED98CE92fa81f2efF2f70f95F8",
			"3": "1",
			"token0": "0x2bDa8F0AE0E7C584c77dD5C74c486Fe717692c30",
			"token1": "0xA4dED08cA94057a49EB6CB98d2BEEa2857a1ba45",
			"pair": "0x49EaE6000a0a39ED98CE92fa81f2efF2f70f95F8"
		}
	}
]
val	0 wei
call to UniswapV2Factory.allPairs
call to UniswapV2Factory.allPairs errored: Returned error: {"jsonrpc":"2.0","error":"invalid opcode: INVALID","id":7370203893933176}
call to UniswapV2Factory.getPair

CALL
[call]from: 0xB26444db4062440543919361d7A19db1495F5785to: UniswapV2Factory.getPair(address,address)data: 0xe6a...92c30
from	0xB26444db4062440543919361d7A19db1495F5785
to	UniswapV2Factory.getPair(address,address) 0xa723C7bC9D8b7d55a9ea6db66c47b5bf27c63A39
input	0xe6a...92c30
decoded input	{
	"address ": "0x2bDa8F0AE0E7C584c77dD5C74c486Fe717692c30"
}
decoded output	{
	"0": "address: 0x49EaE6000a0a39ED98CE92fa81f2efF2f70f95F8"
}
logs	[]
call to UniswapV2Factory.allPairsLength
CALL
[call]from: 0xB26444db4062440543919361d7A19db1495F5785to: UniswapV2Factory.allPairsLength()data: 0x574...f2ba3
from	0xB26444db4062440543919361d7A19db1495F5785
to	UniswapV2Factory.allPairsLength() 0xa723C7bC9D8b7d55a9ea6db66c47b5bf27c63A39
input	0x574...f2ba3
decoded input	{}
decoded output	{
	"0": "uint256: 1"
}
logs	[]
logs	[]
