<script setup lang="ts">
  import { ref } from 'vue';
  import MyComponent from './component.vue'
  
  export class TestClass {
    private privateField = "";
    public publicField = "";
  }
  
  const objects = ref<TestClass[]>([]);
</script>

<template>
  <MyComponent v-for="obj in objects" :key="obj.publicField" :test-prop="obj" />
  <!--                                                        ^^^ This will error -->
</template>


