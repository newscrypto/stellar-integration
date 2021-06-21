# NWC Stellar Python

## Installing

Install and update using pipenv or pip:

```
pip install stellar-sdk==3.3.5
```

### Create NWC asset object

```
nwcAsset = Asset("NWC", "GAAPUOQWOZAG3PENRN7FEPYWXVGJBJVBL6EUE2ZHN5TSY7WBXQDO7AY2")
```

### Create trustline operation

```
.append_change_trust_op(
    asset_code=nwcAsset.code,
    asset_issuer=nwcAsset.issuer
)
```

### Create payment operation for asset

```
.append_payment_op(
    receiver_public_key,
    "350.1234567",
    asset_code=nwcAsset.code,
    asset_issuer=nwcAsset.issuer
)
```

### Note

All examples are for public network.

### Documentation of js stellar sdk

[js-stellar-sdk](https://github.com/stellar/js-stellar-sdk)