# danger-plugin-spellcheck

[![Build Status](https://travis-ci.org/orta/danger-plugin-spellcheck.svg?branch=master)](https://travis-ci.org/orta/danger-plugin-spellcheck)
[![npm version](https://badge.fury.io/js/danger-plugin-spellcheck.svg)](https://badge.fury.io/js/danger-plugin-spellcheck)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

> Spell checks any created or modified markdown files in a GitHub PR using [node-markdown-spellcheck](https://github.com/lukeapage/node-markdown-spellcheck).

## Usage

Install:

```sh
yarn add danger-plugin-spellcheck --dev
```

At a glance:

```js
// dangerfile.js
import spellcheck from 'danger-plugin-spellcheck'

schedule(spellcheck())
```

You can have a shared repo for the settings for your spell checking: 

```js
// dangerfile.js
import spellcheck from 'danger-plugin-spellcheck'

schedule(
  spellcheck({ settings: "artsy/artsy-danger@spellcheck.json" })
)
```

The JSON should look something like like:

```json
{
  "ignore": ["orta", "artsy", "github"],
  "whitelistFiles": ["README.md"]
}
```

*Note:* The `"ignores"` section is case in-sensitive.

## Changelog

See the GitHub [release history](https://github.com/orta/danger-plugin-spellcheck/releases).

## Credits

This was created by [Orta Therox](https://twitter.com/orta) and [Yuki Nishijima](https://twitter.com/yuki24) in an amazing pairing session on cold thursday before an [Artsy Happy Hour](https://github.com/artsy/meta/blob/master/meta/happy_hour.md).

## Contributing

See [CONTRIBUTING.md](contributing.md).
