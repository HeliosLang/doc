---
title: Credential
sidebar_label: Credential
sidebar_class_name: enum_badge
---

# <span className="enum_badge">Credential</span>

Represents the non-staking part of an [`Address`](./address.md). Internally represented as an enum with two variants: 
  * `PubKey` (wraps [`PubKeyHash`](./pubkeyhash.md)) 
  * `Validator` (wraps [`ValidatorHash`](./validatorhash.md))

<br/>

Example instantiation:
```helios
pubkey_credential: Credential::PubKey = Credential::new_pubkey(PubKeyHash::new(#...));

validator_credential: Credential::Validator = Credential::new_validator(ValidatorHash::new(#...)); ...
```

## Associated functions

### `new_pubkey`

```helios
Credential::new_pubkey(pkh: PubKeyHash) -> Credential::PubKey
```

### `new_validator`

```helios
Credential::new_validator(vh: ValidatorHash) -> Credential::Validator
```

### `from_data`

```helios
Credential::from_data(data: Data) -> Credential
```

## Getters

### `hash`

Get the underlying hash.

```helios
pubkey_credential.hash -> PubKeyHash

validator_credential.hash -> ValidatorHash
```

## Operators

### `==`

```helios
Credential == Credential -> Bool
```

### `!=`

```helios
Credential != Credential -> Bool
```

## Methods

### `serialize`

```helios
credential.serialize() -> ByteArray
```