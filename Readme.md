transform-json-types
[![All Contributors](https://img.shields.io/badge/all_contributors-4-orange.svg?style=flat-square)](#contributors)
=========

An utility to generate Flow, TypeScript, Rust Serde Struct and Scala Case Class from JSON.

**Note** : It also detects optional properties for TS/Flow from a Collection.

Installation
============

```
npm install transform-json-types
```

The online REPL is available at
- [JSON to Flow](https://transform.now.sh/json-to-flow-types)
- [JSON to TypeScript](https://transform.now.sh/json-to-ts-interface)
- [JSON to Scala Case Class](https://transform.now.sh/json-to-scala-case-class)
- [JSON to Rust Serde](https://transform.now.sh/json-to-rust-serde)

Basic Usage
===========
```js
import transform from "transform-json-types"

const json = `{
  "hello": "world"
}`

console.log(transform(json, {
  lang: "typescript"
}))

// interface RootJson {
//   hello: string
// }

console.log(transform(json, {
	lang: "rust-serde"
}))

// #[derive(Serialize, Deserialize)]
// struct RootInterface {
//   hello: String,
// }
```

API
===
### transform(json, [options])

#### json : `String | JSON`
You can pass a parsed JSON or a stringified JSON.

### Options
Option|Default|Description
----|-----|-----
lang| 'flow'| One of `flow`, `typescript`, `scala`, `io-ts` or `rust-serde`
rustCase| 'camelCase' | either snakeCase or camelCase

### Inspirations
Majority of the inspiration was from [xperiment](https://github.com/xperiments)'s [json2dts](https://github.com/xperiments/json2dts)

### Development
1. Fork and clone the repo.
1. Create a new branch.
1. Create features or fix bugs.
1. Write test to improve stability.
1. Open a PR.

License
=======
MIT @ [Ritesh Kumar](https://twitter.com/ritz078)





## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars3.githubusercontent.com/u/5389035?v=4" width="100px;"/><br /><sub><b>Ritesh Kumar</b></sub>](http://riteshkr.com)<br />[💻](https://github.com//transform-json-types/commits?author=ritz078 "Code") [📖](https://github.com//transform-json-types/commits?author=ritz078 "Documentation") [🤔](#ideas-ritz078 "Ideas, Planning, & Feedback") | [<img src="https://avatars2.githubusercontent.com/u/47542?v=4" width="100px;"/><br /><sub><b>Florian Gilcher</b></sub>](http://asquera.de)<br />[💻](https://github.com//transform-json-types/commits?author=skade "Code") | [<img src="https://avatars0.githubusercontent.com/u/417709?v=4" width="100px;"/><br /><sub><b>Pedro Casaubon</b></sub>](http://www.xperiments.in)<br />[💻](https://github.com//transform-json-types/commits?author=xperiments "Code") [🤔](#ideas-xperiments "Ideas, Planning, & Feedback") | [<img src="https://avatars2.githubusercontent.com/u/179534?v=4" width="100px;"/><br /><sub><b>stereobooster</b></sub>](https://github.com/stereobooster)<br />[💻](https://github.com//transform-json-types/commits?author=stereobooster "Code") |
| :---: | :---: | :---: | :---: |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!
