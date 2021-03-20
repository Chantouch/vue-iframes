# vue-iframes
> Vue js component for creating dynamic async iframes based on Aaron Peter's article: http://www.aaronpeters.nl/blog/iframe-loading-techniques-performance?%3E#dynamic

[![Latest Version on NPM](https://img.shields.io/npm/v/vue-iframes.svg?style=flat-square)](https://npmjs.com/package/vue-iframes)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![npm](https://img.shields.io/npm/dt/vue-iframes.svg?style=flat-square)](https://npmjs.com/package/vue-iframes)
[![npm](https://img.shields.io/npm/dm/vue-iframes.svg?style=flat-square)](https://npmjs.com/package/vue-iframes)

## Requirements
* [Vue.js](http://vuejs.org/) (^v2.1.4)

## Vue Support

Supports on Vue >= 2

## Installation and Usage

```npm
npm install vue-iframes
```
```yarn
yarn vue-iframes
```

```javascript
import Vue from 'vue'
import VueIframe from 'vue-iframes'

Vue.use(VueIframe, {/* rest of options */})
```

## ♻️ Usage with Nuxt.js

Add `vue-iframes/nuxt` to modules section of `nuxt.config.js`

```js
export default {
    modules: [
        // Simple usage
        'vue-iframes/nuxt',
        // Passing options in module configuration
        ['vue-iframes/nuxt', {/* rest of options */}]
    ],
    // Passing options in module top level configuration
    vueIframes: {/* rest of options */}
}
```

## Components
```js
<template>
  <vue-iframe
    :src="src"
    allow="camera *; geolocation *; microphone *; autoplay *"
    frame-id="my-ifram"
    @load="onLoad"
    name="my-frame"
    width="150px"
    height="200px"
  />
</template>

<script>
export default {
  name: 'MyIframe',
  data: () => ({
    myIframe: null
  }),
  methods: {
    onLoad(frame) {
      this.myIframe = frame.contentWindow
    }
  }
}
</script>
```

## Props

Prop                  | Description            |    Required        | Default
----------------------| ---------------------- | ------------------ | -----------
**src**               | The iframe resource    | true
**crossorigin**       | Cross origin           | false              | anonymous
**target**            | Target of iframe       | false              | _parent
**className**         | Iframe's class         | false              | null
**allow**             | Iframe's allow         | false              | 'camera *; geolocation *; microphone *; autoplay *'
**name**              | Iframe's name          | false              | 'vue-iframes'
**frame-id**          | Iframe's id            | false              | 'vue-iframes'

## Events

Name                  | Description            
----------------------| ---------------------- 
**iframe-load**       | When the iframe is loaded    
**load**              | When the iframe is ready    

### Contributing

Pull requests are welcome, or open up an issue if you have ideas for additional functionality, new features or bugs.

# Contact

Twitter [@DevidCs83](https://twitter.com/DevidCs83)
