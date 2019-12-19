# nuxt-split-chunks-max-size
Nuxt.js split chunks plugin webpack plugin max size configuration

_nuxt.config.js_

```js
export default {
  build: {
    extend(config, { isClient }) {
      const isProd = process.env.NODE_ENV === 'production';
      if (isProd && isClient) {
        config.optimization.splitChunks.maxSize = 249856; // 244 Kib
      }
    },
  },
};
```

see: https://webpack.js.org/plugins/split-chunks-plugin/
