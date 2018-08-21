# Tiny Crypto

Simpler (but secure) crypto utility alternative to the native crypto module shipped with Node.
Tiny Crypto is only for strings like access tokens, secure names, secure Ids, etc and not meant for passwords! (passwords shouldn't be decryptable therefore use [bcrypt](https://www.npmjs.com/package/bcrypt))

## Install

```bash
yarn add tiny-crypto # or npm install tiny-crypto
```

## Use

Keep in mind this is node-only! Here's how you can use it:

```js
// Import!
import TinyCrypto from 'tiny-crypto'

// Init!
const tinyCrypto = new TinyCrypto('secretk3y!') // Ideally from an environment variable

// Use!
const encryptedString = tinyCrypto.encrypt('bacon')
const decryptedString = tinyCrypto.decrypt(encryptedString)

console.log(encryptedString) // 5590fd6409be2494de0226f5d7
console.log(decryptedString) // bacon
```

## Flow Type

I ship a flow type version too, feel free to send a PR if there's any issues. I'm here.

## PRs welcome!

## Idea

- Base code taken from [Cryptr](https://github.com/MauriceButler/cryptr)

## MIT

- Modernized by [Mo Rajabifard](https://twitter.com/morajabi)
