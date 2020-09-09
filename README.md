# rabbits.finance

## Introduction
RAB is is the yield farming on EOS. The private key is burned and the contract code is open source.
The project has no pre-mine, no founder shares, no VC interests. RAB uses TVI (Total Value Inflow) as the project.
The token distribution index will not cause precipitation in the fund pool. The contract will automatically return
90% of the funds to the participating EOS accounts and donate 10% as follow-up development and operation funds.

## Token Info

- Token name: Rabbits（RAB）
- Total supply: 21000.0000
- Token contract: [rabbitstoken](https://bloks.io/account/rabbitstoken)
- Pool contract: [rabbitspoolx](https://bloks.io/account/rabbitspoolx)
- Rabbits Pool:
1. EOS: 13000 RAB
2. EOSRAM: 2700 RAB
3. USDT: 1930 RAB
4. EOSDT: 1030 RAB
5. USDE: 1030 RAB
6. USN: 1030 RAB
7. DFS: 70 RAB
8. DMD: 70 RAB
9. BOX: 70 RAB
10. NDX: 70 RAB

RAB will be distributed in only two weeks.

## Reasons for token selection
- Stable coins issued based on the EOS network (EOSDT, USDE, USN)
- EOS Development Resources (EOSRAM)
- DEX (DFS, BOX, NDX) developed based on EOS network
- The first DeFi (DMD) on EOS to achieve TVL exceeding 50 million USD

## Security

### No pool of funds
RAB uses the TVI model as a project value assessment, and will not lock any funds in the contract, so it can ensure the 100% security of the contract.

### Private keys burned
RAB has given the authority to the system account `eosio`, the project has no control and cannot update the contract (unless the 21 BPs agree).

### How to verify the contract

- EOSIO Version: 2.0.5
- EOS.CDT Version: 1.7.0

```
cleos get code rabbitstoken > rabbitstoken.hash
cleos get code rabbitspoolx > rabbitspoolx.hash
```

Build from source:
```
./build.sh
```

Compare the hash:
`shasum -a 256 build/contracts/xpool/xpool.wasm` of `rabbitspoolx.hash`
`shasum -a 256 build/contracts/eosio.token/eosio.token.wasm` of `rabbitstoken.hash`

- Pool Hash: f35c11106d5987fd97a6d0bcb5ee765bc76fb1c089a29dab31efec40522774d4
- Token Hash: f6a2939074d69fc194d4b7b5a4d2c24e2766046ddeaa58b63ddfd579a0193623
