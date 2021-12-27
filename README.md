# Interaction
## On testnet

Create wallet:

```
erdpy --verbose wallet derive farmer.pem --mnemonic
```

Deploy & interact with contract:

```
erdpy --verbose contract build crowdfunding
```

```
erdpy --verbose contract deploy --project=crowdfunding --recall-nonce --pem="farmer.pem" --gas-limit=60000000 --arguments 500000000000 123000 0x45474c44 --outfile="deploy-testnet.interaction.json" --send --proxy="https://testnet-api.elrond.com" --chain=T
```

```
erdpy contract call erd1qqqqqqqqqqqqqpgql8qtlrmu3886qz6cke9dspy7f7c9g2j9eeyq2297tj --recall-nonce --pem="farmer.pem" --gas-limit=10000000 --function="fund"  --value=5 --proxy="https://testnet-gateway.elrond.com" --chain=T --send
```

View contract info:

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgql8qtlrmu3886qz6cke9dspy7f7c9g2j9eeyq2297tj --function="getDeadline" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgql8qtlrmu3886qz6cke9dspy7f7c9g2j9eeyq2297tj --function="status" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgql8qtlrmu3886qz6cke9dspy7f7c9g2j9eeyq2297tj --function="getTarget" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgql8qtlrmu3886qz6cke9dspy7f7c9g2j9eeyq2297tj --function="getCrowdfundingTokenIdentifier" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgql8qtlrmu3886qz6cke9dspy7f7c9g2j9eeyq2297tj --function="getCurrentFunds" --proxy="https://testnet-gateway.elrond.com"
```
