# prettier-config-enrq

## Setup

To install `prettier-config-enrq`, just add the package name under the `devDependencies` in the `package.json`.

```
  "devDependecies": {
    ...
    "prettier-config-enrq": "emoriarty/prettier-config-enrq",
    ...
  }
```

Once the file has been saved, `npm install` or `yarn install` will do the rest.

## Configuration

If you're going to use the current prettier configuration as it is, there's no need to create a new file. It can be just added into the `package.json` as shown below.

```
{
  ...
  "prettier": "prettier-config-enrq"
}
```

In case new prettier rules must be added or just overwriting existing ones, you can create a `.prettierrc.js` file and extend from the current package.

```
module.exports = {
  ...require('prettier-config-enrq'),
  trailingComma: "es5"
}
```

It is important the file is written in javascript, a json file won't do the trick. You can read more on this [here](https://prettier.io/docs/en/configuration.html#sharing-configurations).

Current prettier options can be found in [index.json file](./index.json).
