# nuxt-split-chunks-max-size
Nuxt.js split chunks plugin webpack plugin max size configuration

_nuxt.config.js_

```js
const isProd = process.env.NODE_ENV === 'production';

export default {
  build: {
    analyze: process.env.NODE_ENV === 'development',
    extend (config, { isClient }) {
      if (isProd && isClient) {
        config.optimization.splitChunks.maxSize = 249856; // 244 Kib
      }
    },
  },
};
```
