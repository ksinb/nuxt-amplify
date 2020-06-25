<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        nuxt-amplify
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <div class="content">
        <div>
          <input
            id="jack"
            v-model="checkedNames"
            type="checkbox"
            value="Jack"
          />
          <label for="jack">Jack</label>
          <input
            id="john"
            v-model="checkedNames"
            type="checkbox"
            value="John"
          />
          <label for="john">John</label>
          <input
            id="mike"
            v-model="checkedNames"
            type="checkbox"
            value="Mike"
          />
          <label for="mike">Mike</label>
        </div>
        <div>
          <span>Checked names: {{ checkedNames }}</span>
        </div>
        <div>
          <button @click="onClick">Click</button>
          <button @click="onClick2">Click2</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Logo from '~/components/Logo.vue'

export default Vue.extend({
  components: {
    Logo,
  },
  data() {
    return {
      checkedNames: [],
    }
  },
  methods: {
    onClick() {
      throw new Error('Click')
    },
    onClick2() {
      console.log([1, 2, 3].find((item) => item % 2 === 0))
      console.log([1, 2, 3].includes(1))
    },
  },
})
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
