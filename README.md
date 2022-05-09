# svelte-hidden-email

Obfuscate email addresses from bots in your svelte project

## Installation 🔧

First you need a [Svelte](https://svelte.dev) 3 project. Its starter template lives at https://github.com/sveltejs/template.

Then install the component by running the following command in your project's directory:

```sh
npm install svelte-hidden-email
```

## Features ❤

* Zero dependencies!
* Protects you from 99.9% of scrapping bots
* Renders an empty standard `<a>` tag

## How to use 🚀

1. First import the component on your svelte page's script section.

```js
import HiddenEmail from 'svelte-hidden-email/src/index.js'
```

2. Call the component where you want it to be placed e.g.:

```html
<HiddenEmail to="user@domain.tld" title="Send us an email" />
```

_If you input an invalid email address nothing will be rendered and a console error will be produced._

## How it works 🔮

The email is rendered inside a CSS psuedo-element leaving the `<a>` tag empty.

## The Cons ❌

* Bots that do OCR can still scrap emails hidden with this trick

## Contribution 🖇️

Feel free to fork. If you find a bug or got something great to add make a pull request!

## Authors ✒️

* ** John Rallis ** - * Initial Work * - [rallisf1](https://github.com/rallisf1)

You can also look at the list of all the [contributors](https://github.com/rallisf1/svelte-hidden-email/contributors) who have participated in this project. 

## License 📄

This project is free to use, edit & distribute under the GNU GPLv3 License.

## Expressions of Gratitude 🎁

* Tell others about this project 📢 
* Buy me a beer 🍺 or coffee ☕ | ₿ [Crypto](https://freewallet.org/id/rallisf1/) |💰 [Cash](https://www.paypal.me/rallisf1) 
* Publicly thanks 🤓

---
⌨️ with ❤️ by  [rallisf1](https://github.com/rallisf1) 😊