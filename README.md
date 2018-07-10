# All-for-react-native

# #  1. Chuẩn bị extendsion for VsCode
- Cài đặt Extendsion: Settings Sync 
- Download setting from Github

# #  2. Chuẩn bị cho AutoCompelete:
Nguồn: https://github.com/Microsoft/TypeScript-React-Native-Starter
- cd vào project hiện tại
```sh
yarn add --dev typescript
yarn add --dev react-native-typescript-transformer
yarn tsc --init --pretty --jsx react
touch rn-cli.config.js
yarn add --dev @types/react @types/react-native
```

The `tsconfig.json` file contains all the settings for the TypeScript compile.
The defaults created by the command above are mostly fine, but open the file and uncomment the following line:

```js
{
  ...
  // "allowSyntheticDefaultImports": true,  /* Allow default imports from modules with no default export. This does not affect code emit, just typechecking. */
  ...
}
```

The `rn-cli.config.js` contains the settings for the React Native TypeScript Transformer.
Open it and add the following:

```js
module.exports = {
  getTransformModulePath() {
    return require.resolve("react-native-typescript-transformer");
  },
  getSourceExts() {
    return ["ts", "tsx"];
  }
};
```
# #  3. Chuẩn bị cho check Lint:
https://medium.com/@oguzhancakmak/react-native-eslint-setup-46ec0586e21b
Lần đầu tiên

```sh
npm install -g eslint
```

```sh
npm install — save-dev eslint-config-rallycoding
```

Make a new file called .eslintrc. Copy and paste the content below into the file.
```js
{
“extends”: “rallycoding”
}
```
