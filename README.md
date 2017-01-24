Quorum-Genesis
==============

Utility for [Quorum](https://github.com/jpmorganchase/quorum) to help
populate the genesis file with voters and blockmakers.

Setup
-----
 * Install Node.js
 * Install this package `npm install`


Use
---

 1. Send JSON to STDIN
 2. It will output genesis to STDOUT

```
 $ cat the-json-below.json | node create-genesis.js > genesis.json
```

STDIN JSON should be in the following format:

```json
{
  "threshold": 3,
  "voters": [
    "0x0fbdc686b912d7722dc86510934589e0aaf3b55a",
    "0x9186eb3d20cbd1f5f992a950d808c4495153abd5",
    "0x0638e1574728b6d862dd5d3a3e0942c3be47d996"
  ],
  "makers": ["0xca843569e3427144cead5e4d5999a3d0ccf92b8e"]
}
```

Where:

* `threshold` is the number of required voters
* `voters` is a list of voter addresses
* `makers` is a list of blockmaker addresses
