# Interaction
## On testnet

Create wallet:

```
erdpy --verbose wallet derive farmer.pem --mnemonic --index 0
```

Get HEX address from BECH32 address:

```
erdpy wallet bech32 --decode erd1q049n3qp2wc0jra5rd83za69u3ze0we0yqm7ax9hghjsde4jeeyqc78p2s
```

Deploy & interact with contract:

```
erdpy --verbose contract build crowdfunding
```

```
erdpy --verbose contract deploy --project=crowdfunding --recall-nonce --pem="../farmer.pem" --gas-limit=60000000 --arguments 100 1640822400 0x45474c44 --outfile="deploy-testnet.interaction.json" --send --proxy="https://testnet-api.elrond.com" --chain=T
```

```
erdpy contract call erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --recall-nonce --pem="../farmer.pem" --gas-limit=10000000 --function="fund"  --value=5 --proxy="https://testnet-gateway.elrond.com" --chain=T --send
```

```
erdpy contract call erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --recall-nonce --pem="../farmer.pem" --gas-limit=10000000 --function="claim"  --proxy="https://testnet-gateway.elrond.com" --chain=T --send
```

View contract info:

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --function="getDeadline" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --function="status" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --function="getTarget" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --function="getCrowdfundingTokenIdentifier" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --function="getDeposit" --arguments "0x03EA59C40153B0F90FB41B4F117745E44597BB2F2037EE98B745E506E6B2CE48" --proxy="https://testnet-gateway.elrond.com"
```

```
erdpy --verbose contract query erd1qqqqqqqqqqqqqpgqg2xqcug6ghcftlrufdge3a5tx52r8z3yeeyq649nn6 --function="getCrowdfundingTokenName" --proxy="https://testnet-gateway.elrond.com"
```
