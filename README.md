# Vue3-Waline
Waline Module for Vuejs 3.0

## How to use it?
### Step 1 - Install Waline client from npm
```
npm install @waline/client
```

### Step 2 - Import this vue module
Here is a example

- For VitePress:
```javascript
// .vitepress/theme/index.ts

import { h } from 'vue'
import Theme from 'vitepress/theme'
import './style.css'

import Walineinit from '../../components/Walineinit.vue'; // Import this Vue file

export default {
  extends: Theme,
  Layout: () => {
    return h(Theme.Layout, null, {
      // https://vitepress.dev/guide/extending-default-theme#layout-slots
    })
  },
  enhanceApp({ app, router, siteData }) {
    // ...
    app.component('Walineinit', Walineinit)
  }
}
```

### Step 3 - Use it
Here is a example

```html
<Walineinit />
```
