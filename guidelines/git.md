# Commit Messages
Commit messages follow a common syntax, providing concise and easy to read message that describes the full commit.

```
<ELEMENT CHANGED> Updates

-<ELEMENT_CHANGE_1>
```

Seperate title `<ELEMENT CHANGED> Updates` by two newlines, then for every `<ELEMENT_CHANGE_N>` add a newline and dash, creating a list.

## Example

```
System Updates

-add a way to control power level
-refactor types.py
```

# Tags & Versioning
Tags and versions follow semantic versioning (major.minor.patch) for clear and specific versioning.

Tags follow the style:

```
v<VERSION_NAME>
```

Where `<VERSION_NAME>` is prefixed by a `v`. Internal software (such as Cargo files, UI displays, etc.) are not prefixed by a `v`, following a simple:

```
<VERSION_NAME>
```

## Example

```
Software Version: "0.1.0"
Release Tag: "v0.1.0"
```
