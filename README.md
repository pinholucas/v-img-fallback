![npm bundle size](https://img.shields.io/bundlephobia/minzip/v-mask)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/probil/v-mask/master/LICENSE)
[![Vue3](https://img.shields.io/badge/Vue-3.x-brightgreen.svg)](https://vuejs.org/)
<h1 align="center"> Vue Image Fallback </h1>
<h4 align="center">for Vue 3</h4>
<br/>
<br/>

## 📄 Description
> v-img-fallback

Vue image placeholder directive for broken images.

If you like this project, please give it a star, and consider following the author. :)

## ⚙️ Install & Usage

### Install with NPM or Yarn

`npm install v-img-fallback --save`

`yarn add v-img-fallback`

### Install globally
```js
import { createApp } from 'vue';
import VueImgFallback from 'v-img-fallback';

const app = createApp({})

app.use(VueImgFallback, {
  loading: 'path/to/loading/image',
  error: 'path/to/error/image'
});
```

### Install locally
```vue
<template>
  <img src="foo.png" v-img-fallback="imgFallback">
</template>

<script>
import { ImgFallback } from 'v-img-fallback';

export default {
  directives: {
    ImgFallback
  },
  data: () => {
    imgFallback: {
      loading: 'path/to/loading/image',
      error: 'path/to/error/image'
    }
  }
};
</script>
```

## API

This directive can receive `string` or `object` value.

**string**

Path or image url. This value will be used in both loading and error state.

**object**

```js
{
  loading: 'path/to/loading/image',
  error: 'path/to/error/image'
}
```

### Sample - pass a string

```vue
<template>
  <img src="foo.png" v-img-fallback="path/to/placeholder">
</template>
```

### Sample - pass an object
```vue
<template>
  <img src="foo.png" v-img-fallback="imgFallback">
</template>

<script>
  export default {
    data: () => {
      imgFallback: {
        loading: 'path/to/loading/image',
        error: 'path/to/error/image'
      }
    }
  }
</script>
```

**Tips**

`loading` value can be a `.gif` **Gee**. **Ahy**. **Ef**. *(I will die with dignity LOL)*.

**Made with :heart: by Jofferson Ramirez Tiquez & ported to Vue 3 by Lucas Pinho (its not a big thing, k) **
