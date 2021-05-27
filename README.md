# babylon-import-test

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

```

For detailed explanation on how nuxt work, check out [the documentation](https://nuxtjs.org).



## The Babylon issue

- So the actual issue is in ` /pages/index.vue`. **Nuxt** is component based, so the Babylon code is inside a *mounted(){...}* method.
The same file contains the **html** (thus the canvas for rendering) in a `<template>` tag, the **typescript** with the *imports* and the **CSS** in a `<style>` tag.
- The `test.glb` file which is the target of *SceneLoader.ImportMeshAsync()* lives in `/static/` which contains the public files
