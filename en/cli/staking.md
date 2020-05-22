### Delegate token to consensus account

```bash
gatecli staking delegate [con-account-addr] [amount]  --from [delegator-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking delegate gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg 100000000NANOGT --from gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 --chain-id testnet
```

### Query the info of a single delegation account in the single consensus account

```bash
gatecli staking delegation [delegator-addr] [con-account-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking delegation gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg --chain-id testnet
```

### Query the info of a single delegation account in all consensus accounts

```bash
gatecli staking delegations [delegator-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking delegations gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 --chain-id testnet
```

### Redelegate

```bash
gatecli staking redelegate [src-con-account-addr] [dst-con-account-addr] [amount] --from [delegator-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking redelegate gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg gc11d0yarljl7zyksc3r9gp95saqnhjdlrtrefcwg8 100000000NANOGT --from gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 --chain-id testnet
```

### Query all redelegate records of the single delegation account

```bash
gatecli staking redelegations [delegator-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking redelegations gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 --chain-id testnet
```

### Query redelegate records of a single delegation account in two consensus accounts

```bash
gatecli staking redelegation [delegator-addr] [src-con-account-addr] [dst-con-account-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking redelegation gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg gc11d0yarljl7zyksc3r9gp95saqnhjdlrtrefcwg8 --chain-id testnet
```

### Unbind from consensus account

```bash
gatecli staking unbond [con-account-addr] [amount] --from [sender account] --chain-id [chain ID]
```
Example：

```bash
gatecli staking unbond gc11d0yarljl7zyksc3r9gp95saqnhjdlrtrefcwg8 100000000NANOGT --from gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 --chain-id testnet
```

### Query untied delegation records of a single delegation account in a single consensus account

```bash
gatecli staking unbonding-delegation [delegator-addr] [con-account-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking unbonding-delegation gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 gc11d0yarljl7zyksc3r9gp95saqnhjdlrtrefcwg8 --chain-id testnet
```

### Query untied delegation records of a single delegation account in all consensus accounts

```bash
gatecli staking unbonding-delegations [delegator-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking unbonding-delegations gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88 --chain-id testnet
```

### Query all delegation of the consensus account

```bash
gatecli staking delegations-to [con-account-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking delegations-to gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg --chain-id testnet
```

### Query all redelegate records of the consensus account

```bash
gatecli staking redelegations-from [con-account-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking redelegations-from gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg --chain-id testnet
```

### Query all unbound delegation of the consensus account

```bash
gatecli staking unbonding-delegations-from [con-account-addr] --chain-id [chain ID]
```
Example：

```bash
gatecli staking unbonding-delegations-from gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg --chain-id testnet
```

### Query stake deposit pool info

```bash
gatecli staking pool --chain-id [chain ID]
```

### Query stake deposit params

```bash
gatecli staking params --chain-id [chain ID]
```