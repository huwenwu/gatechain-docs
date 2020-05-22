### Create a Vault account

```
POST  /vault-account/create/{base-account}
```
parameter:

| parameter name | description |
| :----| :---- |
| base-account | base account |

request BODY example ：

%accordion%json%accordion%

```
{
  "base_req": {
    "from": "gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88",
    "memo": "",
    "chain_id": "testnet",
    "account_number": "0",
    "sequence": "4",
    "gas": "200000",
    "gas_adjustment": "1.2",
    "fees": [
      {
        "denom": "NANOGT",
        "amount": "5000"
      }
    ],
    "simulate": false
  },
  "amount": [
    {
      "denom": "NANOGT",
      "amount": "500000000"
    }
  ],
  "vault_req":{
    "security": "gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88",
    "pubkey": "",
    "delay_height": "100",
    "clear_height": "50000"
  }
}
```

%/accordion%

return:

%accordion%json%accordion%

```
{
    "type":"StdTx",
    "value":{
        "msg":[
            {
                "type":"MsgCreateVault",
                "value":{
                    "from_address":"gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88",
                    "to_address":"gc115ljwsxqhxvu54ndg95kyxn7f82uj2yk3epx4ek",
                    "security_address":"gc11kxgm58wpfr6dch276wwtuq07m8v7g8s9krjx88",
                    "delay_height":"100",
                    "clearing_height":"50000",
                    "amount":[
                        {
                            "denom":"NANOGT",
                            "amount":"500000000"
                        }
                    ],
                    "pubkey":""
                }
            }
        ],
        "fee":{
            "amount":[
                {
                    "denom":"NANOGT",
                    "amount":"5000"
                }
            ],
            "gas":"200000"
        },
        "signatures":null,
        "memo":"",
        "valid_height":null
    }
}
```

%/accordion%

### Change clearing height

```
POST /vault-account/update-clearing-height
```

request BODY example ：

%accordion%json%accordion%

```
{
  "base_req": {
    "from": "vault115ljwsxqhxvu54ndg95kyxn7f82uj2yk380ucm4",
    "memo": "",
    "chain_id": "testnet",
    "account_number": "0",
    "sequence": "4",
    "gas": "200000",
    "gas_adjustment": "1.2",
    "fees": [
      {
        "denom": "NANOGT",
        "amount": "5000"
      }
    ],
    "simulate": false
  },
  "clearing_height": "6200"
}
```

%/accordion%

return：

%accordion%json%accordion%

```
{
    "type":"StdTx",
    "value":{
        "msg":[
            {
                "type":"MsgUpdateClearingHeight",
                "value":{
                    "vault_address":"gc115ljwsxqhxvu54ndg95kyxn7f82uj2yk3epx4ek",
                    "clearing_height":"6200"
                }
            }
        ],
        "fee":{
            "amount":[
                {
                    "denom":"NANOGT",
                    "amount":"5000"
                }
            ],
            "gas":"200000"
        },
        "signatures":null,
        "memo":"",
        "valid_height":null
    }
}
```

%/accordion%

### Clear transaction

```
POST /vault-account/clear
```

request BODY example ：

%accordion%json%accordion%

```
{
    "base_req": {
    "from": "gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg",
    "memo": "",
    "chain_id": "testnet",
    "account_number": "0",
    "sequence": "4",
    "gas": "200000",
    "gas_adjustment": "1.2",
    "fees": [
      {
        "denom": "NANOGT",
        "amount": "5000"
      }
    ],
    "simulate": false
  },
  "vaults": ["vault115ljwsxqhxvu54ndg95kyxn7f82uj2yk380ucm4"]
}
```

%/accordion%

return：

%accordion%json%accordion%

```
{
    "type":"StdTx",
    "value":{
        "msg":[
            {
                "type":"MsgClearVaultAccount",
                "value":{
                    "from_address":"gc11prwhekvxf9qzs0vfnnznx8ax3kt5tq8g3dhvkg",
                    "vault_address":[
                        "gc115ljwsxqhxvu54ndg95kyxn7f82uj2yk3epx4ek"
                    ]
                }
            }
        ],
        "fee":{
            "amount":[
                {
                    "denom":"NANOGT",
                    "amount":"5000"
                }
            ],
            "gas":"200000"
        },
        "signatures":null,
        "memo":"",
        "valid_height":null
    }
}
```

%/accordion%

### Query all revocable transactions  of a Vault Account 

```
GET  /vault-account/list-revocable-txs/{vault-account}
```
parameter:

| parameter name | description |
| :----| :---- |
| vault-account | Vault Account |

return：

%accordion%json%accordion%

```
{
    "height":"6947",
    "result":[
        {
            "height":"6947",
            "msg_index":"0",
            "tokens":[
                {
                    "amount":"5",
                    "denom":"NANOGT"
                }
            ],
            "tx_hash":"REVOCABLEPAY-BB042E7853D6E32C6F81E0205A3CDD5FDA6545F2A7E92627E50EA19F86EFD6B8"
        }
    ]
}
```

%/accordion%