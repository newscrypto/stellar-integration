# NWC Stellar Java-Script

## Installing

Using npm to include js-stellar-sdk in your own project:

```
npm install --save stellar-sdk
```

### Create NWC asset object

```
const nwcAsset = new StellarSdk.Asset("NWC", "GAAPUOQWOZAG3PENRN7FEPYWXVGJBJVBL6EUE2ZHN5TSY7WBXQDO7AY2");
```

### Create trustline operation

```
StellarSdk.Operation.changeTrust({
    // Asset we want to add trustline
    asset: nwcAsset,
    limit: 99999999999999,
})
```

### Create payment operation for asset

```
StellarSdk.Operation.payment({
    destination: receiverPublicKey,
    // Set asset
    asset: nwcAsset,
    // Specify 350.1234567 NWC. They are represented in JS Stellar SDK in string format
    // to avoid errors from the use of the JavaScript Number data structure.
    amount: '350.1234567',
})
```

### Note

All examples are for public network.

### Documentation of js stellar sdk

[js-stellar-sdk](https://github.com/stellar/js-stellar-sdk)