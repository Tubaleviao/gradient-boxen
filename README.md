<!-- markdownlint-disable MD010 MD033 MD001 -->

# gradient-boxen

> **A combo of gradient-string + boxen**

![image](https://user-images.githubusercontent.com/38729705/193000578-d584d1fd-e882-4a69-8d1a-ad8a9c8607ce.png)

**gradient-boxen is a library that allows you to create fully customizable _gradient boxes_ in the terminal. Because what's better than a gradient-y string and a cool terminal box? A gradient box!**

**It effectively combines the popular NPM packages [boxen](https://github.com/sindresorhus/boxen/) and [gradient-string](https://github.com/bokub/gradient-string) into one unified package.**

## 🛠️ Install

Using [npm](https://www.npmjs.com/)

```text
npm i gradient-boxen
```

> Please note that this package is ESM only. Please check out [this guide](https://gist.github.com/sindresorhus/a39789f98801d908bbc7ff3ecc99d99c) on how to convert your project to ESM

---

## 🔗 Usage

> Please note that this package will properly display gradient boxes only in terminals with [TrueColor](https://en.wikipedia.org/wiki/Color_depth#True_color_(24-bit)) support, ie, 16 million colors, in order to properly display the gradients

- Using an array of gradient colors

```js
import gradientBox from 'gradient-boxen';

console.log(
  gradientBox(
    'I love gradients!',
    {
      borderStyle: 'round',
      padding: 1,
      margin: 1,
    },
    ['#11998e', '#38ef7d']
  )
);
```

Output:

![image](https://user-images.githubusercontent.com/38729705/193009542-ef7ac6dd-4e60-484c-979b-172bf2337d63.png)

- Using a predefined preset

```js
import gradientBox from 'gradient-boxen';

console.log(
  gradientBox(
    'I love gradients!',
    {
      borderStyle: 'round',
      padding: 1,
      margin: 1,
    },
    'fruit'
  )
);
```

Output:

![image](https://user-images.githubusercontent.com/38729705/193009624-e777c4c7-4613-4116-aa3d-f45b42165332.png)

<details>

<summary>List of available presets</summary>

![Presets](https://camo.githubusercontent.com/e6afd27113a963ec77568597457b13ec43cd76c31a02e6dad7aeb8553733c578/687474703a2f2f6269742e6c792f3275467967724c)

These presets have been ported from [gradient-string](https://github.com/bokub/gradient-string#available-built-in-gradients)

</details>

---

## 🔮 API

### `gradientBox(boxText, boxOptions, gradientOptions)`

#### boxText

Type: `string`

Text inside the box. Can be multiline too.

> Please note that all pre-existing ANSI colors are stripped from the text, so that the gradient can be properly displayed

#### boxOptions

Type: `object`

The configuration options for the box as per the [boxen](https://github.com/sindresorhus/boxen#options) package

Options include:

```js
{
  borderColor?: string
  borderStyle?: string
  dimBorder?: boolean
  padding?: number
  margin?: number
  float?: 'left' | 'right' | 'center'
  backgroundColor?: 'string'
  textAlignment?: 'left' | 'right' | 'center';
  title?: string
  titleAlignment?: 'left' | 'right' | 'center'
  width?: number
  height?: number
  fullscreen?: boolean
}
```

#### gradientOptions

Type: `string` or `string[]`

The gradient preset (or a set of gradients) to be used for the box. Can be a string or an array of valid color codes.

A list of presets can be found [here](https://github.com/bokub/gradient-string#available-built-in-gradients)

---

## ❤️ Support

You can support further development of this project by **giving it a 🌟** and help me make even better stuff in the future by **buying me a ☕**

<a href="https://www.buymeacoffee.com/savioxavier">
<img src="https://cdn.buymeacoffee.com/buttons/v2/default-blue.png" height="50px">
</a>

<br>

**Also, if you liked this repo, consider checking out my other projects, that would be real cool!**

---

## 💫 Attributions and special thanks

- [boxen](https://github.com/sindresorhus/boxen/)
- [gradient-string](https://github.com/bokub/gradient-string)
