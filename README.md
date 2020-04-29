# Thanks [zetachang/react-native-dotenv](https://github.com/zetachang/react-native-dotenv)

# Add Feature

Add BUNDLE_ENV, You can add a `BUNDLE_ENV=staging` in the react native bundle command, like `BUNDLE_ENV=staging react-native bundle --platform android --dev false`
Then `.env.development` replace to `.env.staging`. `staging` can be anything.

# babel-plugin-dotenv

Loads environment variables from a .env file through `import` statement.

## Installation

```sh
$ npm install babel-plugin-dotenv
```

## Usage

**.babelrc**

```json
{
  "plugins": [["babel-plugin-dotenv", {
      "replacedModuleName": "babel-dotenv"
   }]]
}
```

**.env**

```
DB_HOST=localhost
DB_USER=root
DB_PASS=s1mpl3
```

In **whatever.js**

```js
import { DB_HOST, DB_USER, DB_PASS } from "babel-dotenv"
db.connect({
  host: DB_HOST,
  username: DB_USER,
  password: DB_PASS
});
```
