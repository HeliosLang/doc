---
title: Option
sidebar_label: Option
sidebar_class_name: enum_badge
---

# <span className="enum_badge">Option</span>

`Option[`*`SomeType`*`]` is an enum used to represent an optional value. Its type syntax takes one type parameter. An option has two variants:
  * `Some`
  * `None`

<br/>

Example:
```helios
option_some: Option[Int] = Option[Int]::Some{42};
option_none: Option[Int] = Option[Int]::None; ...
```

## Associated functions

### `from_data`

```helios
Option[SomeType]::from_data(data: Data) -> Option[SomeType]
```

## Getters

### `Option[SomeType]::Some`

#### `some`

Returns content of `Option[`*`SomeType`*`]::Some`.

```helios
option_some.some -> SomeType
```

> **Note**: this getter doesn't exist on `Option[`*`SomeType`*`]::None`.

## Operators

### `==`

```helios
Option[SomeType] == Option[SomeType] -> Bool
```

### `!=`

```helios
Option[SomeType] != Option[SomeType] -> Bool
```

## Methods

### `map`

Maps `None` to `None` and `Some` to `Some`.

```helios
option.map[NewSomeType](
    fn: (some: OldSomeType) -> NewSomeType
) -> Option[NewSomeType]
```

### `serialize`

```helios
option.serialize() -> ByteArray
```

### `show`

Returns a string representation of the option, and, in case of `Some`, its content. This can be useful for debugging.

```helios
option.show() -> String
```

### `unwrap`

Returns the value wrapped by `Some`. Throws an error if `None`.

```helios
option.unwrap() -> SomeType
```