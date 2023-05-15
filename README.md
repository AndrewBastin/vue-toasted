# [@hoppscotch/vue-toasted](https://www.npmjs.com/package/@hoppscotch/vue-toasted)

### A Vue 3 port of the [vue-toasted](https://github.com/shakee93/vue-toasted) library.

<br />
<br />

## Install
- Install the package from npm
  ```bash
  npm install @hoppscotch/vue-toasted
  ```

## Usage
- Initialize the Vue plugin.
  For example, for a Vite Vue application
  ```js
  // main.js
  import Toasted from "@hoppscotch/vue-toasted"
  import { createApp } from "vue"
  import App from "./App.vue"
  
  // Make sure to include the default stylings
  import "@hoppscotch/vue-toasted/dist/style.css"
  
  const app = createApp(App)

  app.use(Toasted) // You can pass options as a second parameter

  ```
- Now you will be able to access `vue-toasted` in your Vue components.
  <br />
  <br />
  For Options API:
  ```js
  import { defineComponent } from "vue"

  export default defineComponent({
    mounted() {
        // Should give you access to the toasted show function
        this.$toasted.show("Hola! From Options API!")
    }
  })
  ```
  For Composition API:
  ```js
  const toast = useToasted()
  toast.show("Hola! From Composition API!")
  ```
