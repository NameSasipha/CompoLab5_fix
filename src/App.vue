
<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { useMessageStore } from './stores/message';
import { storeToRefs } from 'pinia';
const store = useMessageStore()
const {message} = storeToRefs(store)
import {ref} from 'vue'
const sizes = ref<number>(2)
</script>

<template>
  <header class="max-h-screen leading-normal text-center ">
    <div class=" bg-yellow-600 transition duration-3000  "	 v-if="message">
      <h1>SASIPHA THONKHAN</h1>
    <h4> {{ message }}</h4></div>
    <div class="m-center	">
      <nav class="w-full space-x-2 text-center ">
        <RouterLink :to="{name: 'event-list'}">Home</RouterLink>
        <RouterLink :to="{name: 'category'}">Category</RouterLink>
        <RouterLink :to="{name: 'student'}">Student</RouterLink>

      </nav>
      <!-- <div class="size">
        <label>  Size : </label>
        <input class="sizes" type="number" v-model="sizes" />
      </div> -->
    </div>
  </header>
  <h1></h1>
  
  <h1 class="text-lime-200 mt-2 text-center" >Events for Good</h1>


  <RouterView class="text-center mt-5 " :size="sizes"/>
</template>

<!-- <style scoped>
/* header {
  line-height: 1.5;
  max-height: 100vh;
} */

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }}

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
  h4{
    font-size: 20px;
    }

  @keyframes yellowfade {
    from {
      background: yellow;
    } to {
      background: transparent;
    }
  }
  .flashMessage {
    animation: yellowfade 3s ease-in-out;
  }

</style> -->
