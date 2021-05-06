# umi-plugin-flexible

umijs plugin that automatically injects flexible scripts and converts pixel units to rem units

### Install

```bash
$ npm i umi-plugin-flexible -D
# or
$ yarn add umi-plugin-flexible -D
```

### Usage

Config plugin in .umirc.ts

```javascript
import { defineConfig } from 'umi';

export default defineConfig({
  postcss: {
    rootValue: 37.5,
    propList: ['*'],
  },
  plugins: [require.resolve('umi-plugin-flexible')],
});
```


Flexible scripts are automatically injected into the head

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Will be generated automatically -->
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,viewport-fit=cover"
    />
    <script>
    // flexible script
    </script>
  </head>
  <body></body>
</html>
```

### Resource

- https://github.com/cuth/postcss-pxtorem
- https://github.com/posuihushui/flexible.js
