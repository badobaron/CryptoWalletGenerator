Command line interface to generate mnemonic hd wallet in python3

Can be used to create bitcoin, bitcoin-testnet or ethereum account

Follow same pattern as this website : https://iancoleman.io/bip39/

# Before install
pip3 install mnemonic 

pip3 install bip32utils

pip3 install ethereum

# install

git clone https://github.com/MohamedLEGH/CryptoWalletGenerator
cd CryptoWalletGenerator

chmod u+x walletgen

# Usage

To generate 24 words and mnemonic
```
./walletgen --mnemonic 
output : 
  24 words
  equivalent master seed 

To generate 24 words

```
./walletgen --words
rate latin vicious music pig physical fix number raven session leaf festival indicate wrap umbrella federal begin grocery crop unfair task submit two payment
```

To generate seed

```
./walletgen --seed
7376da6f43b6e8fe46897c6343b8f14f05581b65f6b6cb296ef4098258a3a29c61073180cc0f348b9934f6abf299c107d9ecf9215ce212f7f6fea791147d8462
```

To derivate account from seed

./walletgen --datafromseed

enter the seed

enter network (ethereum or bitcoin or bitcoin-testnet)

enter the account number you want to generate

output:
  private key
  wif (only bitcoin and bitcoin-testnet)
  public key (only bitcoin and bitcoin-testnet)
  address
  
  
```


To derivate account from 24 words

./walletgen --data

enter the mnemonic 24 words

enter network (ethereum or bitcoin or bitcoin-testnet)

enter the account number you want to generate

output:
  private key
  wif (only bitcoin and bitcoin-testnet)
  public key (only bitcoin and bitcoin-testnet)
  address
  
  
```

To derivate privatekey from seed
```
./walletgen --key SEED NETWORK ACCOUNT_NUMBER
(example) :
./walletgen --key 7376da6f43b6e8fe46897c6343b8f14f05581b65f6b6cb296ef4098258a3a29c61073180cc0f348b9934f6abf299c107d9ecf9215ce212f7f6fea791147d8462 ethereum 2
output : 3aeb641849cd9583133f48d18ac88ee08e28450294f3985aa095ae164bdb9192
```

To derivate address from seed
```
./walletgen --address SEED NETWORK ACCOUNT_NUMBER
(example) :
./walletgen --address 7376da6f43b6e8fe46897c6343b8f14f05581b65f6b6cb296ef4098258a3a29c61073180cc0f348b9934f6abf299c107d9ecf9215ce212f7f6fea791147d8462 ethereum 2
output : 0x0c0F7DD7C1A12F1e151958C42e031Fd61f1df1dC
```
